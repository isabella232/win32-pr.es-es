---
title: ELEMENTO EFFECTS
description: ELEMENTO EFFECTS
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Reproductor de Windows Media máscaras,elemento EFFECTS
- skins,EFFECTS, elemento
- EFFECTS, elemento
- referencia de máscaras,elemento EFFECTS
- elements,EFFECTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651145"
---
# <a name="effects-element"></a>ELEMENTO EFFECTS

El **elemento EFFECTS** proporciona una manera de organizar y manipular visualizaciones mediante los siguientes atributos y métodos. También se proporciona **un elemento EFFECTS** predefinido para mayor comodidad.

El **elemento EFFECTS** admite los atributos siguientes.



| Atributo                                                        | Descripción                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Especifica o recupera un valor que indica si se deben incluir todas las visualizaciones en el Registro.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Especifica o recupera la visualización actual.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera el número de valores preestablecidos disponibles para la visualización actual.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera el título de presentación de la visualización actual.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera el nombre del registro de la visualización actual.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Especifica o recupera el valor preestablecido actual de la visualización actual.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera el título del valor preestablecido actual de la visualización actual.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera un valor que indica si la visualización actual se puede mostrar a pantalla completa.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera el número de visualizaciones disponibles.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera un valor que indica si la visualización actual tiene una página de propiedades.                                                                                                                                                                  |
| [Fullscreen](effects-fullscreen.md)                             | Especifica o recupera un valor que indica si la visualización actual se muestra a pantalla completa. Solo se puede establecer en tiempo de ejecución.                                                                                                                   |
| [Ventana](effects-windowed.md)                                 | Especifica o recupera un valor que indica si la visualización va a estar en ventanas o sin ventanas, es decir, si todo el rectángulo del control estará visible en todo momento o si se puede recortar. Solo se puede establecer en tiempo de diseño. |



 

El **elemento EFFECTS** admite los métodos siguientes.



| Método                                       | Descripción                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera el nombre descriptivo de la visualización con el índice del Registro especificado.                               |
| [effectType](effects-effecttype.md)         | Recupera el nombre del Registro de la visualización con el índice del Registro especificado.                               |
| [siguiente](effects-next.md)                     | Muestra el siguiente valor preestablecido de visualización, pasando a la siguiente visualización si es necesario.                            |
| [nextEffect](effects-nexteffect.md)         | Muestra el primer valor preestablecido de la siguiente visualización, omitiendo los valores preestablecidos que intervienen.                                |
| [nextPreset](effects-nextpreset.md)         | Muestra el siguiente valor preestablecido de la visualización actual.                                                            |
| [previous](effects-previous.md)             | Muestra el valor preestablecido de visualización anterior, pasando al último valor preestablecido de la visualización anterior si es necesario. |
| [previousEffect](effects-previouseffect.md) | Muestra la visualización anterior, omitiendo los valores preestablecidos.                                                            |
| [previousPreset](effects-previouspreset.md) | Muestra el valor preestablecido anterior de la visualización actual.                                                        |
| [settings](effects-settings.md)             | Muestra la página de atributos de la visualización actual, si está presente.                                            |



 

El **elemento EFFECTS** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente.](ambient-event-handlers.md)

Los efectos predefinidos son elementos **EFFECTS** normales con varias configuraciones de atributo comunes especificadas de forma predeterminada. Están disponibles los siguientes efectos predefinidos.



| EFECTOS predefinidos           | Descripción                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Elemento **EFFECTS** que recorre en iteración los efectos disponibles. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




