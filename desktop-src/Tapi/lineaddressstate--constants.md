---
description: Las \_ constantes de marcador de bits LINEADDRESSSTATE describen varios elementos de estado de dirección.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes de LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690975"
---
# <a name="lineaddressstate_-constants"></a>Constantes de LINEADDRESSSTATE \_

Las constantes de marcador de bits **LINEADDRESSSTATE \_** describen varios elementos de estado de dirección.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para la dirección han cambiado. La aplicación debe usar [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) para leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de API recibirán los mensajes de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión a TAPI para obtener la información actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



El elemento específico del dispositivo del estado de la dirección ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ adelante**
</dt> <dd> <dl> <dt>



El estado de reenvío de la dirección ha cambiado, incluido posiblemente el número de anillos para determinar una condición de no respuesta. La aplicación debe comprobar el estado de la dirección para determinar los detalles sobre el estado de reenvío actual de la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



La dirección supervisada o con puentes ha cambiado para que una estación la esté usando más de una.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



La dirección ha cambiado de inactiva o en uso por muchas estaciones puente para que solo una estación la esté usando.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



La dirección ha cambiado a inactiva (no está en uso por ninguna estación).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



El número de llamadas en la dirección ha cambiado. Este es el resultado de eventos como una nueva llamada entrante, una llamada saliente en la dirección o una llamada que cambia su estado de suspensión. Esta marca cubre los cambios en cualquiera de los miembros **dwNumActiveCalls**, **dwNumOnHoldCalls** y **dwNumOnHoldPendingCalls** en la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) . La aplicación debe comprobar los tres miembros cuando recibe un mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ otro**
</dt> <dd> <dl> <dt>



Los elementos de estado de dirección distintos de los que se enumeran a continuación han cambiado. La aplicación debe comprobar el estado de la dirección actual para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminales LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



La configuración de terminal para la dirección ha cambiado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

A una aplicación se le notifican los cambios de estos elementos de estado en el mensaje [**line \_ ADDRESSSTATE**](line-addressstate.md) . Las funcionalidades de dispositivo de la dirección indican qué cambios de estado de dirección se pueden notificar para esta dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LÍNEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




