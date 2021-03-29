---
description: Código de ejemplo que muestra cómo utilizar la función CreateFile para crear un nuevo archivo o abrir un archivo existente.
ms.assetid: 04e089a7-c559-4a35-a38b-e1acdf3438d1
title: Apertura de un archivo para lectura o escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254684538a64a37cd94841812df84808da8374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810766"
---
# <a name="opening-a-file-for-reading-or-writing"></a><span data-ttu-id="b9db2-103">Apertura de un archivo para lectura o escritura</span><span class="sxs-lookup"><span data-stu-id="b9db2-103">Opening a File for Reading or Writing</span></span>

<span data-ttu-id="b9db2-104">La función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) puede crear un archivo nuevo o abrir uno existente.</span><span class="sxs-lookup"><span data-stu-id="b9db2-104">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function can create a new file or open an existing file.</span></span> <span data-ttu-id="b9db2-105">Debe especificar el nombre de archivo, las instrucciones de creación y otros atributos.</span><span class="sxs-lookup"><span data-stu-id="b9db2-105">You must specify the file name, creation instructions, and other attributes.</span></span> <span data-ttu-id="b9db2-106">Cuando una aplicación crea un archivo nuevo, el sistema operativo lo agrega al directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="b9db2-106">When an application creates a new file, the operating system adds it to the specified directory.</span></span>

## <a name="example-open-a-file-for-writing"></a><span data-ttu-id="b9db2-107">Ejemplo: abrir un archivo para escribir en él</span><span class="sxs-lookup"><span data-stu-id="b9db2-107">Example: Open a File for Writing</span></span>

<span data-ttu-id="b9db2-108">En el ejemplo siguiente se usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para crear un nuevo archivo y abrirlo para escritura y [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) para escribir una cadena simple de forma sincrónica en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b9db2-108">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create a new file and open it for writing and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to write a simple string synchronously to the file.</span></span>

<span data-ttu-id="b9db2-109">Una llamada subsiguiente para abrir este archivo con [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) producirá un error hasta que se cierre el controlador.</span><span class="sxs-lookup"><span data-stu-id="b9db2-109">A subsequent call to open this file with [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) will fail until the handle is closed.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void DisplayError(LPTSTR lpszFunction);

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    char DataBuffer[] = "This is some test data to write to the file.";
    DWORD dwBytesToWrite = (DWORD)strlen(DataBuffer);
    DWORD dwBytesWritten = 0;
    BOOL bErrorFlag = FALSE;

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error:\tIncorrect number of arguments\n\n");
        _tprintf(TEXT("%s <file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // name of the write
                       GENERIC_WRITE,          // open for writing
                       0,                      // do not share
                       NULL,                   // default security
                       CREATE_NEW,             // create new file only
                       FILE_ATTRIBUTE_NORMAL,  // normal file
                       NULL);                  // no attr. template

    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: Unable to open file \"%s\" for write.\n"), argv[1]);
        return;
    }

    _tprintf(TEXT("Writing %d bytes to %s.\n"), dwBytesToWrite, argv[1]);

    bErrorFlag = WriteFile( 
                    hFile,           // open file handle
                    DataBuffer,      // start of data to write
                    dwBytesToWrite,  // number of bytes to write
                    &dwBytesWritten, // number of bytes that were written
                    NULL);            // no overlapped structure

    if (FALSE == bErrorFlag)
    {
        DisplayError(TEXT("WriteFile"));
        printf("Terminal failure: Unable to write to file.\n");
    }
    else
    {
        if (dwBytesWritten != dwBytesToWrite)
        {
            // This is an error because a synchronous write that results in
            // success (WriteFile returns TRUE) should write all data as
            // requested. This would not necessarily be the case for
            // asynchronous writes.
            printf("Error: dwBytesWritten != dwBytesToWrite\n");
        }
        else
        {
            _tprintf(TEXT("Wrote %d bytes to %s successfully.\n"), dwBytesWritten, argv[1]);
        }
    }

    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
