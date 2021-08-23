---
title: Funciones (Api de ampliación)
description: Esta sección contiene información de referencia sobre las funciones de la API de ampliación.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 4513258f5c4bbb1cafe9ef22b35a4708c63e1c45be353b55c8bda1e20c4fce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644625"
---
# <a name="magnification-api-functions"></a>Funciones de API de ampliación

Esta sección contiene información de referencia sobre las funciones de la API de ampliación.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|:---|:---|
| [**MagGetColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Obtiene la matriz de transformación de color para un control de lupa.<br/> |
| [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Recupera la matriz de transformación de color asociada a la lupa de pantalla completa.<br/> |
| [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Recupera la configuración de ampliación para la lupa de pantalla completa.<br/>  |
| [***MagGetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _*En desuso en Windows 7 y versiones posteriores**<br/>Recupera la función de devolución de llamada registrada que implementa una transformación personalizada para el escalado de imágenes. <br/> |
| [**MagGetInputTransform**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Recupera la transformación de entrada actual para la entrada táctil y de lápiz, representada como un rectángulo de origen y un rectángulo de destino.<br/>  |
| [**MagGetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Recupera la lista de ventanas que se amplían o excluyen de la ampliación.<br/>  |
| [**MagGetWindowSource**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Obtiene el rectángulo del área que se va a ampliar.<br/>  |
| [**MagGetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Recupera la matriz de transformación asociada a un control de lupa. <br/>  |
| [***MagImageScalingCallback** _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _*En desuso en Windows 7 y versiones posteriores**<br/>Prototipo de una función de devolución de llamada que implementa una transformación personalizada para el escalado de imágenes.<br/>  |
| [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Crea e inicializa los objetos en tiempo de ejecución de lupa. <br/>  |
| [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >establece la matriz de transformación de color para un control de lupa.<br/>  |
| [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Cambia la matriz de transformación de color asociada a la lupa de pantalla completa.<br/>  |
| [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Cambia la configuración de ampliación de la lupa de pantalla completa.<br/>  |
| [***MagSetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _*En desuso en Windows 7 y versiones posteriores**<br/>Establece la función de devolución de llamada para el filtrado y el escalado externos de imágenes.<br/>  |
| [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Establece la transformación de entrada activa actual para la entrada táctil y de lápiz, representada como un rectángulo de origen y un rectángulo de destino.<br/>  |
| [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Establece la lista de ventanas que se va a aumentar o la lista de ventanas que se excluirán de la ampliación.<br/>  |
| [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Establece el rectángulo de origen de la ventana de ampliación.<br/>  |
| [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Establece la matriz de transformación para un control de lupa. <br/>  |
| [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Muestra u oculta el cursor del sistema.<br/>  |
| [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Destruye los objetos en tiempo de ejecución de lupa.<br/>  |

## <a name="related-topics"></a>Temas relacionados

[Referencia](entry-magapi-ref.md)
