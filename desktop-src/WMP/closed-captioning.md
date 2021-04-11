---
title: Subtítulos (CC)
description: Subtítulos (CC)
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player, migrar subtítulos (CC)
- Modelo de objetos de Windows Media Player, subtítulos (CC) Smigrating
- modelo de objetos, migrar subtítulos
- Windows Media Player Mobile, migrar subtítulos (CC)
- Control ActiveX de Windows Media Player, migrar subtítulos (CC)
- Control ActiveX móvil de Windows Media Player, migración de subtítulos cerrados
- Control ActiveX, migrar subtítulos (CC)
- Intercambio de multimedia accesible sincronizado (SAMI), migración de subtítulos cerrados
- SAMI (intercambio de multimedia accesible sincronizado), migración de subtítulos cerrados
- Guía de migración, intercambio de multimedia accesible sincronizado (SAMI)
- Guía de migración, subtítulos (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149106"
---
# <a name="closed-captioning"></a>Subtítulos (CC)

El control ActiveX de Windows Media Player 6,4 incluye un panel de presentación de un título cerrado integrado que, cuando se hace visible, habilita los subtítulos (SAMI) de intercambio de medios accesibles sincronizados y muestra el texto de la leyenda cerrada. El control Windows Media Player 7 o posterior habilita la presentación de la leyenda cerrada de SAMI mediante un **<DIV>** elemento HTML. Por ejemplo:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Esta técnica proporciona una flexibilidad completa, ya que puede diseñar su página web para mostrar los subtítulos (CC) de una manera personalizada. ya no es necesario que la presentación de subtítulos cerrados esté en una ubicación fija adyacente a la interfaz de usuario de Windows Media Player.

Una vez que haya creado un área para mostrar los subtítulos cerrados, use *ClosedCaption*. propiedad **captioningID** para especificar la ubicación donde Windows Media Player representa el texto de la leyenda cerrada.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



El kit de desarrollo de software (SDK) de Windows Media Player contiene un ejemplo funcional de un reproductor incrustado que muestra el texto de la leyenda cerrada. Para obtener los ejemplos del SDK, descargue e instale el SDK de Windows Media Player completo en el sitio web de Microsoft. Para obtener más información acerca de los subtítulos y SAMI, vea el [sitio web de accesibilidad de Microsoft](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




