---
description: Las \_ constantes de marca de bits LINEOFFERINGMODE (versiones de TAPI 1,4 y posteriores) describen los distintos subestados de una llamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes de LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690754"
---
# <a name="lineofferingmode_-constants"></a>Constantes de LINEOFFERINGMODE \_

Las constantes de marca de bits **LINEOFFERINGMODE \_** (versiones de TAPI 1,4 y posteriores) describen los distintos subestados de una llamada de oferta. Un modo está disponible como estado de la llamada a la aplicación después del estado de la llamada trdansitions a la oferta y dentro del mensaje de la [**línea \_ CALLSTATE**](line-callstate.md) que indica que la llamada está en la \_ oferta LINECALLSTATE. Estos valores se usan cuando la llamada se realiza en una dirección compartida (puente) con otras estaciones (consulte [**LINEADDRESSSHARING \_ constantes**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ activo**
</dt> <dd> <dl> <dt>



Indica que la llamada se notifica en la estación actual (irá acompañada de mensajes LINEDEVSTATE \_ Ringing) y, si alguna aplicación está configurada para responder automáticamente, puede hacerlo. Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente). (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INactivo**
</dt> <dd> <dl> <dt>



Indica que la llamada se está ofreciendo en más de una estación, pero la estación actual no es de alerta (por ejemplo, puede ser una estación de operador en la que el estado de la oferta es consultivo, como parpadear una luz). el software del conjunto de estaciones para la respuesta automática no debe responder a la llamada, ya que debe ser prerrogativa en la estación principal (de alertas), pero [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) se puede usar para conectar la llamada. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

No extensible. Todos los 32 bits están reservados.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no utilizar estos \_ valores de LINEOFFERINGMODE si no se admiten en la versión negociada. Las aplicaciones que no son Cognizant de LINEOFFERINGMODE \_ probablemente suponen que una llamada que está en la \_ oferta LINECALLSTATE está \_ activa en LINEOFFERINGMODE.

Los \_ valores INactivos de LINEOFFERINGMODE activo y LINEOFFERINGMODE \_ se usan cuando la llamada está en una dirección que se comparte con otras estaciones (puente; [vea \_ constantes de LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas. Si el modo de estado de la llamada de la oferta es "activo", significa que la llamada se notifica en la estación actual (irá acompañada de \_ los mensajes LINEDEVSTATE Ringing) y, si alguna aplicación está configurada para responder automáticamente, puede hacerlo. Si el modo de estado de la llamada es "inactivo", la llamada se ofrece en más de una estación, pero la estación actual no se alerta (por ejemplo, puede ser una estación de operador en la que el estado de la oferta es aviso, como parpadear una luz). el software del conjunto de estaciones para la respuesta automática no debe responder a la llamada, ya que debe ser prerrogativa en la estación principal (de alertas), pero [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) se puede usar para conectar la llamada. Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor está activo (que sería la situación en una dirección no puente).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




