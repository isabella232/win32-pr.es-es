---
description: Envía un paquete de finalización de e/s a un puerto de finalización de e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Función PostQueuedCompletionStatus (IoAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668273"
---
# <a name="postqueuedcompletionstatus-function"></a>PostQueuedCompletionStatus función)

Envía un paquete de finalización de e/s a un puerto de finalización de e/s.

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

*CompletionPort* \[ de\]
</dt> <dd>

Identificador de un puerto de finalización de e/s en el que se va a publicar el paquete de finalización de e/s.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ de\]
</dt> <dd>

Valor que se va a devolver mediante el parámetro *lpNumberOfBytesTransferred* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*dwCompletionKey* \[ de\]
</dt> <dd>

Valor que se va a devolver mediante el parámetro *lpCompletionKey* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ en, opcional\]
</dt> <dd>

Valor que se va a devolver mediante el parámetro *lpOverlapped* de la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Observaciones

El paquete de finalización de e/s satisfará una llamada pendiente a la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Esta función devuelve con los tres valores pasados como el segundo, tercer y cuarto parámetro de la llamada a **PostQueuedCompletionStatus**. El sistema no usa ni valida estos valores. En concreto, el parámetro *lpOverlapped* no debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Technology                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo bloque de mensajes del servidor (SMB) 3,0<br/>   | Sí<br/> |
| Conmutación por error transparente SMB 3,0 (TFO)<br/>        | Sí<br/> |
| SMB 3,0 con recursos compartidos de archivos de escalabilidad horizontal (por lo tanto)<br/>   | Sí<br/> |
| Sistema de archivos Volumen compartido de clúster (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

CsvFs realizará la e/s redirigida para archivos comprimidos.

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

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**SUPERPUESTA**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

