---
description: Marca las operaciones de E/S sincrónicas pendientes emitidas por el subproceso especificado como canceladas.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Función CancelSynchronousIo (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582555"
---
# <a name="cancelsynchronousio-function"></a>Función CancelSynchronousIo

Marca las operaciones de E/S sincrónicas pendientes emitidas por el subproceso especificado como canceladas.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hThread* \[ En\]
</dt> <dd>

Identificador del subproceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la función, el valor devuelto es 0 (cero). Para obtener información de error extendida, llame a [**la función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR NOT \_ \_ FOUND**.

## <a name="remarks"></a>Comentarios

El autor de la llamada debe tener el [derecho de acceso THREAD \_ TERMINATE.](/windows/desktop/ProcThread/thread-security-and-access-rights)

Si hay alguna operación de E/S pendiente en curso para el subproceso especificado, la función **CancelSynchronousIo** las marca para la cancelación. La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; Otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al autor de la llamada. La **función CancelSynchronousIo** no espera a que se completen todas las operaciones canceladas. Para obtener más información, vea [Instrucciones de finalización y cancelación de E/S.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

La operación que se cancela se completa con uno de los tres estados; debe comprobar el estado de finalización para determinar el estado de finalización. Los tres estados son:

-   **La operación se completó con normalidad.** Esto puede ocurrir incluso si la operación se canceló, porque es posible que la solicitud de cancelación no se haya enviado a tiempo para cancelar la operación.
-   **Operación cancelada.** La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR OPERATION \_ \_ ABORTED.**
-   **Se produjo otro error en la operación.** La [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.

En Windows 8 y Windows Server 2012, esta función es compatible con las siguientes tecnologías.



| Tecnología                                           | Compatible      |
|------------------------------------------------------|----------------|
| Protocolo Bloque de mensajes del servidor (SMB) 3.0<br/>   | Sí<br/> |
| Conmutación por error transparente (TFO) de SMB 3.0<br/>        | Sí<br/> |
| SMB 3.0 con recursos compartidos de archivos de escalabilidad horizontal (SO)<br/>   | Sí<br/> |
| Volumen compartido de clúster file system (CsvFS)<br/> | Sí<br/> |
| Sistema de archivos resistente a errores (ReFS)<br/>              | Sí<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                                                                                                                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                                                                                                                                    |
| Header<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h en Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista (Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[Funciones de administración de archivos](file-management-functions.md)
</dt> <dt>

[E/S sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

