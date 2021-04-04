---
title: Control deslizante (referencia de elementos de interfaz de usuario de MSAA)
description: Un control deslizante, también denominado control TrackBar, permite a un usuario seleccionar un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076294"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Control deslizante (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control deslizante** para fines de referencia de elementos de interfaz de usuario de MSAA. Cómo crear objetos de **control deslizante** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un control deslizante, también denominado control TrackBar, permite a un usuario seleccionar un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.

El nombre de la clase de ventana de un control deslizante es TRACKBAR \_ (clase), que se define como "msctls \_ TRACKBAR" en commctrl. h.

El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si el control deslizante es vertical u horizontal y en el que el cliente consulta las siguientes partes del control deslizante:

-   Ventana de control deslizante
-   Control deslizante
-   Área sombreada por encima (o hasta
-   Área sombreada debajo (o a la derecha del control deslizante)

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control deslizante admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un control deslizante admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la propiedad **KeyboardShortcut** es la tecla de acceso de la ventana de control deslizante, que es un carácter subrayado en el texto de la etiqueta del control deslizante. La cadena devuelta contiene el carácter de tecla de acceso anexado a la cadena "Alt +".
-   [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propiedad **Name** depende de la parte del control deslizante que se consulta.

    Las partes de un control deslizante vertical tienen los nombres siguientes:

    

    | Elemento Slider                    | Nombre                                |
    |--------------------------------|-------------------------------------|
    | Ventana de control deslizante                  | Control de texto estático utilizado como etiqueta |
    | Control deslizante                   | Localización                          |
    | Área sombreada encima del control deslizante | "Re Pág"                           |
    | Área sombreada debajo del control deslizante | "Av Pág"                         |

    

     

    Las partes de un control deslizante horizontal tienen los nombres siguientes:

    

    | Elemento Slider                              | Nombre                                |
    |------------------------------------------|-------------------------------------|
    | Ventana de control deslizante                            | Control de texto estático utilizado como etiqueta |
    | Control deslizante                             | Localización                          |
    | Área sombreada a la izquierda de la miniatura del control deslizante  | "Página izquierda"                         |
    | Área sombreada a la derecha de la miniatura del control deslizante | "Página derecha"                        |

    

     

-   [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propiedad **primaria** de los botones de flecha, el control de desplazamiento y el área sombreada de cualquier lado del control es la ventana de control deslizante. La propiedad **primaria** de la ventana de control deslizante es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana.
-   [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad **role** depende de la parte del control deslizante que se consulta. 

    | Elemento Slider                                     | [Rol](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Ventana de control deslizante                                   | [**\_control deslizante del sistema de roles \_**](object-roles.md)         |
    | Control deslizante                                    | [**\_indicador del sistema de roles \_**](object-roles.md)   |
    | Áreas sombreadas en cualquier lado del control deslizante | [**\_PUSHBUTTON del sistema de roles \_**](object-roles.md) |

    

     

-   [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate):[los valores](object-state-constants.md) de la propiedad **State** dependen de la parte del control deslizante que se consulta. 

    | Elemento Slider                                     | Valores de estado posibles                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana de control deslizante                                   | [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocable**](object-state-constants.md) del sistema estado de \| [**\_ \_ enfoque**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) |
    | Control deslizante                                    | Cero (0), lo que significa que el objeto está visible o el sistema de [**estado \_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) del sistema                                                                                                                       |
    | Áreas sombreadas en cualquier lado del control deslizante | Cero (0), lo que significa que el objeto está visible o el sistema de [**estado \_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) del sistema                                                                                                                       |

    

     

-   [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propiedad **Value** de la ventana de control deslizante indica la posición del control Thumb y es una cadena que contiene un entero de "0" a "100".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de desplazamiento**](scroll-bar.md)
</dt> </dl>

 

 




