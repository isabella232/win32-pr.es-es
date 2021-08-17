---
description: Cancela una operación de espera registrada emitida por la función RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Función UnregisterWaitEx (Threadpoollegacyapiset.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 4181aa43cb0c2844f99b7ad81b448271366eb2925740c25d400f891389efb129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765539"
---
# <a name="unregisterwaitex-function"></a>Función UnregisterWaitEx

Cancela una operación de espera registrada emitida por [**la función RegisterWaitForSingleObject.**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WaitHandle* \[ En\]
</dt> <dd>

Identificador de espera. La función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) devuelve este identificador.

</dd> <dt>

*CompletionEvent* \[ en, opcional\]
</dt> <dd>

Identificador del objeto de evento que se va a señalar cuando se ha anulado el registro de la operación de espera. Este parámetro puede ser **NULL**.

Si este parámetro es **INVALID \_ HANDLE \_ VALUE**, la función espera a que se completen todas las funciones de devolución de llamada antes de volver.

Si este parámetro es **NULL,** la función marca el temporizador para su eliminación y devuelve inmediatamente. Sin embargo, la mayoría de los llamadores deben esperar a que se complete la función de devolución de llamada para poder realizar cualquier limpieza necesaria.

Si el autor de la llamada proporciona este evento y la función se realiza correctamente o se produce un error en la función **con ERROR \_ IO \_ PENDING**, no cierre el evento hasta que se señale.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

No se puede realizar una llamada de bloqueo **a UnregisterWaitEx** desde dentro de una función de devolución de llamada para la misma operación de espera. De lo contrario, la devolución de llamada estará esperando a que finalice. En general, una llamada de bloqueo a **UnregisterWaitEx** crea una dependencia entre el subproceso actual y la devolución de llamada, por lo que para realizar una llamada de bloqueo de anulación del registro en otra operación de espera, debe asegurarse de que las funciones de devolución de llamada no dependen entre sí y de que la segunda operación de espera no realiza también una llamada de bloqueo anulación del registro en la primera operación.

Tenga cuidado al realizar una llamada **unregisterWaitEx** de bloqueo en un subproceso persistente. Si la operación de espera que se anula del registro se creó **con WT \_ EXECUTEINPERSISTENTTHREAD,** puede producirse un interbloqueo.

Después de realizar una llamada sin bloqueo **a UnregisterWaitEx,** no se puede poner en cola ninguna función de devolución de llamada nueva asociada a *WaitHandle.* Sin embargo, puede haber funciones de devolución de llamada pendientes ya en cola en subprocesos de trabajo.

En algunas condiciones, la función producirá un **error con ERROR IO \_ \_ PENDING** si *CompletionEvent* es **NULL.** Esto indica que hay funciones de devolución de llamada pendientes. Esas devoluciones de llamada se ejecutarán o se encuentran en medio de la ejecución.

Si *CompletionEvent* es un identificador de un evento proporcionado por el autor de la llamada, es posible que la función se complete correctamente, con **error \_ E/S \_ PENDIENTE** o con un código de error diferente. Si la función se realiza correctamente, o si se produce un error en la función con **ERROR \_ E/S \_ PENDIENTE,** el autor de la llamada siempre debe esperar hasta que se señale al evento para cerrar el evento. Si se produce un error en la función con un código de error diferente, no es necesario esperar hasta que se señale al evento para cerrar el evento.

**Windows XP:** Si *CompletionEvent es* un identificador de un evento proporcionado por el autor de la llamada y se produce un error en la función **con ERROR IO \_ \_ PENDING**, el autor de la llamada debe esperar hasta que se señale al evento para cerrar el evento. Este comportamiento cambió a partir de Windows Vista.

Para compilar una aplicación que use esta función, defina **\_ \_ WINNT win32** como 0x0500 o posterior. Para obtener más información, [vea Using the Windows Headers](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                                                                                                           |
| Header<br/>                   | <dl> <dt>Threadpoollegacyapiset.h en Windows 8 y Windows Server 2012 (incluya Windows.h);</dt> <dt>WinBase.h en Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP y Windows Server 2003 (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Funciones de sincronización](synchronization-functions.md)
</dt> <dt>

[Agrupación de subprocesos](../procthread/thread-pooling.md)
</dt> </dl>

 

 
