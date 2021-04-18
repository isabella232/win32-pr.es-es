---
description: En las \_ constantes LINEFEATURE se enumeran las operaciones que se pueden invocar en una línea mediante esta API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes de LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681216"
---
# <a name="linefeature_-constants"></a>Constantes de LINEFEATURE \_

En **las \_ constantes LINEFEATURE** se enumeran las operaciones que se pueden invocar en una línea mediante esta API.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Las operaciones específicas del dispositivo se pueden usar en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**
</dt> <dd> <dl> <dt>



Las características específicas del dispositivo se pueden usar en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ adelante**
</dt> <dd> <dl> <dt>



Se puede usar el reenvío de todas las direcciones en la línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica no molestar en todas las direcciones de la línea. \_También se establecerá LINEFEATURE forward. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar llamadas en todas las direcciones de la línea a otros números. \_También se establecerá LINEFEATURE forward. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Se puede colocar una llamada saliente en esta línea mediante una dirección no especificada.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**
</dt> <dd> <dl> <dt>



La función [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) se puede invocar en el dispositivo de línea. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Se puede establecer el control multimedia en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Se pueden establecer los modos de terminal para esta línea.

> [!Note]  
> Si ninguno de los nuevos bits modificados "FORWARD" se ha establecido en el miembro **dwLineFeatures** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) \_ , pero se establece el bit de avance LINEFEATURE, cualquiera de los modos de avance puede funcionar; el proveedor de servicios simplemente no especificó ninguno de ellos.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Las \_ constantes LINEFEATURE se usan en [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (devuelta por [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)). [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) notifica, para una línea determinada, qué características de línea se pueden invocar realmente mientras la línea está en el estado actual. Una aplicación realizaría esta determinación dinámicamente después de que cambie el estado de línea, normalmente causado por las actividades relacionadas con la dirección o la llamada en la línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



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

 

 




