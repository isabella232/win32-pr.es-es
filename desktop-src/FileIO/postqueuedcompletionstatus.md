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
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069870"
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

Valor que se va a devolver a *través del parámetro lpNumberOfBytesTransferred* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*dwCompletionKey* \[ En\]
</dt> <dd>

Valor que se va a devolver a través *del parámetro lpCompletionKey* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ in, opcional\]
</dt> <dd>

Valor que se va a devolver a *través del parámetro lpOverlapped* de la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

El paquete de finalización de E/S cumplirá una llamada pendiente a la [**función GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Esta función devuelve con los tres valores pasados como segundo, tercero y cuarto parámetros de la llamada a **PostQueuedCompletionStatus**. El sistema no usa ni valida estos valores. En concreto, el *parámetro lpOverlapped* no necesita apuntar a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes de servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster de archivos (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

CsvFs realizará E/S redirigida para archivos comprimidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones \[ de escritorio XP para aplicaciones para \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2003 \[ \| aplicaciones para UWP\]<br/>                                                                                                                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP (incluye Windows.h)</dt> </dl> |
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

[**COMPROMETIDOS**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

