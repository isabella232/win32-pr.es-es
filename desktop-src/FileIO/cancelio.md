---
description: Cancela todas las operaciones de entrada y salida (E/S) pendientes emitidas por el subproceso de llamada para el archivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Función CancelIo (IoAPI.h)
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
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075345"
---
# <a name="cancelio-function"></a>Función CancelIo

Cancela todas las operaciones de entrada y salida (E/S) pendientes emitidas por el subproceso de llamada para el archivo especificado. La función no cancela las operaciones de E/S que otros subprocesos emiten para un identificador de archivo.

Para cancelar operaciones de E/S desde otro subproceso, use la [**función CancelIoEx.**](cancelioex-func.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFile* \[ En\]
</dt> <dd>

Identificador del archivo.

La función cancela todas las operaciones de E/S pendientes para este identificador de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero. Se solicitó correctamente la operación de cancelación para todas las operaciones de E/S pendientes emitidas por el subproceso de llamada para el identificador de archivo especificado. El subproceso puede usar la [**función GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar cuándo se han completado las propias operaciones de E/S.

Si se produce un error en la función, el valor devuelto es cero (0). Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Si hay alguna operación de E/S pendiente en curso para el identificador de archivo especificado y el subproceso que realiza la llamada las emite, la **función CancelIo** las cancela. **CancelIo** solo cancela la E/S pendiente en el identificador, no cambia el estado del identificador; Esto significa que no puede confiar en el estado del identificador porque no puede saber si la operación se completó correctamente o se canceló.

Las operaciones de E/S se deben emitir como E/S superpuestas. Si no lo están, las operaciones de E/S no vuelven para permitir que el subproceso llame a la **función CancelIo.** Llamar a **la función CancelIo** con un identificador de archivo que no se abre con **FILE FLAG \_ \_ OVERLAPPED** no hace nada.

Todas las operaciones de E/S canceladas se completan con el error **ERROR \_ OPERATION \_ ABORTED** y todas las notificaciones de finalización de las operaciones de E/S se producen normalmente.

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes de servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster file system (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP (Windows.h)</dt> </dl> |
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

[E/S sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

