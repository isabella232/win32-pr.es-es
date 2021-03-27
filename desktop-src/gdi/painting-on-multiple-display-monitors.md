---
description: El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen diferentes profundidades de color.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Pintar en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811906"
---
# <a name="painting-on-multiple-display-monitors"></a>Pintar en varios monitores de pantalla

El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen diferentes profundidades de color. Normalmente, esto produce buenos resultados, pero puede no ser óptimo. Por ejemplo, una ventana de dos monitores de profundidades de color considerablemente diferentes podría tener una representación de color deficiente. Además, los monitores con la misma profundidad de color pueden tener un ejemplo de formatsfor de color diferente, los colores se pueden codificar con diferentes números de bits o estar ubicados en lugares diferentes en el valor de color de un píxel.

Para obtener los mejores resultados de cada uno de los monitores de un controlador de dominio que abarca más de una pantalla, llame a [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) para enumerar los monitores que forman una intersección con el controlador de dominio y pinte el área de intersección de cada uno de ellos por separado según los atributos de visualización de ese monitor. Vea el ejemplo del [dibujo en un controlador de dominio que abarca varias pantallas](painting-on-a-dc-that-spans-multiple-displays.md).

Si realiza todo el dibujo en el código de **\_ Paint de WM** y el código de **\_ Paint de WM** controla todos los distintos modos de vídeo, debería poder colocar el código de la **\_ pintura de WM** en el **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) con solo algunas modificaciones.

 

 



