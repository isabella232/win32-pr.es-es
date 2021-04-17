---
description: Marca las operaciones de e/s sincrónicas pendientes que emite el subproceso especificado como cancelada.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Función CancelSynchronousIo (IoAPI. h)
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
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546699"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo función)

Marca las operaciones de e/s sincrónicas pendientes que emite el subproceso especificado como cancelada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hThread* \[ de\]
</dt> <dd>

Identificador del subproceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si se produce un error en la función, el valor devuelto es 0 (cero). Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Si esta función no encuentra una solicitud para cancelar, el valor devuelto es 0 (cero) y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **error \_ no \_ encontrado**.

## <a name="remarks"></a>Observaciones

El autor de la llamada debe tener el [subproceso \_ terminar](/windows/desktop/ProcThread/thread-security-and-access-rights) el acceso.

Si hay alguna operación de e/s pendiente en curso para el subproceso especificado, la función **CancelSynchronousIo** las marca para su cancelación. La mayoría de los tipos de operaciones se pueden cancelar inmediatamente; otras operaciones pueden continuar hasta su finalización antes de que se cancelen realmente y se notifique al llamador. La función **CancelSynchronousIo** no espera a que se completen todas las operaciones canceladas. Para obtener más información, vea [instrucciones de finalización/cancelación de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

La operación que se está cancelando se completa con uno de los tres Estados siguientes: debe comprobar el estado de finalización para determinar el estado de finalización. Los tres Estados son:

-   **La operación se completó con normalidad.** Esto puede ocurrir incluso si se canceló la operación, porque es posible que no se haya enviado la solicitud de cancelación en el tiempo para cancelar la operación.
-   **Operación cancelada.** La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la **operación de error \_ \_ anulada**.
-   **No se pudo realizar la operación debido a otro error.** La función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error pertinente.

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
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                                                                                                                                                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                                                                                                                                    |
| Encabezado<br/>                   | <dl> <dt>IoAPI. h (incluye Windows. h); </dt> <dt>Winbase. h en Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista (incluido Windows. h)</dt> </dl> |
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

[E/s sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

