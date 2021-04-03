---
title: Cuadro combinado (referencia de elementos de interfaz de usuario de MSAA)
description: Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776633"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Cuadro combinado (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **cuadro combinado** para fines de referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **cuadro combinado** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado. La parte del cuadro de lista del control se muestra en todo momento o solo cuando el usuario selecciona la flecha de lista desplegable (que es un botón de control) junto al control. Si el campo de selección es un control de edición, el usuario puede escribir información que no esté en la lista. de lo contrario, el usuario solo puede seleccionar los elementos de la lista.

El nombre de clase de ventana de un cuadro combinado es "COMBOBOX".

El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de cuál de las siguientes partes del cuadro combinado consulta el cliente:

-   Ventana de cuadro combinado
-   Control de edición o control de texto estático
-   La flecha de lista desplegable (que es un botón de tecla)
-   Cuadro de lista
-   Los elementos de lista del cuadro de lista

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los cuadros combinados admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los cuadros combinados admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): en la tabla siguiente se muestra el valor de recuento secundario para las distintas partes del cuadro combinado. 

    | Elemento de cuadro combinado   | ChildCount               |
    |------------------|--------------------------|
    | Ventana de cuadro combinado | 3                        |
    | Edit (control)     | 0                        |
    | Flecha desplegable  | 0                        |
    | Cuadro de lista         | El número de elementos de lista |
    | Elemento de lista        | 0                        |

    

     

-   [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): en la tabla siguiente se muestra la propiedad **DEFAULTACTION** para las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | DefaultAction                                                  |
    |------------------|----------------------------------------------------------------|
    | Ventana de cuadro combinado | None                                                           |
    | Edit (control)     | None                                                           |
    | Flecha desplegable  | "Abrir" o "cerrar" según el estado de la lista desplegable |
    | Cuadro de lista         | None                                                           |
    | Elemento de lista        | "Doble clic"                                                 |

    

     

-   [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): en la tabla siguiente se muestra la propiedad **KeyboardShortcut** para las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Ventana de cuadro combinado | Clave de acceso de la etiqueta asociada |
    | Edit (control)     | None                           |
    | Flecha desplegable  | "Alt + flecha abajo"               |
    | Cuadro de lista         | None                           |
    | Elemento de lista        | None                           |

    

     

    La tecla de acceso de un cuadro combinado es el carácter subrayado en el texto de un control de texto estático asociado que etiqueta el cuadro combinado. Por ejemplo, en un cuadro de diálogo Abrir estándar que abre archivos, como en Microsoft WordPad, el cuadro combinado con la etiqueta "files of Type:" tiene el **KeyboardShortcut** "alt + t".

-   [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): en la tabla siguiente se muestra la propiedad **nombre** para las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | Nombre                                                           |
    |------------------|----------------------------------------------------------------|
    | Ventana de cuadro combinado | Control de texto estático utilizado como etiqueta                            |
    | Edit (control)     | Control de texto estático utilizado como etiqueta                            |
    | Flecha desplegable  | "Abrir" o "cerrar" según el estado de la lista desplegable |
    | Cuadro de lista         | Etiqueta asociada                                               |
    | Elemento de lista        | Texto del elemento de lista                                          |

    

     

    La propiedad **nombre** de un cuadro combinado, su control de edición secundario y su cuadro de lista secundario es el texto de un control de texto estático asociado que etiqueta el cuadro combinado. Por ejemplo, en un cuadro de diálogo Abrir estándar que abre archivos, como en WordPad, las propiedades de **nombre** de los dos cuadros combinados son "Buscar en" y "archivos de tipo:".

-   [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): en la tabla siguiente se muestra el valor primario de las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado                        | Parent                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana de cuadro combinado                      | Ventana con la propiedad **role** de la [**\_ \_ ventana del sistema de roles**](object-roles.md) que rodea el cuadro combinado y tiene la misma propiedad **nombre** y el nombre de clase de ventana que el cuadro combinado. |
    | Control de edición (o control de texto estático) | Ventana del cuadro combinado.                                                                                                                                                                                          |
    | Flecha desplegable                       | Ventana del cuadro combinado.                                                                                                                                                                                          |
    | Ventana primaria del cuadro de lista                | Ventana del cuadro combinado. Esta ventana rodea el cuadro de lista.                                                                                                                                                      |
    | Cuadro de lista                              | Ventana primaria del cuadro de lista.                                                                                                                                                                                    |
    | Elemento de lista                             | Cuadro de lista.                                                                                                                                                                                                  |

    

     

-   [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): en la tabla siguiente se muestra la propiedad de **rol** para las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado                        | [Rol](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana de cuadro combinado                      | [**\_cuadro combinado de sistema de roles \_**](object-roles.md)                                                                    |
    | Control de edición (o control de texto estático) | [**Rol \_ de \_**](object-roles.md) [ **\_ \_ STATICTEXT** de sistema de rol o texto del sistema](object-roles.md) |
    | Flecha desplegable                       | [**\_PUSHBUTTON del sistema de roles \_**](object-roles.md)                                                                |
    | Cuadro de lista                              | [**\_lista de sistema de roles \_**](object-roles.md)                                                                            |
    | Elemento de lista                             | [**\_ListItem del sistema de roles \_**](object-roles.md)                                                                    |

    

     

-   [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): en la tabla siguiente se muestra la propiedad **Estado** de distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | [Estados posibles](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana de cuadro combinado | [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocable**](object-state-constants.md) del \| [**\_ \_**](object-state-constants.md) sistema \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) de estado sistema de estado normal del sistema de estado expandido sistema de estado ampliado |
    | Edit (control)     | [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocable**](object-state-constants.md) del sistema estado de \| [**\_ \_ enfoque**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                                                                         |
    | Flecha desplegable  | 0, que significa que el botón está visible y no presionado; o [**sistema de estado invisible sistema \_ de estado \_**](object-state-constants.md) \| [**\_ \_ invisible**](object-state-constants.md) sistema de estado \| \_ \_ normal                                                                                                                                                                                                                                                                                                                                                    |
    | Cuadro de lista         | [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocable**](object-state-constants.md) al sistema de estado flotante sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ flotante**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                      |
    | Elemento de lista        | [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ enfocable**](object-state-constants.md) del sistema de estado \| [**seleccionado \_ \_**](object-state-constants.md) del sistema estado seleccionado sistema estado \| [**\_ \_ seleccionado**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                        |

    

     

-   [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): en la tabla siguiente se muestra la propiedad **Value** para las distintas partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | Value                                |
    |------------------|--------------------------------------|
    | Ventana de cuadro combinado | Texto del elemento de lista seleccionado actualmente |
    | Edit (control)     | Texto del elemento de lista seleccionado actualmente |
    | Flecha desplegable  | None                                 |
    | Cuadro de lista         | None                                 |
    | Elemento de lista        | None                                 |

    

     

## <a name="notes"></a>Notas

-   Cuando se llama a [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) con la marca de [**NAVDIR \_ siguiente**](navigation-constants.md) en la parte del cuadro de lista de un cuadro combinado, navega incorrectamente a la ventana de bandeja cuando debe devolver **VT \_ vacío**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




