---
title: Definición del ámbito de reproducción
description: Definición del ámbito de reproducción
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853c74cc4115cee72e4253e339f934e73b8d8e7e223f1b91e9992969c4ce3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785425"
---
# <a name="defining-playback-scope"></a>Definición del ámbito de reproducción

MCIWnd proporciona macros que permiten definir el ámbito de *reproducción*. El ámbito es la parte de la reproducción que desea reproducir. Por ejemplo, puede reproducir el contenido desde una posición que no sea la posición inicial mediante la macro [**MCIWndPlayFrom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) Esta macro se mueve a la posición especificada, comienza la reproducción y continúa hasta el final del contenido. De forma similar, puede reproducir el contenido en un punto final especificado mediante la macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) Esta macro comienza en la posición de reproducción actual y se reproduce hasta que alcanza la posición especificada o se alcanza el final del contenido, lo que llegue primero.

Además, puede definir las posiciones inicial y final mediante la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) Esta macro se mueve a la posición inicial especificada y se reproduce hasta que se alcanza la posición final especificada o el final del contenido.

 

 




