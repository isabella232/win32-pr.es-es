---
title: Elemento LISTBOX
description: Elemento LISTBOX
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Aspectos de Windows Media Player, elemento LISTBOX
- máscaras, elemento LISTBOX
- Elemento LISTBOX
- referencia de las máscaras, elemento LISTBOX
- elementos, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075509"
---
# <a name="listbox-element"></a>Elemento LISTBOX

El elemento **ListBox** proporciona una manera para que los usuarios seleccionen elementos de una lista. Estos elementos se pueden especificar utilizando elementos **Item** como elementos secundarios del elemento **ListBox** . Si necesita un control de cuadro de lista que solo se muestre cuando sea necesario, use el elemento **popup** , que es idéntico al elemento **ListBox** excepto el valor predeterminado del atributo **popup** , que determina su comportamiento de presentación.

El elemento **ListBox** admite los siguientes atributos.



| Atributo                                        | Descripción                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](listbox-backgroundcolor.md)   | Especifica o recupera el color de fondo del control de cuadro de lista.                                                  |
| [PDA](listbox-border.md)                     | Especifica o recupera un valor que indica si el control de cuadro de lista tiene un borde. Solo se puede establecer en tiempo de diseño.  |
| [firstVisibleItem](listbox-firstvisibleitem.md) | Especifica o recupera el índice de la primera línea visible en el control de cuadro de lista.                                   |
| [focusItem](listbox-focusitem.md)               | Especifica o recupera la línea que contiene el foco.                                                                  |
| [fontFace](listbox-fontface.md)                 | Especifica o recupera la fuente para el control de cuadro de lista.                                                             |
| [fontSize](listbox-fontsize.md)                 | Especifica o recupera el tamaño de fuente para el control de cuadro de lista.                                                        |
| [fontStyle](listbox-fontstyle.md)               | Especifica o recupera el estilo de fuente para el control de cuadro de lista.                                                       |
| [foregroundColor](listbox-foregroundcolor.md)   | Especifica o recupera el color del texto en el control de cuadro de lista.                                                        |
| [itemCount](listbox-itemcount.md)               | Recupera el número de elementos del control de cuadro de lista.                                                                |
| [Selección múltiple](listbox-multiselect.md)           | Especifica o recupera un valor que indica si el usuario puede seleccionar varias líneas. Solo se puede establecer en tiempo de diseño. |
| [Emergente](listbox-popup.md)                       | Especifica un valor que indica si el elemento representa un control emergente o de cuadro de lista.                              |
| [readOnly](listbox-readonly.md)                 | Especifica o recupera un valor que indica si el texto es de solo lectura o si el usuario puede seleccionar texto.              |
| [selectedItem](listbox-selecteditem.md)         | Especifica o recupera el índice del elemento seleccionado en el control de cuadro de lista.                                        |
| [ordenados](listbox-sorted.md)                     | Especifica o recupera un valor que indica si el control de cuadro de lista está ordenado alfabéticamente.                      |



 

El elemento **ListBox** admite los métodos siguientes.



| Método                                                 | Descripción                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [appendItem](listbox-appenditem.md)                   | Inserta texto nuevo al final del control de cuadro de lista.                                                                  |
| [deleteAll](listbox-deleteall.md)                     | Elimina todos los elementos del control de cuadro de lista.                                                                          |
| [deleteItem](listbox-deleteitem.md)                   | Elimina el elemento de control de cuadro de lista en el índice especificado.                                                             |
| [rechazar](listbox-dismiss.md)                         | Oculta el control.                                                                                                    |
| [findItem](listbox-finditem.md)                       | Busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.                                |
| [getItem](listbox-getitem.md)                         | Recupera el texto del elemento con el índice especificado.                                                             |
| [getNextSelectedItem](listbox-getnextselecteditem.md) | Recupera el siguiente elemento seleccionado en el control de cuadro de lista, empezando por el elemento que tiene el índice especificado. |
| [insertItem](listbox-insertitem.md)                   | Inserta el texto especificado en el índice especificado del control de cuadro de lista.                                            |
| [replaceItem](listbox-replaceitem.md)                 | Reemplaza el texto que se encuentra en el índice especificado por el texto especificado.                                                     |
| [setSelectedState](listbox-setselectedstate.md)       | Selecciona o anula la selección del elemento con el índice especificado.                                                               |
| [show](listbox-show.md)                               | Muestra el control.                                                                                                 |



 

> [!Note]  
> Este elemento requiere Windows Media Player para Windows XP o posterior.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




