---
description: Cancela una operación de espera registrada emitida por la función RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Función UnregisterWaitEx (Threadpoollegacyapiset. h)
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
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910022"
---
# <a name="unregisterwaitex-function"></a>UnregisterWaitEx función)

Cancela una operación de espera registrada emitida por la función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*WaitHandle* \[ de\]
</dt> <dd>

Identificador de espera. Este identificador es devuelto por la función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

</dd> <dt>

*CompletionEvent* \[ en, opcional\]
</dt> <dd>

Identificador del objeto de evento que se va a señalar cuando se haya anulado el registro de la operación de espera. Este parámetro puede ser **NULL**.

Si este parámetro es **un \_ \_ valor de identificador no válido**, la función espera a que todas las funciones de devolución de llamada se completen antes de devolver.

Si este parámetro es **null**, la función marca el temporizador para su eliminación y vuelve inmediatamente. Sin embargo, la mayoría de los llamadores deben esperar a que se complete la función de devolución de llamada para que puedan realizar cualquier limpieza necesaria.

Si el autor de la llamada proporciona este evento y la función se ejecuta correctamente, o si se produce un error en la función de **\_ e/s \_ pendiente**, no cierre el evento hasta que se señale.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

No se puede hacer una llamada de bloqueo a **UnregisterWaitEx** desde una función de devolución de llamada para la misma operación de espera. De lo contrario, la devolución de llamada estará esperando a que finalice. En general, una llamada de bloqueo a **UnregisterWaitEx** crea una dependencia entre el subproceso actual y la devolución de llamada, por lo que para realizar una llamada de bloqueo de anulación de registro en otra operación de espera, debe asegurarse de que las funciones de devolución de llamada no dependen entre sí y que la segunda operación de espera no realiza también una llamada de anulación de registro en la primera operación.

Tenga cuidado al realizar una llamada de bloqueo de **UnregisterWaitEx** en un subproceso persistente. Si la operación de espera que se va a eliminar del registro se creó con **WT \_ EXECUTEINPERSISTENTTHREAD**, puede producirse un interbloqueo.

Después de realizar una llamada de no bloqueo a **UnregisterWaitEx**, no se pueden poner en cola las nuevas funciones de devolución de llamada asociadas a *WaitHandle* . Sin embargo, puede haber funciones de devolución de llamada pendientes que ya estén en la cola de subprocesos de trabajo.

En algunas condiciones, la función generará un **error de \_ e/s \_ pendiente** si *CompletionEvent* es **null**. Esto indica que hay funciones de devolución de llamada pendientes. Esas devoluciones de llamada se ejecutarán o estarán en medio de la ejecución.

Si *CompletionEvent* es un identificador de un evento proporcionado por el autor de la llamada, es posible que la función se ejecute correctamente, se produzca un **error de \_ e/s \_ pendiente** o se produzca un error con un código de error diferente. Si la función se ejecuta correctamente, o si se produce un error en la función de **\_ e/s \_ pendiente**, el llamador siempre debe esperar hasta que se señale el evento para cerrar el evento. Si se produce un error en la función con un código de error diferente, no es necesario esperar hasta que se señale el evento para cerrar el evento.

**Windows XP:** Si *CompletionEvent* es un identificador de un evento proporcionado por el autor de la llamada y se produce un error en la función de **\_ e/s \_ pendiente**, el llamador debe esperar hasta que se señale el evento para cerrar el evento. Este comportamiento ha cambiado a partir de Windows Vista.

Para compilar una aplicación que usa esta función, defina **\_ Win32 \_ WinNT** como 0x0500 o posterior. Para obtener más información, consulte [uso de los encabezados de Windows](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Threadpoollegacyapiset. h en Windows 8 y Windows Server 2012 (incluido Windows. h); </dt> <dt>Winbase. h en Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP y Windows server 2003 (incluido Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Funciones de sincronización](synchronization-functions.md)
</dt> <dt>

[Agrupación de subprocesos](../procthread/thread-pooling.md)
</dt> </dl>

 

 