```



## <a name="example-open-a-file-for-reading"></a><span data-ttu-id="b9db2-110">Ejemplo: abrir un archivo para leerlo</span><span class="sxs-lookup"><span data-stu-id="b9db2-110">Example: Open a File for Reading</span></span>

<span data-ttu-id="b9db2-111">En el ejemplo siguiente se usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un archivo existente para lectura y [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) para leer de forma sincrónica hasta 80 caracteres del archivo.</span><span class="sxs-lookup"><span data-stu-id="b9db2-111">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open an existing file for reading and [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) to read up to 80 characters synchronously from the file.</span></span>

<span data-ttu-id="b9db2-112">En este caso, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) solo se realiza correctamente si el archivo especificado ya existe en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="b9db2-112">In this case, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) succeeds only if the specified file already exists in the current directory.</span></span> <span data-ttu-id="b9db2-113">Una llamada subsiguiente para abrir este archivo con **CreateFile** se realizará correctamente si la llamada usa los mismos modos de acceso y uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b9db2-113">A subsequent call to open this file with **CreateFile** will succeed if the call uses the same access and sharing modes.</span></span>

<span data-ttu-id="b9db2-114">Sugerencia: puede usar el archivo que creó con el ejemplo WriteFile anterior para probar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b9db2-114">Tip: You can use the file you created with the previous WriteFile example to test this example.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFFERSIZE 5
DWORD g_BytesTransferred = 0;

void DisplayError(LPTSTR lpszFunction);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped
);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped )
 {
  _tprintf(TEXT("Error code:\t%x\n"), dwErrorCode);
  _tprintf(TEXT("Number of bytes:\t%x\n"), dwNumberOfBytesTransfered);
  g_BytesTransferred = dwNumberOfBytesTransfered;
 }

//
// Note: this simplified sample assumes the file to read is an ANSI text file
// only for the purposes of output to the screen. CreateFile and ReadFile
// do not use parameters to differentiate between text and binary file types.
//

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    DWORD  dwBytesRead = 0;
    char   ReadBuffer[BUFFERSIZE] = {0};
    OVERLAPPED ol = {0};

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error: Incorrect number of arguments\n\n");
        _tprintf(TEXT("Usage:\n\t%s <text_file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED, // normal file
                       NULL);                 // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: unable to open file \"%s\" for read.\n"), argv[1]);
        return; 
    }

    // Read one character less than the buffer size to save room for
    // the terminating NULL character. 

    if( FALSE == ReadFileEx(hFile, ReadBuffer, BUFFERSIZE-1, &ol, FileIOCompletionRoutine) )
    {
        DisplayError(TEXT("ReadFile"));
        printf("Terminal failure: Unable to read from file.\n GetLastError=%08x\n", GetLastError());
        CloseHandle(hFile);
        return;
    }
    SleepEx(5000, TRUE);
    dwBytesRead = g_BytesTransferred;
    // This is the section of code that assumes the file is ANSI text. 
    // Modify this block for other data types if needed.

    if (dwBytesRead > 0 && dwBytesRead <= BUFFERSIZE-1)
    {
        ReadBuffer[dwBytesRead]='\0'; // NULL character

        _tprintf(TEXT("Data read from %s (%d bytes): \n"), argv[1], dwBytesRead);
        printf("%s\n", ReadBuffer);
    }
    else if (dwBytesRead == 0)
    {
        _tprintf(TEXT("No data read from file %s\n"), argv[1]);
    }
    else
    {
        printf("\n ** Unexpected value for dwBytesRead ** \n");
    }

    // It is always good practice to close the open file handles even though
    // the app will exit here and clean up open handles anyway.
    
    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



## <a name="related-topics"></a><span data-ttu-id="b9db2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9db2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9db2-116">Crear y abrir archivos</span><span class="sxs-lookup"><span data-stu-id="b9db2-116">Creating and Opening Files</span></span>](creating-and-opening-files.md)
</dt> </dl>

 

 



