---
title: Proporcionar controles para recortar y extender imágenes
description: Proporcionar controles para recortar y extender imágenes
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
- Macro MCIWndGetDest
- Macro MCIWndPutDest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372158"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Proporcionar controles para recortar y extender imágenes

MCIWnd permite recortar y extender imágenes de un clip de vídeo. Para comprender estas características, debe comprender las relaciones entre el tamaño del *marco,* el rectángulo de *origen,* el rectángulo de *destino* y el área *de reproducción.*

Un clip de vídeo consta de varios fotogramas, cada uno con una imagen. El tamaño del fotograma de un clip de vídeo es el tamaño de la imagen en el fotograma actual. Normalmente, un clip de vídeo tiene un tamaño de fotograma porque todas las imágenes del clip tienen el mismo tamaño.

El rectángulo de origen es un área rectangular que superpone los fotogramas de un clip de vídeo. El rectángulo de origen define la parte de cada fotograma que se muestra durante la reproducción. Cuando se carga un clip de vídeo con MCIWnd, el rectángulo de origen se inicializa con las mismas dimensiones y posición que el fotograma inicial del clip de vídeo.

El rectángulo de destino es un área rectangular que define una ventana de reproducción virtual. El rectángulo de destino recibe los datos de imagen del rectángulo de origen para cada fotograma del clip de vídeo. Cuando las dimensiones del rectángulo de origen y de destino son diferentes, MCIWnd ajusta los datos de la imagen horizontal y verticalmente según sea necesario para rellenar el rectángulo de destino. Cuando se carga un clip de vídeo con MCIWnd, el rectángulo de destino se inicializa con las mismas dimensiones y posición que el fotograma inicial del clip de vídeo.

El área de reproducción es la parte de una ventana de MCIWnd que una aplicación usa para mostrar el clip de vídeo. El área de reproducción es el área cliente de una ventana MCIWnd o la parte del área de cliente que excluye la barra de herramientas de MCIWnd. Cuando se carga un clip de vídeo con MCIWnd, el área de reproducción se inicializa con las mismas dimensiones y posición que el fotograma inicial del clip de vídeo.

Puede recortar un clip de vídeo mediante las macros [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) y [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) para modificar el rectángulo de origen. El recorte de una imagen determina solo qué parte de los fotogramas se muestran durante la reproducción; no modifica el contenido del archivo que se va a reproducir. Antes de recortar una imagen, puede recuperar el tamaño actual del rectángulo de origen mediante **MCIWndGetSource**. Después de calcular el nuevo tamaño y la ubicación del rectángulo de origen, puede establecer los límites de recorte del rectángulo de origen mediante **MCIWndPutSource**.

Puede extender un clip de vídeo mediante las macros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) y [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) para modificar el rectángulo de destino. Al extender un clip de vídeo, se acorta o se acorta el tamaño del fotograma de un clip de vídeo vertical, horizontalmente o en ambas direcciones. Antes de extender una imagen, puede recuperar el tamaño y la ubicación actuales del rectángulo de destino mediante **MCIWndGetDest.** La **macro MCIWndPutDest** permite volver a definir el rectángulo de destino. El stretch puede distorsionar la imagen durante la reproducción, pero no modifica el contenido del archivo que se está reproduciendo.

Si el tamaño del rectángulo de destino es mayor que el área de reproducción, puede especificar qué parte del área de reproducción mostrará el clip de vídeo mediante **MCIWndPutDest.**

> [!Note]  
> La [**macro MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) no cambia el tamaño del área de reproducción. Para extender la ventana MCIWnd junto con el rectángulo de destino, debe conocer el tamaño actual de la ventana MCIWnd y emitir nuevas dimensiones de ventana basadas en el rectángulo de destino. Puede recuperar las dimensiones de la ventana MCIWnd mediante la función [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) y cambiar el tamaño de la ventana MCIWnd mediante la [función SetWindowPos.](/windows/win32/api/winuser/nf-winuser-setwindowpos)

 

 

 