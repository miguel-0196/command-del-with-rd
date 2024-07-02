### UBUNTU: The command not only delete the file(folder) but also overwrite with random bytes.
find tmpName -type f -exec shred -zvu -n 5 {} \;

### MACOS: First is to overwrite with random bytes and second is to delete file(folder).
find tmpName -type f -exec dd if=/dev/random bs=1 count=100 2>/dev/null of={} \;
rm -rf tmpName

### Ignore file and dir
! -name '*.txt'
! -path '*/node_module*'
