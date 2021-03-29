---
description: Se envía el mensaje APPNEWCALL de línea de TAPI \_ para informar a una aplicación cuando se ha creado un nuevo identificador de llamada espontáneamente en su nombre.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Mensaje de LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680775"
---
# <a name="line_appnewcall-message"></a>Mensaje de línea \_ APPNEWCALL

Se envía el mensaje **\_ APPNEWCALL de línea** de TAPI para informar a una aplicación cuando un nuevo identificador de llamada se ha creado espontáneamente en su nombre (excepto a través de una llamada de API de la aplicación, en cuyo caso el identificador se habría devuelto a través de un parámetro de puntero pasado a la función).


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea en el que se ha creado la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la dirección en la línea en la que aparece la llamada. Un identificador de dirección está asociado de forma permanente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Identificador de la aplicación para la nueva llamada.

</dd> <dt>

*dwParam3* 
</dt> <dd>

El privilegio Applications para la nueva llamada (LINECALLPRIVILEGE \_ Owner o LINECALLPRIVILEGE \_ monitor).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las aplicaciones que admiten la versión 2,0 o posterior de TAPI recibirán un mensaje de **línea \_ APPNEWCALL** cada vez que la aplicación reciba un identificador de una nueva llamada espontáneamente. Dado que el mensaje incluye los parámetros *hLine* y *dwAddressID* en los que existe la llamada, la aplicación puede crear fácilmente un nuevo objeto de llamada en el contexto correcto. El mensaje **line \_ APPNEWCALL** siempre va seguido inmediatamente de un mensaje [**line \_ CALLSTATE**](line-callstate.md) que indica el estado inicial de la llamada.

Las aplicaciones anteriores (que negociaron una versión de API anterior a 2,0) solo se envían a un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) , como se documenta en versiones anteriores de la API. Dichas aplicaciones crearían un nuevo objeto Call al recibir un mensaje [**line \_ CALLSTATE**](line-callstate.md) que tiene *dwParam3* establecido en un valor distinto de cero y que contiene un identificador de llamada que la aplicación no conoce actualmente. Las desventajas son que (a) la aplicación debe llamar a [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar los parámetros *hLine* y *dwAddressID* asociados con la llamada. (b) la aplicación debe examinar todos los identificadores de llamadas conocidos para determinar que la llamada es una llamada nueva. y (c) es posible, en determinadas condiciones, para que la aplicación piense que está recibiendo un nuevo identificador de llamada cuando en realidad ha desasignado su identificador a la llamada (por ejemplo, la aplicación ha desasignado simplemente un identificador de llamada, pero un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) que le asigna la propiedad de la aplicación de la llamada debido a un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) de otra aplicación ya estaba en la cola de mensajes TAPI de la aplicación)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




