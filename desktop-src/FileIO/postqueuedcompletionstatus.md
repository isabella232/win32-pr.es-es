---
description: Envía un paquete de finalización de E/S a un puerto de finalización de E/S.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Función PostQueuedCompletionStatus (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: e56bad8b9de85f22836f9446b67340d22e71fe83552da6796e7864d3baddae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683365"
---
# <a name="postqueuedcompletionstatus-function"></a>Función PostQueuedCompletionStatus

Envía un paquete de finalización de E/S a un puerto de finalización de E/S.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CompletionPort* \[ En\]
</dt> <dd>

Identificador de un puerto de finalización de E/S en el que se va a publicar el paquete de finalización de E/S.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ En\]
</dt> <dd>

Valor que se va a devolver a través del *parámetro lpNumberOfBytesTransferred* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*dwCompletionKey* \[ En\]
</dt> <dd>

Valor que se va a devolver a través *del parámetro lpCompletionKey* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ en, opcional\]
</dt> <dd>

Valor que se va a devolver a través *del parámetro lpOverlapped* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentarios

El paquete de finalización de E/S cumplirá una llamada pendiente a la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Esta función devuelve con los tres valores pasados como segundo, tercero y cuarto parámetros de la llamada a **PostQueuedCompletionStatus**. El sistema no usa ni valida estos valores. En concreto, el *parámetro lpOverlapped* no necesita apuntar a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo Bloque de mensajes del servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster file system (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

CsvFs realizará la E/S redirigida para los archivos comprimidos.

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

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**Comprometidos**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

