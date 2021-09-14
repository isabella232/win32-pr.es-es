---
description: Las constantes de marca de bits LINEADDRESSSTATE \_ describen varios elementos de estado de dirección.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: LINEADDRESSSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249993"
---
# <a name="lineaddressstate_-constants"></a>Constantes \_ LINEADDRESSSTATE

Las constantes de marca de bits **LINEADDRESSSTATE \_** describen varios elementos de estado de dirección.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) de la dirección han cambiado. La aplicación debe usar [**lineGetAddressCaps para**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**\_ LINE ADDRESSSTATE**](line-addressstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocien una versión de API anterior recibirán mensajes [**\_ LINEDEVSTATE**](line-linedevstate.md) que especifican LINEDEVSTATE REINIT, lo que les obliga a cerrar y reinicializar su conexión a TAPI para obtener la información \_ actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



El elemento específico del dispositivo del estado de la dirección ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ FORWARD**
</dt> <dd> <dl> <dt>



El estado de reenvío de la dirección ha cambiado, incluido posiblemente el número de anillos para determinar una condición de no respuesta. La aplicación debe comprobar el estado de la dirección para determinar los detalles sobre el estado de reenvío actual de la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



La dirección supervisada o puente ha pasado de estar en uso por una estación a estar en uso por más de una estación.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



La dirección ha cambiado de inactiva o en uso por muchas estaciones de puente a estar en uso por una sola estación.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



La dirección ha cambiado a inactiva (no está en uso en ninguna estación).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



El número de llamadas en la dirección ha cambiado. Este es el resultado de eventos como una nueva llamada entrante, una llamada saliente en la dirección o una llamada que cambia su estado de retención. Esta marca cubre los cambios en cualquiera de los miembros **dwNumActiveCalls,** **dwNumOnHoldCalls** y **dwNumOnHoldPendingCalls** en la [**estructura LINEADDRESSSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) La aplicación debe comprobar los tres miembros cuando recibe un mensaje [**LINE \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Los elementos de estado de dirección distintos de los que se enumeran a continuación han cambiado. La aplicación debe comprobar el estado de la dirección actual para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**TERMINALES LINEADDRESSSTATE \_**
</dt> <dd> <dl> <dt>



La configuración del terminal para la dirección ha cambiado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

Se notifica a una aplicación sobre los cambios en estos elementos de estado en el [**mensaje LINE \_ ADDRESSSTATE.**](line-addressstate.md) Las funcionalidades del dispositivo de la dirección indican qué cambios de estado de dirección se pueden indicar para esta dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




