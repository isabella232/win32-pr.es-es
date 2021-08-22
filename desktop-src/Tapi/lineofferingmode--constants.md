---
description: Las constantes de marca de bits LINEOFFERINGMODE \_ (versiones 1.4 y posteriores de TAPI) describen diferentes subestados de una llamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c2c36d18d006cdc1e2d9fc79095d58b6f56f1e58f4939c4e08ec6936af6855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518915"
---
# <a name="lineofferingmode_-constants"></a>LINEOFFERINGMODE \_ (Constantes)

Las constantes de marca de bits **LINEOFFERINGMODE \_** (versiones 1.4 y posteriores de TAPI) describen diferentes subestados de una llamada de oferta. Un modo está disponible como estado de llamada para la aplicación después de las trdansitions del estado de llamada a la oferta y dentro del mensaje [**LINE \_ CALLSTATE**](line-callstate.md) que indica que la llamada está en LINECALLSTATE \_ OFFERING. Estos valores se usan cuando la llamada se encuentra en una dirección que se comparte (une) con otras estaciones (consulte [**LINEADDRESSSHARING \_ Constants**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ACTIVE**
</dt> <dd> <dl> <dt>



Indica que la llamada está generando alertas en la estación actual (va a ir acompañada de mensajes LINEDEVSTATE RINGING) y, si alguna aplicación está configurada para responder automáticamente, puede \_ hacerlo. Si el modo de estado de llamada es CERO, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente). (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INACTIVE**
</dt> <dd> <dl> <dt>



Indica que la llamada se ofrece en más de una estación, pero la estación actual no está alertando (por ejemplo, puede ser una estación de asistencia en la que el estado de la oferta sea de aviso, como parpadear una luz); El software de la estación establecido para la respuesta automática no debe responder preferiblemente a la llamada, ya que debe ser la prerrogativa en la estación principal (alerta), pero se puede usar [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) para conectar la llamada. (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

No extensible. Los 32 bits están reservados.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión negociada de la API en la línea y no usar estos valores LINEOFFERINGMODE si no se admiten en la versión \_ negociada. Las aplicaciones que no son conscientes de LINEOFFERINGMODE probablemente asumirán que una llamada que se encuentra en LINECALLSTATE OFFERING está en \_ \_ LINEOFFERINGMODE \_ ACTIVE.

Los valores LINEOFFERINGMODE ACTIVE y LINEOFFERINGMODE INACTIVE se usan cuando la llamada se encuentra en una dirección que se comparte con otras estaciones \_ \_ (puente; vea [LINEADDRESSSHARING \_ Constants](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas. Si el modo de estado de llamada de la oferta es "activo", significa que la llamada está generando alertas en la estación actual (va a ir acompañada de mensajes LINEDEVSTATE RINGING) y, si alguna aplicación está configurada para responder automáticamente, puede \_ hacerlo. Si el modo de estado de llamada es "inactivo", la llamada se ofrece en más de una estación, pero la estación actual no está alertando (por ejemplo, puede ser una estación de servicio con aviso del estado de la oferta, como parpadear una luz); El software de la estación establecido para la respuesta automática no debe responder preferiblemente a la llamada, ya que debe ser la prerrogativa en la estación principal (alerta), pero [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) se puede usar para conectar la llamada. Si el modo de estado de llamada es CERO, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




