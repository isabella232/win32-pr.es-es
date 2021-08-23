---
description: El código \_ de control DA GET \_ NFS \_ ATTRIBUTES consulta información adicional sobre un recurso compartido NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES código de control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: e3e2b974d58888c35c24e18f16e1e75da46a180bb8123e9745170e074cd448de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956114"
---
# <a name="da_get_nfs_attributes-control-code"></a>Código \_ de control DA GET \_ NFS \_ ATTRIBUTES

El código de control **\_ DA GET \_ NFS \_ ATTRIBUTES** consulta información adicional sobre un recurso compartido NFS.

Para realizar esta operación, llame a la [**función DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* \[ En\]
</dt> <dd>

Identificador de un archivo en el recurso compartido NFS. Para obtener este identificador, llame a la [**función CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ En\]
</dt> <dd>

Código de control de la operación. Use **DA \_ GET \_ NFS \_ ATTRIBUTES para** esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación; se establece en **NULL.**

</dd> <dt>

*nInBufferSize* \[ En\]
</dt> <dd>

No se usa con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Puntero al búfer de salida, que contiene una **estructura NFS \_ FILE \_ ATTRIBUTES.** Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*nOutBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR INSUFFICIENT \_ \_ BUFFER** y *lpBytesReturned* es cero.

Si *lpOverlapped* es **NULL,** *lpBytesReturned* no puede ser **NULL.** Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Después de una operación de este tipo, el valor *de lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **NULL,** *lpBytesReturned* puede ser **NULL.** Si este parámetro no es **NULL y** la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se completa la operación superpuesta. Para recuperar el número de bytes devueltos, llame [**a GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Si el *parámetro hDevice* está asociado a un puerto de finalización de E/S, puede recuperar el número de bytes devueltos llamando a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ En\]
</dt> <dd>

Puntero a una [**estructura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Si *hDevice se* abrió sin especificar **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* se omite.

Si *hDevice se* abrió con la marca **FILE FLAG \_ \_ OVERLAPPED,** la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contenga un identificador para un objeto de evento. De lo contrario, se produce un error en la función de maneras imprevisibles.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) se devuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no se devuelve hasta que se ha completado la operación o se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Este código de control no tiene ningún archivo de encabezado asociado. Debe definir el código de control y las estructuras de datos como se muestra a continuación.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

Los miembros de la estructura se pueden describir de la siguiente manera.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Valor opaco que se usa para tipos de archivo especiales, como archivos FIFO, especiales de caracteres y bloques especiales.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Valor opaco que se usa para tipos de archivo especiales, como archivos FIFO, especiales de caracteres y bloques especiales.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Segundos**
</dt> <dd>

Valor de 64 bits que representa los segundos desde el 1 de enero de 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Número de nanosegundos que se van a agregar al **miembro Seconds.**

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Eltipo**
</dt> <dd>

Tipo de archivo NFS del recurso compartido.



| Tipo de archivo NFS                                                                              | Descripción                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS \_ TYPE \_ REG<br/>    | Un archivo normal.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>DIR DE TIPO NFS \_ \_<br/>    | Un directorio.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>BLK DE TIPO NFS \_ \_<br/>    | Un archivo especial de bloque.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS \_ TYPE \_ CHR<br/>    | Un archivo especial de caracteres.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>LNK DE TIPO NFS \_ \_<br/>    | Vínculo simbólico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>SOCK DE TIPO NFS \_ \_<br/> | Socket Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>FIFO DE TIPO NFS \_ \_<br/> | Un archivo FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo**
</dt> <dd>

Modo de archivo.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Número de vínculos al recurso compartido.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**
</dt> <dd>

Identificador UNIX usuario (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**
</dt> <dd>

Identificador UNIX de grupo (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamaño**
</dt> <dd>

Tamaño del archivo, en bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Utilizado**
</dt> <dd>

Tamaño de archivo utilizado, en bytes. Esto es igual que el tamaño del archivo.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Identificador del dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Identificador del sistema de archivos.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**
</dt> <dd>

Identificador de archivo.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

Hora de último acceso.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

Hora de la última modificación.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

Hora del último cambio.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Estructura **NFS \_ FILE \_ ATTRIBUTES.**

> [!Note]  
> Para obtener descripciones más detalladas de los miembros de esta estructura, vea la estructura **de la nfs3** en la especificación del protocolo NFS versión 3 (como se define en [RFC 1813).](https://www.ietf.org/rfc/rfc1813.txt)

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**
</dt> <dd>

Especifica si la conexión en la que se creó el identificador con el recurso compartido NFS es a través del protocolo NFS versión 2 o NFS versión 3.



| Value                            | Descripción              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | Versión 2 de NFS<br/> |
| <span id="3"></span>3<br/> | Versión 3 de NFS<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>    |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>         |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
