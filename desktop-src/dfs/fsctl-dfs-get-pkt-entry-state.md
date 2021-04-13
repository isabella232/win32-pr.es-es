---
title: Código de control FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: El código de control de FSCTL_DFS_GET_PKT_ENTRY_STATE puede obtener la misma información que la función NetDfsGetClientInfo, pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539177"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>Código de control de FSCTL_DFS_GET_PKT_ENTRY_STATE

El código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** puede obtener la misma información que la función [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS. No se recomienda usar el código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** a menos que haya problemas de rendimiento.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* [in]
</dt> <dd>

Identificador del dispositivo. Para obtener un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

Código de control de la operación. Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** para esta operación.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Dirección de una estructura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) y las cadenas unicode 1-3 siguientes.

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta el parámetro *lpInBuffer* .

</dd> <dt>

*lpOutBuffer* [out]
</dt> <dd>

Dirección de una estructura de **DFS_INFO_ \#** y de las cadenas y estructuras a las que apunta la estructura de **DFS_INFO_ \#** . La estructura específica devuelta depende del miembro de **nivel** de la estructura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) pasada en el búfer de entrada.

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta el parámetro *lpOutBuffer* . Debido a las cadenas y estructuras a las que hace referencia la estructura de **DFS_INFO_ \#** devuelta que también están en el búfer de salida, este búfer debe ser mayor que la estructura de **DFS_INFO_ \#** especificada.

</dd> <dt>

*lpBytesReturned* [out]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos almacenados en el búfer de salida, en bytes.

Si el búfer de salida es demasiado pequeño, pero al menos lo suficientemente grande como para contener un **valor DWORD**, se produce un error en la llamada, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR_MORE_DATA**, y el primer **valor DWORD** del búfer de salida contiene el tamaño que se habría requerido. Si el búfer de salida no puede contener un **valor DWORD** , se produce un error en la llamada con **ERROR_INSUFFICIENT_BUFFER** y el valor de *lpBytesReturned* es cero.

Si *lpOverlapped* es **null**, *lpBytesReturned* no puede ser **null**. Incluso cuando una operación no devuelve datos de salida y *lpOutBuffer* es **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) hace uso de *lpBytesReturned*. Después de una operación de este tipo, el valor de *lpBytesReturned* no tiene sentido.

Si *lpOverlapped* no es **null**, *lpBytesReturned* puede ser **null**. Si este parámetro no es **null** y la operación devuelve datos, *lpBytesReturned* no tiene sentido hasta que se haya completado la operación superpuesta. Para recuperar el número de bytes devueltos, llame a [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Si el parámetro *hDevice* está asociado a un puerto de finalización de e/s, puede recuperar el número de bytes devueltos mediante una llamada a [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* [in]
</dt> <dd>

Puntero a una estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si se abrió *hDevice* sin especificar **FILE_FLAG_OVERLAPPED**, *lpOverlapped* se omite.

Si *hDevice* se abrió con la marca **FILE_FLAG_OVERLAPPED** , la operación se realiza como una operación superpuesta (asincrónica). En este caso, *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contiene un identificador para un objeto de evento. De lo contrario, se produce un error imprevisible en la función.

En el caso de las operaciones superpuestas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) vuelve inmediatamente y el objeto de evento se señala cuando se ha completado la operación. De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.

Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                       |
| Encabezado<br/>                   | <dl> <dt>LmDfs. h (incluye LmDfs. h)</dt> </dl> |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
