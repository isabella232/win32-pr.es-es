---
title: Subtítulos
description: Subtítulos
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media de objetos, Intercambio de medios accesibles sincronizado (SAMI)
- object model,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- Reproductor de Windows Media ActiveX control, Intercambio de medios accesibles sincronizado (SAMI)
- Reproductor de Windows Media Control ActiveX dispositivos móviles, intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control, Intercambio de medios accesibles sincronizado (SAMI)
- Reproductor de Windows Media, migrar subtítulos
- Reproductor de Windows Media de objetos, subtítulos de extensión
- modelo de objetos, migración de subtítulos
- Reproductor de Windows Media Móvil, migración de subtítulos
- Reproductor de Windows Media ActiveX control, migrar subtítulos
- Reproductor de Windows Media Control de ActiveX móvil, migración de subtítulos
- ActiveX control, migración de subtítulos
- Intercambio multimedia accesible sincronizado (SAMI), migración de subtítulos
- SAMI (intercambio multimedia accesible sincronizado), migración de subtítulos
- guía de migración, Intercambio multimedia accesible sincronizado (SAMI)
- guía de migración, subtítulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa83cb5fb6735475a883986673c958db9642386bd8ce2c76151ddd6c2f23ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119607"
---
# <a name="closed-captioning"></a>Subtítulos

El control Reproductor de Windows Media 6.4 ActiveX incluye un panel de visualización de subtítulos integrado que, cuando se hace visible, habilita los subtítulos synchronized Accessible Media Interchange (SAMI) y muestra el texto del título cerrado. El Reproductor de Windows Media control 7 o posterior habilita la presentación de subtítulos SAMI mediante un elemento **<DIV>** HTML. Por ejemplo:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Esta técnica le proporciona una flexibilidad completa, ya que puede diseñar la página web para mostrar subtítulos de una manera personalizada. Ya no es necesario que la presentación del título cerrado esté en una ubicación fija adyacente a la Reproductor de Windows Media interfaz de usuario.

Una vez que haya creado un área para mostrar subtítulos, use *ClosedCaption*. **propiedad captioningID** para especificar la ubicación donde Reproductor de Windows Media representa el texto del título cerrado.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



El Reproductor de Windows Media Software Development Kit (SDK) contiene un ejemplo de trabajo de un reproductor insertado que muestra texto de subtítulo. Para obtener los ejemplos del SDK, descargue e instale el SDK Reproductor de Windows Media completo desde el sitio web de Microsoft. Para obtener más información sobre los subtítulos y SAMI, consulte el sitio [web de accesibilidad de Microsoft](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




