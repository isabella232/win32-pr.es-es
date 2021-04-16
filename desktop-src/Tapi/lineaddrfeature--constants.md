---
description: En las \_ constantes LINEADDRFEATURE se enumeran las operaciones que se pueden invocar en una dirección.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes de LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680228"
---
# <a name="lineaddrfeature_-constants"></a>Constantes de LINEADDRFEATURE \_

En las constantes **LINEADDRFEATURE \_** se enumeran las operaciones que se pueden invocar en una dirección.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ adelante**
</dt> <dd> <dl> <dt>



La dirección se puede reenviar.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Se puede colocar una llamada saliente en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**recogida de LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



Se puede seleccionar una llamada en la dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en una dirección específica.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en el grupo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**
</dt> <dd> <dl> <dt>



La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una dirección de destino **nula** ) se puede usar para recoger una llamada que se mantiene en la dirección. Normalmente, solo se usa en una organización exclusiva con puente.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una dirección de destino **nula** ) se puede usar para recopilar una llamada de llamada en espera. Tenga en cuenta que esto no indica necesariamente que una llamada en espera esté realmente presente, porque a menudo es imposible que un dispositivo de telefonía detecte automáticamente dicha llamada. sin embargo, indica que se invocará la función de enlace-Flash para intentar cambiar a dicha llamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Se puede establecer el control multimedia en esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Se pueden establecer los modos de terminal para esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



En esta dirección se puede configurar una llamada de conferencia con una llamada inicial **null** .


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



Las solicitudes de finalización de llamada se pueden cancelar en esta dirección.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**Desactivación \_ de LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



Las llamadas se pueden desactivar con esta dirección.

> [!Note]  
> Si no se establece ninguno de los nuevos bits de "recogida" modificados en el miembro **dwAddressFeatures** de [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) \_ , pero se establece el bit de recogida LINEADDRFEATURE, puede que cualquiera de los modos de recogida funcione; el proveedor de servicios simplemente no especificó ninguno.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica no molestar en la dirección. \_También se establecerá LINEADDRFEATURE forward.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar las llamadas en la dirección a otros números. \_También se establecerá LINEADDRFEATURE forward.

> [!Note]  
> Si ninguno de los nuevos bits modificados "FORWARD" se establece en el miembro **dwAddressFeatures** de [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , pero \_ se establece el bit de avance LINEADDRFEATURE, puede que cualquiera de los modos de avance funcione; el proveedor de servicios simplemente no especificó ninguno de ellos.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Esta constante se usa en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (devuelta por [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) y en [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (devuelta por [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **LINEADDRESSCAPS** informa de la disponibilidad de las características de dirección por parte del proveedor de servicios (principalmente, el modificador) para una dirección determinada. Una aplicación realizaría esta determinación cuando se inicializa. La estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) notifica, para una dirección determinada, en la que se pueden invocar realmente características mientras la dirección está en el estado actual. Una aplicación realizaría esta determinación de forma dinámica después de los cambios de estado de dirección, normalmente causado por actividades relacionadas con llamadas en la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 




