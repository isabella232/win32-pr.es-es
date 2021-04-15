---
title: Acerca de la copia de CD
description: Acerca de la copia de CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- CD, acerca de
- copiar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695548"
---
# <a name="about-cd-ripping"></a>Acerca de la copia de CD

El SDK de Windows Media Player 11 presenta nuevas funciones para copiar pistas de audio de CDs en el equipo del usuario. Este proceso se denomina *copia desde CD*.

Cuando se copian pistas de audio mediante las interfaces del SDK de Windows Media Player, las pistas de música resultantes se crean mediante la configuración definida por el usuario en el cuadro de diálogo **Opciones** de Media Player de Windows.

Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** . Para recuperar un puntero a esta interfaz, llame a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Mediante el uso de los métodos **Count** y **Item** , puede recorrer en iteración la colección para recuperar un puntero de la interfaz **IWMPCDROM** para cada unidad de CD del equipo del usuario. La interfaz **IWMPCdrom** representa una unidad de CD individual. Antes de empezar a copiar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la interfaz **IWMPCdromRip** .

Para iniciar la operación de copia, simplemente llame a [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Puede supervisar el progreso de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Este método recupera un valor de progreso para toda la operación de copia. El valor recuperado es un número que representa el porcentaje de copia completada. Puede supervisar el estado de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Este método recupera un valor de enumeración [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenido. También puede supervisar el estado de la operación de copia desde CD mediante el control del evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . Debe tener cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de copia desde CD para asegurarse de que la operación ha generado el evento. Puede detener la operación de copia desde CD llamando a [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Para recibir notificaciones de error sobre una operación de copia desde CD, puede controlar el evento [IWMPEvents3:: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) . Al igual que **CdromRipStateChange**, este evento proporciona un puntero de interfaz **IWMPCdromRip** que representa la operación de copia desde CD que ha generado el evento. El evento también proporciona un puntero **IDispatch** que representa el elemento multimedia que provocó el evento. Puede llamar a **QueryInterface** a través de este puntero para recuperar un puntero **IWMPMedia** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




