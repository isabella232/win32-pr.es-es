---
description: Las constantes LINEADDRFEATURE \_ enumera las operaciones que se pueden invocar en una dirección.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: LINEADDRFEATURE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249981"
---
# <a name="lineaddrfeature_-constants"></a>LineADDRFEATURE \_ (Constantes)

Las **constantes LINEADDRFEATURE \_** enumera las operaciones que se pueden invocar en una dirección.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ FORWARD**
</dt> <dd> <dl> <dt>



La dirección se puede reenviar.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Se puede colocar una llamada saliente en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**RECOGIDA LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



Se puede seleccionar una llamada en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



La [**función linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en una dirección específica.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



La [**función linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en el grupo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUP (RECOGIDA DE LINEADDRFEATURE)**
</dt> <dd> <dl> <dt>



La [**función linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una **dirección** de destino null) se puede usar para seleccionar una llamada que se mantiene en la dirección. Normalmente, esto solo se usa en una disposición exclusiva de puente.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



La [**función linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una **dirección** de destino null) se puede usar para seleccionar una llamada en espera de llamada. Tenga en cuenta que esto no indica necesariamente que una llamada en espera está realmente presente, ya que a menudo es imposible que un dispositivo de telefonía detecte automáticamente dicha llamada. sin embargo, indica que se invocará la función hook-flash para intentar cambiar a dicha llamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



El control multimedia se puede establecer en esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Se pueden establecer los modos de terminal de esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



En esta dirección se **puede** configurar una llamada de conferencia con una llamada inicial NULL.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



Las solicitudes de finalización de llamadas se pueden cancelar en esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNPARK**
</dt> <dd> <dl> <dt>



Las llamadas se pueden desesparparpar mediante esta dirección.

> [!Note]  
> Si no se establece ninguno de los nuevos bits "PICKUP" modificados en el miembro **dwAddressFeatures** en [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) pero el bit LINEADDRFEATURE PICKUP está establecido, puede que cualquiera de los modos de recogida funcione; el proveedor de servicios simplemente no ha especificado \_ cuáles.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La [**función lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica No interrumpir en la dirección. También se establecerá LINEADDRFEATURE \_ FORWARD.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La [**función lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar llamadas de la dirección a otros números. También se establecerá LINEADDRFEATURE \_ FORWARD.

> [!Note]  
> Si ninguno de los nuevos bits "FORWARD" modificados se establece en el miembro **dwAddressFeatures** en [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) pero el bit LINEADDRFEATURE FORWARD está establecido, puede que cualquiera de los modos de reenvío funcione; el proveedor de servicios simplemente no ha especificado \_ cuáles.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

Esta constante se usa tanto en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (devuelto por [**lineGetAddressCaps)**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)como en [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (devuelto por [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **LINEADDRESSCAPS informa** de la disponibilidad de las características de dirección por parte del proveedor de servicios (principalmente el modificador) para una dirección determinada. Una aplicación tomaría esta determinación cuando se inicializa. La [**estructura LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) notifica, para una dirección determinada, qué características de dirección se pueden invocar realmente mientras la dirección está en el estado actual. Una aplicación tomaría esta determinación dinámicamente después de los cambios de estado de dirección, normalmente causados por actividades relacionadas con llamadas en la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




