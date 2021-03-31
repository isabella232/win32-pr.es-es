---
title: Elemento de vídeo
description: Elemento de vídeo
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Aspectos de Windows Media Player, elemento de vídeo
- aspectos, elemento de vídeo
- Elemento de vídeo
- referencia de las máscaras, elemento de vídeo
- elementos, vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776639"
---
# <a name="video-element"></a>Elemento de vídeo

El elemento de **vídeo** proporciona una manera de manipular una ventana de vídeo en una máscara, mediante los siguientes atributos y eventos. También se proporciona un elemento de **vídeo** predefinido para mayor comodidad.

El elemento de **vídeo** admite los siguientes atributos.



| Atributo                                            | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](video-backgroundcolor.md)         | Especifica o recupera el color de fondo del control de vídeo.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.                                                                                                                               |
| [Completa](video-fullscreen.md)                   | Especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa. Solo se puede establecer en tiempo de ejecución.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Especifica o recupera un valor que indica si el vídeo mantendrá la relación de aspecto cuando se intenta ajustar el ancho y el alto definidos para el control.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Especifica o recupera un valor que indica si el vídeo se reducirá al ancho y al alto definidos para el control de vídeo.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Especifica o recupera un valor que indica si el vídeo se ajustará al ancho y al alto definidos para el control de vídeo.                                                                                                   |
| [Herramienta](video-tooltip.md)                         | Especifica o recupera el texto de información sobre herramientas para la ventana de vídeo.                                                                                                                                                                            |
| [sin ventana](video-windowless.md)                   | Especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar. Solo se puede establecer en tiempo de diseño. |
| [General](video-zoom.md)                               | Especifica el porcentaje por el que se va a escalar el vídeo.                                                                                                                                                                                    |



 

El elemento de **vídeo** puede implementar los controladores de eventos siguientes.



| Controlador de eventos                          | Descripción                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Controla un evento que se produce cuando el vídeo detiene la representación y se descarga. |
| [onvideostart](video-onvideostart.md) | Controla un evento que se produce cuando el vídeo se carga y comienza a representarse.  |



 

El elemento de **vídeo** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente, excepto donde se indique. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

Los elementos de vídeo predefinidos son elementos de **vídeo** normales con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes elementos de vídeo predefinidos.



| VÍDEO predefinido         | Descripción                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Un elemento de **vídeo** que estira el vídeo cuando se cambia el tamaño. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




