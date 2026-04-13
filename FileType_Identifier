def magic_bytes():
    return{
        "png" : b'\x89PNG\r\n\x1a\n',
        "jpeg" : b'\xff\xd8\xff\xe0',
        "pdf" : b'%PDF-',
        "gif" : b'GIF8',
        "zip" : b'PK\x03\x04'
        }
        
def file_magic():
    file = input("Enter the file path: ")
    
    signature = magic_bytes()
    
    max_length = max(len(sig) for sig in signature.values())
    
    with open(file, 'rb') as f:
        header = f.read(max_length)
    
    for file_type, sig in signature.items():
            if header.startswith(sig):
                print("Filetype Detected:", file_type)
        
if __name__ == "__main__":
    file_magic()
