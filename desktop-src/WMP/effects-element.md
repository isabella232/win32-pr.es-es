---
title: EFFECTs, elemento
description: EFFECTs, elemento
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Aspectos de Windows Media Player, elemento EFFECTs
- máscaras, elemento EFFECTs
- EFFECTs, elemento
- referencia de las máscaras, elemento EFFECTs
- elementos, efectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b6fdcde74288b0dd4215732d1e5b6a281154f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418378"
---
# <a name="effects-element"></a>EFFECTs, elemento

El elemento **Effects** proporciona una manera de organizar y manipular visualizaciones mediante los siguientes atributos y métodos. También se proporciona un elemento predefinido **Effects** para mayor comodidad.

El elemento **Effects** admite los siguientes atributos.



| Atributo                                                        | Descripción                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | Especifica o recupera un valor que indica si se deben incluir todas las visualizaciones en el registro.                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | Especifica o recupera la visualización actual.                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | Recupera el número de valores preestablecidos disponibles para la visualización actual.                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | Recupera el título de presentación de la visualización actual.                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | Recupera el nombre del registro de la visualización actual.                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | Especifica o recupera el valor predeterminado actual de la visualización actual.                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | Recupera el título del valor predeterminado actual de la visualización actual.                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | Recupera un valor que indica si la visualización actual se puede mostrar a pantalla completa.                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | Recupera el número de visualizaciones disponibles.                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | Recupera un valor que indica si la visualización actual tiene una página de propiedades.                                                                                                                                                                  |
| [Completa](effects-fullscreen.md)                             | Especifica o recupera un valor que indica si la visualización actual se muestra en pantalla completa. Solo se puede establecer en tiempo de ejecución.                                                                                                                   |
| [ventanas](effects-windowed.md)                                 | Especifica o recupera un valor que indica si la visualización se va a dividir en ventanas o sin ventanas, es decir, si todo el rectángulo del control será visible en todo momento o si se puede recortar. Solo se puede establecer en tiempo de diseño. |



 

El elemento **Effects** admite los métodos siguientes.



| Método                                       | Descripción                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | Recupera el nombre descriptivo de la visualización con el índice de registro especificado.                               |
| [effectType](effects-effecttype.md)         | Recupera el nombre del registro de la visualización con el índice del registro especificado.                               |
| [siguiente](effects-next.md)                     | Muestra el valor preestablecido de visualización siguiente, pasando a la siguiente visualización si es necesario.                            |
| [nextEffect](effects-nexteffect.md)         | Muestra el primer valor predefinido de la siguiente visualización, omitiendo los valores preestablecidos que intervienen.                                |
| [nextPreset](effects-nextpreset.md)         | Muestra el siguiente valor preestablecido de la visualización actual.                                                            |
| [previous](effects-previous.md)             | Muestra el valor preestablecido de visualización anterior, pasando al último valor preestablecido de la visualización anterior si es necesario. |
| [previousEffect](effects-previouseffect.md) | Muestra la visualización anterior, omitiendo los valores preestablecidos.                                                            |
| [previousPreset](effects-previouspreset.md) | Muestra el valor preestablecido anterior de la visualización actual.                                                        |
| [settings](effects-settings.md)             | Muestra la página de atributos de la visualización actual, si está presente.                                            |



 

El elemento **Effects** admite los atributos de ambiente y puede implementar los controladores de eventos ambiente. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

Los efectos predefinidos son elementos de **efectos** normales con varios valores de atributos comunes especificados de forma predeterminada. Están disponibles los siguientes efectos predefinidos.



| EFECTOS predefinidos           | Descripción                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | Un elemento **Effects** que recorre en iteración los efectos disponibles. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




