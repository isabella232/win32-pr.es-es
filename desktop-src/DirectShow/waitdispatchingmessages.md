---
description: La función WaitDispatchingMessages espera a que se señalice un objeto, mientras se envían mensajes de ventana.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Función WaitDispatchingMessages (Wxutil. h)
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
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690249"
---
# <a name="waitdispatchingmessages-function"></a>WaitDispatchingMessages función)

La `WaitDispatchingMessages` función espera a que se señale un objeto mientras se envían mensajes de ventana.

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

Identificador del objeto que se va a esperar.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervalo de tiempo de espera, en milisegundos.

</dd> <dt>

*identificador* 
</dt> <dd>

Identificador opcional de una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Mensaje de ventana opcional que especifica un mensaje para enviar.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador opcional de un evento que se va a esperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la función **WaitForMultipleObjects** .

## <a name="remarks"></a>Observaciones

Si un objeto posee una ventana, debe enviar los mensajes de ventana mientras se espera. Esta función permite al objeto esperar a un evento, semáforo u otro objeto de exclusión mutua durante el envío de mensajes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




