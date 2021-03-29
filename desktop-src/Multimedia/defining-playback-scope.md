---
title: Definir el ámbito de reproducción
description: Definir el ámbito de reproducción
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom (macro)
- MCIWndPlayTo (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994201"
---
# <a name="defining-playback-scope"></a>Definir el ámbito de reproducción

MCIWnd proporciona macros que permiten definir el *ámbito* de reproducción. El ámbito es la parte de la reproducción que desea reproducir. Por ejemplo, puede reproducir el contenido de una posición distinta de la posición inicial mediante la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) . Esta macro se mueve a la posición especificada, comienza la reproducción y continúa hasta el final del contenido. Del mismo modo, puede reproducir el contenido en un punto final especificado mediante la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) . Esta macro se inicia en la posición de reproducción actual y se reproduce hasta que llega a la posición especificada o hasta que se alcanza el final del contenido, lo que suceda primero.

Además, puede definir las posiciones inicial y final mediante la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) . Esta macro se mueve a la posición inicial especificada y se reproduce hasta que se alcanza la posición final especificada o el final del contenido.

 

 




