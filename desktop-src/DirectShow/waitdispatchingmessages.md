---
description: La función WaitDispatchingMessages espera a que se señale un objeto, mientras se envían mensajes de ventana.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Función WaitDispatchingMessages (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26442633d1a4d5187b5e53ae53e0a898f759f91dc3719f09715b570108b701f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071909"
---
# <a name="waitdispatchingmessages-function"></a>Función WaitDispatchingMessages

La `WaitDispatchingMessages` función espera a que se señale un objeto, mientras se envían mensajes de ventana.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hObject* 
</dt> <dd>

Identificador del objeto que se espera.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervalo de tiempo de espera, en milisegundos.

</dd> <dt>

*Hwnd* 
</dt> <dd>

Identificador opcional para una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Mensaje de ventana opcional, especificando un mensaje que se enviará.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador opcional para un evento que se debe esperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la **función WaitForMultipleObjects.**

## <a name="remarks"></a>Comentarios

Si un objeto posee una ventana, debe enviar mensajes de ventana mientras espera. Esta función permite que el objeto espere un evento, un semáforo u otro objeto de exclusión mutua al enviar mensajes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




