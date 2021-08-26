---
title: Acerca de CD Desasoyendo
description: Acerca de CD Desasoyendo
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Reproductor de Windows Media, cds
- Reproductor de Windows Media modelo de objetos, algarada de CD
- modelo de objetos, resalte de CD
- Reproductor de Windows Media ActiveX control, cds
- ActiveX control, cds
- Reproductor de Windows Media Control ActiveX dispositivos móviles, algarada de CD
- Reproductor de Windows Media Móvil, cds
- CD a, acerca de
- CDs de arras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903605"
---
# <a name="about-cd-ripping"></a>Acerca de CD Desasoyendo

El SDK Reproductor de Windows Media 11 presenta una nueva funcionalidad para copiar pistas de audio desde CD al equipo del usuario. Este proceso se denomina *algar.*

Cuando se desgarran pistas de audio mediante las interfaces del SDK de Reproductor de Windows Media, las pistas de música resultantes se crean mediante la configuración definida por el usuario en el cuadro de diálogo Reproductor de Windows Media **opciones.**

Para enumerar las unidades de CD en el equipo del usuario, use la **interfaz IWMPCdromCollection.** Para recuperar un puntero a esta interfaz, llame a [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Mediante el uso **de los métodos count** y **item,** puede iterar la colección para recuperar un puntero de interfaz **IWMPCdrom** para cada unidad de CD del equipo del usuario. La **interfaz IWMPCdrom** representa una unidad de CD individual. Antes de empezar a trabajar con un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la **interfaz IWMPCdromRip.**

Para iniciar la operación de desenlazado, simplemente llame a [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Puede supervisar el progreso de la operación de pra llamando periódicamente a [IWMPCdromRip::get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Este método recupera un valor de progreso para toda la operación de async. El valor recuperado es un número que representa el porcentaje de aseadas completadas. Puede supervisar el estado de la operación de integración llamando periódicamente a [IWMPCdromRip::get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Este método recupera un valor de [enumeración WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenida. También puede supervisar el estado de la operación de manipulación controlando el evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) Debe tener cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de alerón para asegurarse de que la operación ha producido el evento. Puede detener la operación de zilla llamando a [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Para recibir notificaciones de error sobre una operación de estoque, puede controlar el evento [IWMPEvents3::CdromRipMediaError.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) Al **igual que CdromRipStateChange,** este evento proporciona un puntero de interfaz **IWMPCdromRip** que representa la operación de direccionamiento que ha producido el evento. El evento también proporciona un **puntero IDispatch** que representa el elemento multimedia que ha producido el evento. Puede llamar a **QueryInterface a través** de este puntero para recuperar un **puntero IWMPMedia.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> </dl>

 

 




