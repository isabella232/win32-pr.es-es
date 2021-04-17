---
description: Recupera los atributos del dispositivo de disco especificado.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: Código de control de IOCTL_DISK_GET_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 613c73c2fd82e76768b0fc692b63b0761938a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669687"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a>\_Código de \_ control de información de \_ clúster de obtención de disco ioctl \_

Recupera los atributos del dispositivo de disco especificado.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador del disco.

Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Código de control de la operación.

Use **ioctl \_ Disk \_ Get \_ cluster \_ info** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

No se usa con esta operación. Se establece en **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Tamaño del búfer de entrada, en bytes. Se establece en 0 (cero).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Un puntero a un búfer que recibe una estructura de datos de [**\_ \_ información del clúster de disco**](disk-cluster-info.md) .

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Tamaño del búfer de salida, en bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

No se usa con esta operación. Se establece en **null**.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si se abrió *hDevice* sin especificar la **marca de archivo \_ \_ superpuesta**, *lpOverlapped* se omite.

Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento. De lo contrario, se produce un error imprevisible en la función.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, lo que indica que todos los volúmenes del disco están listos para su uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Códigos de control de administración de discos](disk-management-control-codes.md)
</dt> <dt>

[**\_información del clúster de disco \_**](disk-cluster-info.md)
</dt> <dt>

[**\_ \_ \_ información del clúster de conjunto de discos ioctl \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

