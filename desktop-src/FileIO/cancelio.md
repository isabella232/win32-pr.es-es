---
description: Cancela todas las operaciones de entrada y salida (e/s) pendientes emitidas por el subproceso que realiza la llamada para el archivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Función CancelIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666966"
---
# <a name="cancelio-function"></a>CancelIo función)

Cancela todas las operaciones de entrada y salida (e/s) pendientes emitidas por el subproceso que realiza la llamada para el archivo especificado. La función no cancela las operaciones de e/s que otros subprocesos emiten para un identificador de archivo.

Para cancelar las operaciones de e/s de otro subproceso, utilice la función [**CancelIoEx**](cancelioex-func.md) .

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ de\]
</dt> <dd>

Identificador del archivo.

La función cancela todas las operaciones de e/s pendientes para este identificador de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero. La operación de cancelación para todas las operaciones de e/s pendientes emitidas por el subproceso que realiza la llamada para el identificador de archivo especificado se solicitó correctamente. El subproceso puede usar la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las operaciones de e/s.

Si se produce un error en la función, el valor devuelto es cero (0). Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

Si hay alguna operación de e/s pendiente en curso para el identificador de archivo especificado y la emite el subproceso que realiza la llamada, la función **CancelIo** las cancela. **CancelIo** cancela solo e/s pendientes en el identificador, no cambia el estado del identificador. Esto significa que no se puede confiar en el estado del identificador porque no se puede saber si la operación se completó correctamente o se canceló.

Las operaciones de e/s deben emitirse como e/s superpuestas. Si no es así, las operaciones de e/s no vuelven a permitir que el subproceso llame a la función **CancelIo** . La llamada a la función **CancelIo** con un identificador de archivo que no está abierto con la **marca de archivo \_ \_ superpuesto** no hace nada.

Todas las operaciones de e/s que se han cancelado se **han \_ anulado con la operación error \_ cancelada** y todas las notificaciones de finalización de las operaciones de e/s se producen con normalidad.

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Technology                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes del servidor (SMB) 3,0<br/>   | Sí<br/> |
| Conmutación por error transparente SMB 3,0 (TFO)<br/>        | Sí<br/> |
| SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)<br/>   | Sí<br/> |
| Sistema de archivos Volumen compartido de clúster (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows XP \|\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluido Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[E/s sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

