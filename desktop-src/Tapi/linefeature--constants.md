---
description: Las constantes LINEFEATURE \_ enumera las operaciones que se pueden invocar en una línea mediante esta API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: LINEFEATURE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1d65ea846ea8209850837877e1e880fc89fed0ad7e0d6209b38ff0f3703f34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073055"
---
# <a name="linefeature_-constants"></a>LineFEATURE \_ (Constantes)

Las **constantes LINEFEATURE \_ enumera** las operaciones que se pueden invocar en una línea mediante esta API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Las operaciones específicas del dispositivo se pueden usar en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**
</dt> <dd> <dl> <dt>



Las características específicas del dispositivo se pueden usar en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ FORWARD**
</dt> <dd> <dl> <dt>



El reenvío de todas las direcciones se puede usar en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La [**función lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica No interrumpir en todas las direcciones de la línea. También se establecerá LINEFEATURE \_ FORWARD. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La [**función lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar llamadas en todas las direcciones de la línea a otros números. También se establecerá LINEFEATURE \_ FORWARD. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Se puede colocar una llamada saliente en esta línea mediante una dirección no especificada.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**
</dt> <dd> <dl> <dt>



La [**función lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) se puede invocar en el dispositivo de línea. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



El control multimedia se puede establecer en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Se pueden establecer modos de terminal para esta línea.

> [!Note]  
> Si ninguno de los nuevos bits "FORWARD" modificados se establece en el miembro **dwLineFeatures** en [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) pero se establece el bit LINEFEATURE FORWARD, cualquiera de los modos de reenvío puede funcionar; el proveedor de servicios simplemente no ha especificado \_ cuáles.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Las constantes LINEFEATURE \_ se usan en [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (devuelto por [**lineGetLineDevStatus).**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) [**LINEDEVSTATUS notifica,**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) para una línea determinada, qué características de línea se pueden invocar realmente mientras la línea está en el estado actual. Una aplicación realizaría esta determinación dinámicamente después de los cambios de estado de línea, normalmente causados por actividades relacionadas con la dirección o la llamada en la línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




