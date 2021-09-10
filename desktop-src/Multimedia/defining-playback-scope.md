---
title: Definición del ámbito de reproducción
description: Definición del ámbito de reproducción
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372169"
---
# <a name="defining-playback-scope"></a>Definición del ámbito de reproducción

MCIWnd proporciona macros que permiten definir el ámbito de *reproducción*. El ámbito es la parte de la reproducción que desea reproducir. Por ejemplo, puede reproducir el contenido desde una posición que no sea la posición inicial mediante la macro [**MCIWndPlayFrom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) Esta macro se mueve a la posición especificada, comienza la reproducción y continúa hasta el final del contenido. De forma similar, puede reproducir el contenido en un punto final especificado mediante la macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) Esta macro comienza en la posición de reproducción actual y se reproduce hasta que alcanza la posición especificada o se alcanza el final del contenido, lo que llegue primero.

Además, puede definir las posiciones inicial y final mediante la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) Esta macro se mueve a la posición inicial especificada y se reproduce hasta que se alcanza la posición final especificada o el final del contenido.

 

 




