---
description: El código de control de los atributos de das \_ Get \_ NFS \_ consulta información adicional sobre un recurso compartido de NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Código de control de DA_GET_NFS_ATTRIBUTES
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
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538680"
---
# <a name="da_get_nfs_attributes-control-code"></a>DA \_ obtiene \_ el \_ código de control de atributos NFS

El código de control de los **atributos de das \_ Get \_ NFS \_** consulta información adicional sobre un recurso compartido de NFS.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


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

*hDevice* \[ de\]
</dt> <dd>

Identificador de un archivo en el recurso compartido NFS. Para obtener este identificador, llame a la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ de\]
</dt> <dd>

Código de control de la operación. Use **\_ \_ \_ los atributos de das Get NFS** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se utiliza con esta operación; se establece en **null**.

</dd> <dt>

*nInBufferSize* \[ de\]
</dt> <dd>

No se utiliza con esta operación; se establece en cero.

</dd> <dt>

*lpOutBuffer* \[ enuncia\]
</dt> <dd>

Un puntero al búfer de salida, que contiene una estructura de **\_ \_ atributos de archivo NFS** . Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*nOutBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y *lpBytesReturned* es cero.

Si *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**. Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*. Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**. Si este parámetro no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta. Para recuperar el número de bytes devueltos, llame a [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ de\]
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.

Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento. De lo contrario, se produce un error imprevisible en la función.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Este código de control no tiene ningún archivo de encabezado asociado. Debe definir el código de control y las estructuras de datos como se indica a continuación.

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

Un valor opaco que se usa para los tipos de archivo especiales, como archivos de bloque especial, especial de caracteres y FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Un valor opaco que se usa para los tipos de archivo especiales, como archivos de bloque especial, especial de caracteres y FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**S**
</dt> <dd>

Un valor de 64 bits que representa los segundos desde el 1 de enero de 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Número de nanosegundos que se van a agregar al miembro de **segundos** .

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

El tipo de archivo NFS del recurso compartido.



| Tipo de archivo NFS                                                                              | Descripción                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_registro de tipo NFS \_<br/>    | Un archivo normal.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir de tipo NFS \_<br/>    | Un directorio.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_tipo \_ BLK de NFS<br/>    | Un archivo de bloque especial.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo de NFS \_ \_ Chr<br/>    | Archivo especial de caracteres.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo de NFS \_ \_ lnk<br/>    | Vínculo simbólico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo de NFS \_ \_ sock<br/> | Un socket de Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo de NFS \_ \_ FIFO<br/> | Un archivo FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modo**
</dt> <dd>

Modo de archivo.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Número de vínculos al recurso compartido.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**
</dt> <dd>

El identificador de usuario (UID) de UNIX.

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**
</dt> <dd>

El identificador de grupo (GID) de UNIX.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Ajusta**
</dt> <dd>

Tamaño del archivo, en bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Usa**
</dt> <dd>

Tamaño de archivo utilizado, en bytes. Es el mismo que el tamaño del archivo.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Identificador del dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Identificador del sistema de archivos.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**ID**
</dt> <dd>

Identificador de archivo.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

Última hora de acceso.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

Hora de la última modificación.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

La hora del último cambio.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Estructura **de \_ \_ atributos de archivo NFS** .

> [!Note]  
> Para obtener descripciones más detalladas de los miembros de esta estructura, consulte la estructura **fattr3** en la especificación del protocolo NFS versión 3 (tal y como se define en [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión**
</dt> <dd>

Especifica si la conexión en la que se creó el identificador del recurso compartido de NFS es a través del protocolo NFS versión 2 o NFS versión 3.



| Value                            | Descripción              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | Versión 2 de NFS<br/> |
| <span id="3"></span>3<br/> | NFS versión 3<br/> |



 

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

 

 
