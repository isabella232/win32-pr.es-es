---
description: El mensaje TAPI LINE APPNEWCALL se envía para informar a una aplicación cuando se ha creado un nuevo identificador de llamada \_ en su nombre.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: LINE_APPNEWCALL mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250227"
---
# <a name="line_appnewcall-message"></a>LINE \_ APPNEWCALL message

El mensaje TAPI **LINE \_ APPNEWCALL** se envía para informar a una aplicación cuando se ha creado un nuevo identificador de llamada en su nombre (distinto de a través de una llamada API desde la aplicación, en cuyo caso el identificador se habría devuelto a través de un parámetro de puntero pasado a la función).


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

El identificador de la aplicación al dispositivo de línea en el que se ha creado la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la dirección en la línea en la que aparece la llamada. Un identificador de dirección está asociado permanentemente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Identificador de la aplicación para la nueva llamada.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Privilegio de las aplicaciones para la nueva llamada (LINECALLPRIVILEGE \_ OWNER o LINECALLPRIVILEGE \_ MONITOR).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las aplicaciones que admiten TAPI versión 2.0 o posterior se envían un mensaje **LINE \_ APPNEWCALL** cada vez que se le da a la aplicación un identificador para una nueva llamada. Dado que el mensaje incluye los *parámetros hLine* y *dwAddressID* en los que existe la llamada, la aplicación puede crear fácilmente un nuevo objeto de llamada en el contexto correcto. El **mensaje \_ LINE APPNEWCALL** siempre va seguido inmediatamente de un [**mensaje LINE \_ CALLSTATE**](line-callstate.md) que indica el estado inicial de la llamada.

Las aplicaciones anteriores (que negociaron una versión de API anterior a la 2.0) solo se envían un mensaje [**LINE \_ CALLSTATE,**](line-callstate.md) como se documenta en versiones anteriores de la API. Estas aplicaciones crearían un nuevo objeto de llamada al recibir un mensaje [**LINE \_ CALLSTATE**](line-callstate.md) que tiene *dwParam3* establecido en un valor distinto de cero y que contiene un identificador de llamada no conocido actualmente por la aplicación. Las desventajas son que (a) la aplicación debe llamar a [**lineGetCallInfo para**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) determinar los parámetros *hLine* y *dwAddressID* asociados a la llamada; (b) la aplicación debe examinar todos los identificadores de llamadas conocidos para determinar que la llamada es una nueva llamada; y (c) es posible, en determinadas condiciones, que la aplicación piense que recibe un nuevo identificador de llamada cuando en realidad acaba de desasignar su identificador a la llamada (por ejemplo, la aplicación acaba de desasignar un identificador de llamada, pero un mensaje [**LINE \_ CALLSTATE**](line-callstate.md) que da a la aplicación la propiedad de la llamada debido a que una [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) de otra aplicación ya estaba en la cola de mensajes TAPI de la aplicación).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




