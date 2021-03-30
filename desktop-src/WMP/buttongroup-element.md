---
title: Elemento BUTTONGROUP
description: Elemento BUTTONGROUP
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Aspectos de Windows Media Player, elemento BUTTONGROUP
- aspectos, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- referencia de las máscaras, elemento BUTTONGROUP
- elementos, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148847"
---
# <a name="buttongroup-element"></a>Elemento BUTTONGROUP

El elemento **BUTTONGROUP** proporciona una manera de agrupar varios botones dentro de una máscara. Estos botones se pueden especificar mediante los elementos **BUTTONELEMENT** como elementos secundarios del elemento **BUTTONGROUP** .

El elemento **BUTTONGROUP** admite los siguientes atributos.



| Atributo                                              | Descripción                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | Recupera el número de botones de **BUTTONGROUP**.                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | Especifica o recupera el tipo de cursor que aparece cuando el mouse está encima de un botón en **BUTTONGROUP**.                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | Especifica o recupera el nombre de la imagen que representa el Estado deshabilitado de los botones de **BUTTONGROUP**.                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | Especifica o recupera el nombre de la imagen que representa el estado de inactividad de **BUTTONGROUP**.                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | Especifica o recupera el nombre de la imagen que representa el estado de mantener el mouse de un botón en el **BUTTONGROUP**. El estado de desactivación se produce cuando el botón está en estado inactivo y el usuario mantiene el mouse sobre él. |
| [hoverImage](buttongroup-hoverimage.md)               | Especifica o recupera el nombre de la imagen que representa el estado de desplazamiento de un botón en el **BUTTONGROUP**. El estado de desplazamiento se produce cuando el botón está en el estado up y el usuario mantiene el mouse sobre él.             |
| [hueShift](buttongroup-hueshift.md)                   | Especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes de **BUTTONGROUP** .                                                                                                                                    |
| [image](buttongroup-image.md)                         | Especifica o recupera el nombre de la imagen que representa los botones de un **BUTTONGROUP**.                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | Especifica o recupera el nombre de la imagen que representa el mapa de botones de **BUTTONGROUP**.                                                                                                                                |
| [radio](buttongroup-radio.md)                         | Especifica o recupera un valor que indica si **BUTTONGROUP** se compone de botones de radio.                                                                                                                             |
| [satura](buttongroup-saturation.md)               | Especifica o recupera el valor de saturación de las imágenes de **BUTTONGROUP** .                                                                                                                                                      |
| [showBackground](buttongroup-showbackground.md)       | Especifica o recupera un valor que indica si **BUTTONGROUP** solo muestra los botones o muestra el mapa de bits completo especificado en el atributo de **imagen** .                                                              |
| [Property](buttongroup-transparencycolor.md) | Especifica o recupera el color transparente de las imágenes de **BUTTONGROUP** .                                                                                                                                                     |



 

El elemento **BUTTONGROUP** admite los siguientes métodos.



| Método                                 | Descripción                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [hizo](buttongroup-click.md)         | Llama al controlador de eventos **onclick** definido para **BUTTONELEMENT** con el índice especificado. |
| [getButton](buttongroup-getbutton.md) | Recupera **BUTTONELEMENT** con el índice especificado.                                       |



 

El elemento **BUTTONGROUP** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




