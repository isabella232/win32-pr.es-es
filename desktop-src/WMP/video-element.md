---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Reproductor de Windows Media máscaras, elemento VIDEO
- skins,ELEMENTO VIDEO
- Elemento VIDEO
- referencia de máscaras,elemento VIDEO
- elements,VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070827"
---
# <a name="video-element"></a>Elemento VIDEO

El **elemento VIDEO** proporciona una manera de manipular una ventana de vídeo en una máscara, mediante los siguientes atributos y eventos. También se proporciona **un elemento VIDEO** predefinido para mayor comodidad.

El **elemento VIDEO** admite los siguientes atributos.



| Atributo                                            | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](video-backgroundcolor.md)         | Especifica o recupera el color de fondo del control Vídeo.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Especifica o recupera el valor del cursor que se usa cuando el mouse está sobre un área en la que se puede hacer clic del vídeo.                                                                                                                               |
| [Fullscreen](video-fullscreen.md)                   | Especifica o recupera un valor que indica si el vídeo se muestra en modo de pantalla completa. Solo se puede establecer en tiempo de ejecución.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Especifica o recupera un valor que indica si el vídeo mantendrá la relación de aspecto al intentar ajustarse al ancho y alto definidos para el control.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Especifica o recupera un valor que indica si el vídeo se reducirá al ancho y alto definidos para el control Vídeo.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Especifica o recupera un valor que indica si el vídeo se ajustará al ancho y alto definidos para el control Vídeo.                                                                                                   |
| [Descripción](video-tooltip.md)                         | Especifica o recupera el texto de la información sobre herramientas para la ventana de vídeo.                                                                                                                                                                            |
| [sin ventana](video-windowless.md)                   | Especifica o recupera un valor que indica si el control Vídeo se va a usar en ventanas o sin ventanas; es decir, si todo el rectángulo del control estará visible en todo momento o se puede recortar. Solo se puede establecer en tiempo de diseño. |
| [Zoom](video-zoom.md)                               | Especifica el porcentaje por el que se va a escalar el vídeo.                                                                                                                                                                                    |



 

El **elemento VIDEO** puede implementar los siguientes controladores de eventos.



| Controlador de eventos                          | Descripción                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Controla un evento que tiene lugar cuando el vídeo deja de representarse y se descarga. |
| [onvideostart](video-onvideostart.md) | Controla un evento que tiene lugar cuando se carga el vídeo y comienza a representarse.  |



 

El **elemento VIDEO** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente, excepto donde se indica. Para obtener más información, vea [Atributos de ambiente](ambient-attributes.md) y Controladores de eventos de [ambiente.](ambient-event-handlers.md)

Los elementos de vídeo predefinidos son elementos **VIDEO** normales con varios valores de atributo comunes especificados de forma predeterminada. Están disponibles los siguientes elementos de vídeo predefinidos.



| VÍDEO predefinido         | Descripción                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Elemento **VIDEO** que ajusta el vídeo cuando se cambia el tamaño. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




