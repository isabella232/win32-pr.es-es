---
title: Elemento BUTTONGROUP
description: Elemento BUTTONGROUP
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Reproductor de Windows Media máscaras,elemento BUTTONGROUP
- máscaras, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- referencia de máscaras,elemento BUTTONGROUP
- elements,BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021d29322b98fe4cea96a67998aaf82fbd11e1abe397578a9b0f8999179ee1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120056"
---
# <a name="buttongroup-element"></a>Elemento BUTTONGROUP

El **elemento BUTTONGROUP** proporciona una manera de agrupar varios botones dentro de una máscara. Estos botones se pueden especificar mediante el uso de **elementos BUTTONELEMENT** como elementos secundarios del **elemento BUTTONGROUP.**

El **elemento BUTTONGROUP** admite los atributos siguientes.



| Atributo                                              | Descripción                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | Recupera el número de botones de **BUTTONGROUP.**                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | Especifica o recupera el tipo de cursor que aparece cuando el mouse está sobre un botón en **BUTTONGROUP**.                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | Especifica o recupera el nombre de la imagen que representa el estado deshabilitado de los botones en **BUTTONGROUP**.                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | Especifica o recupera el nombre de la imagen que representa el estado de apagado de **BUTTONGROUP.**                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | Especifica o recupera el nombre de la imagen que representa el estado de mantener el mouse sobre un botón en **BUTTONGROUP.** El estado de mantener el mouse hacia abajo se produce cuando el botón está en estado de bajada y el usuario mantiene el mouse sobre él con el mouse. |
| [hoverImage](buttongroup-hoverimage.md)               | Especifica o recupera el nombre de la imagen que representa el estado del mouse de un botón en **BUTTONGROUP.** El estado de mantener el puntero se produce cuando el botón está en estado hacia arriba y el usuario mantiene el mouse sobre él con el mouse.             |
| [hueShift](buttongroup-hueshift.md)                   | Especifica o recupera la cantidad por la que se desplaza el matiz de las imágenes **BUTTONGROUP.**                                                                                                                                    |
| [image](buttongroup-image.md)                         | Especifica o recupera el nombre de la imagen que representa los botones de **buttongroup.**                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | Especifica o recupera el nombre de la imagen que representa el mapa de botones de **BUTTONGROUP.**                                                                                                                                |
| [radio](buttongroup-radio.md)                         | Especifica o recupera un valor que indica si **BUTTONGROUP** se compone de botones de radio.                                                                                                                             |
| [Saturación](buttongroup-saturation.md)               | Especifica o recupera el valor de saturación de las **imágenes BUTTONGROUP.**                                                                                                                                                      |
| [showBackground](buttongroup-showbackground.md)       | Especifica o recupera un valor que indica si **BUTTONGROUP** muestra solo los botones o muestra el mapa de bits completo especificado en el **atributo image.**                                                              |
| [transparencyColor](buttongroup-transparencycolor.md) | Especifica o recupera el color transparente de las **imágenes BUTTONGROUP.**                                                                                                                                                     |



 

El **elemento BUTTONGROUP** admite los métodos siguientes.



| Método                                 | Descripción                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [Haga clic](buttongroup-click.md)         | Llama al **controlador de eventos onclick** definido para **BUTTONELEMENT** con el índice especificado. |
| [getButton](buttongroup-getbutton.md) | Recupera **buttonelement con** el índice especificado.                                       |



 

El **elemento BUTTONGROUP** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente.](ambient-event-handlers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




