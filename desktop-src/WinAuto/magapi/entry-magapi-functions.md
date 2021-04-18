---
title: Functions (API de ampliación)
description: Esta sección contiene información de referencia sobre las funciones de la API de ampliación.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 33418b0d74ec55b7e67cdf5a6130cbd867186dac
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721639"
---
# <a name="magnification-api-functions"></a>Funciones de la API de ampliación

Esta sección contiene información de referencia sobre las funciones de la API de ampliación.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|:---|:---|
| [**MagGetColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Obtiene la matriz de transformación de color para un control ampliador.<br/> |
| [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Recupera la matriz de transformación de color asociada al ampliador de pantalla completa.<br/> |
| [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Recupera la configuración de ampliación del ampliador de pantalla completa.<br/>  |
| [***MagGetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _ * En desuso en Windows 7 y versiones posteriores * *<br/>Recupera la función de devolución de llamada registrada que implementa una transformación personalizada para el ajuste de escala de la imagen. <br/> |
| [**MagGetInputTransform**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Recupera la transformación de entrada actual para el lápiz y la entrada táctil, representada como un rectángulo de origen y un rectángulo de destino.<br/>  |
| [**MagGetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Recupera la lista de ventanas que se amplían o se excluyen de la ampliación.<br/>  |
| [**MagGetWindowSource**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Obtiene el rectángulo del área que se va a ampliar.<br/>  |
| [**MagGetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Recupera la matriz de transformación asociada a un control ampliador. <br/>  |
| [***MagImageScalingCallback** _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _ * En desuso en Windows 7 y versiones posteriores * *<br/>Prototipo para una función de devolución de llamada que implementa una transformación personalizada para el ajuste de escala de imagen.<br/>  |
| [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Crea e inicializa los objetos de tiempo de ejecución del ampliador. <br/>  |
| [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >establece la matriz de transformación de color para un control ampliador.<br/>  |
| [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Cambia la matriz de transformación de color asociada al ampliador de pantalla completa.<br/>  |
| [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Cambia la configuración de ampliación del ampliador de pantalla completa.<br/>  |
| [***MagSetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _ * En desuso en Windows 7 y versiones posteriores * *<br/>Establece la función de devolución de llamada para el filtrado y el escalado de imágenes externas.<br/>  |
| [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Establece la transformación de entrada activa actual para el lápiz y la entrada táctil, representada como un rectángulo de origen y un rectángulo de destino.<br/>  |
| [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Establece la lista de ventanas que se va a ampliar o la lista de ventanas que se van a excluir de la ampliación.<br/>  |
| [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Establece el rectángulo de origen para la ventana de ampliación.<br/>  |
| [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Establece la matriz de transformación para un control ampliador. <br/>  |
| [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Muestra u oculta el cursor del sistema.<br/>  |
| [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Destruye los objetos de tiempo de ejecución del ampliador.<br/>  |

## <a name="related-topics"></a>Temas relacionados

[Referencia](entry-magapi-ref.md)
