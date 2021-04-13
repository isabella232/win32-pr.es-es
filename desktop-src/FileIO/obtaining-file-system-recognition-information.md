---
description: El reconocimiento del sistema de archivos es la capacidad de reconocer los medios de almacenamiento que contienen un diseño válido del sistema de archivos o volumen que aún no se ha definido, pero el medio puede identificarse a sí mismo a través de la presencia de la estructura de reconocimiento definida internamente por Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Obtención de información de reconocimiento del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360457"
---
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="9aff8-103">Obtención de información de reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="9aff8-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="9aff8-104">El [reconocimiento del sistema de archivos](file-system-recognition.md) es la capacidad de reconocer los medios de almacenamiento que contienen un diseño válido del sistema de archivos o volumen que aún no se ha definido, pero el medio puede identificarse a sí mismo a través de la presencia de la estructura de reconocimiento definida internamente por Windows.</span><span class="sxs-lookup"><span data-stu-id="9aff8-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="9aff8-105">Dado que ningún sistema de archivos existente reconocerá un nuevo diseño de disco, el sistema de archivos "sin formato" montará el volumen y proporcionará acceso de nivel de bloque directo.</span><span class="sxs-lookup"><span data-stu-id="9aff8-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="9aff8-106">El sistema de archivos "sin formato", incorporado en *NtosKrnl*, tendrá la capacidad de leer la estructura de reconocimiento del sistema de archivos y proporcionar acceso a las aplicaciones a estas estructuras a través de la solicitud de control del sistema de archivos [**\_ \_ \_ \_ reconocimiento del sistema de archivos de consulta FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), que se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9aff8-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9aff8-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9aff8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aff8-108">Reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="9aff8-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="9aff8-109">**\_estructura de \_ reconocimiento del sistema de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="9aff8-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="9aff8-110">**\_ \_ \_ reconocimiento del sistema de archivos de consulta FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="9aff8-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
