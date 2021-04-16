---
description: Las \_ constantes de marcador de bits LINECONNECTEDMODE describen diferentes subestados de una llamada conectada.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes de LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690502"
---
# <a name="lineconnectedmode_-constants"></a>Constantes de LINECONNECTEDMODE \_

Las constantes de marcador de bits **LINECONNECTEDMODE \_** describen diferentes subestados de una llamada conectada. Un modo está disponible como estado de la llamada a la aplicación después de que el estado de la llamada cambie a conectado y en el mensaje de línea \_ CALLSTATE que indica que la llamada está en LINECALLSTATE \_ conectado. Estos valores se usan cuando la llamada se realiza en una dirección compartida (con puentes) con otras estaciones (para obtener más información, consulte [**\_ constantes de LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas. Las **\_ constantes LINECONNECTEDMODE** tienen los siguientes valores:

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ activo**
</dt> <dd> <dl> <dt>



Indica que la llamada está conectada a la estación actual (la estación actual es un participante en la llamada). Si el modo de estado de la llamada es 0 (cero), la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente). El modo puede cambiar entre activo e inactivo durante una llamada si el usuario se une y deja la llamada a través de la acción manual. En una situación de puente, es posible que una operación de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) no elimine realmente la llamada o la ponga en espera, ya que el estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones); en su lugar, la llamada puede cambiar al modo inactivo si permanece conectado en otras estaciones.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**
</dt> <dd> <dl> <dt>



Indica que la estación es un participante activo en la llamada, pero que la parte remota ha realizado la llamada en espera (la otra parte considera que la llamada está en estado de suspensión). Normalmente, esta información solo está disponible cuando ambos extremos de la llamada se encuentran en el mismo dominio de cambio. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmado**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios ha recibido una notificación afirmativa de que la llamada ha entrado en el estado conectado (por ejemplo, a través de la supervisión de respuestas o mecanismos similares). Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INactivo**
</dt> <dd> <dl> <dt>



Indica que la llamada está activa en una o varias estaciones, pero la estación actual no es un participante de la llamada. Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente). Una llamada en el estado inactivo se puede combinar con [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). Muchas operaciones que son válidas en llamadas en el estado CONNECTed pueden ser imposibles en el modo inactivo, como la supervisión de tonos y dígitos, ya que la estación no participa realmente en la llamada; Normalmente, la supervisión se suspende (aunque no se cancela) mientras la llamada está en modo inactivo.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**
</dt> <dd> <dl> <dt>



Indica que la estación no es un participante activo en la llamada y que la parte remota ha realizado la llamada en espera. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

No extensible. Todos los 32 bits están reservados.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no utilizar los valores de LINECONNECTEDMODE \_ que no se admiten en la versión negociada. Las aplicaciones que no son Cognizant de LINECONNECTEDMODE \_ probablemente suponen que una llamada que está en LINECALLSTATE \_ conectada está activa en LINECONNECTEDMODE \_ .

Los \_ valores INactivos de LINECONNECTEDMODE activo y LINECONNECTEDMODE \_ se usan cuando la llamada está en una dirección que se comparte con otras estaciones (puente; [**vea \_ constantes de LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemas de claves electrónicas. Si el modo de estado de llamada conectado es "activo", significa que la llamada está conectada a la estación actual (la estación actual es un participante en la llamada). Si el modo de estado de la llamada es "inactivo", la llamada está activa en una o varias estaciones, pero la estación actual no es un participante de la llamada. Si el modo de estado de la llamada es cero, la aplicación debe suponer que el valor es "Active" (que sería la situación en una dirección no puente). El modo puede cambiar entre activo e inactivo durante una llamada si el usuario se une y deja la llamada a través de la acción manual.

En una situación de puente, es posible que una operación de [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) no elimine realmente la llamada o la ponga en espera, ya que el estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones). en su lugar, la llamada solo se puede cambiar al modo inactivo si permanece conectado en otras estaciones. Una llamada en el estado inactivo puede combinarse mediante [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).

Muchas operaciones que son válidas en llamadas en el estado Connected pueden ser imposibles en el modo inactivo, como la supervisión de tonos y dígitos, ya que la estación no participa realmente en la llamada; Normalmente, la supervisión se suspende (aunque no se cancela) mientras la llamada está en modo inactivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




