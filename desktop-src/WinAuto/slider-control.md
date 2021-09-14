---
title: Control Deslizante (Referencia del elemento de la interfaz de usuario de MSAA)
description: Un control deslizante, también denominado control de barra de seguimiento, permite a un usuario seleccionar entre un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070619"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Control Deslizante (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos control deslizante** para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe **cómo crear objetos de control** deslizante en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control deslizante, también denominado control de barra de seguimiento, permite a un usuario seleccionar entre un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.

El nombre de clase de ventana de un control deslizante es TRACKBAR CLASS, que se define como \_ "msctls \_ trackbar" en Commctrl.h.

El contenido de las [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si el control deslizante es vertical u horizontal y de cuál de las siguientes partes del control deslizante consulta el cliente:

-   Ventana deslizante
-   Control deslizante
-   Área sombreada por encima (o a)
-   Área sombreada debajo (o a la derecha de) el control deslizante

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control deslizante admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un control deslizante admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)la propiedad **KeyboardShortcut** es la tecla de acceso de la ventana deslizante, que es un carácter subrayado en el texto de la etiqueta del control deslizante. La cadena devuelta contiene el carácter de clave de acceso anexado a la cadena "Alt+".
-   [**get \_ accName:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)la **propiedad Name** depende de la parte del control deslizante que se consulta.

    Las partes de un control deslizante vertical tienen los nombres siguientes:

    

    | Parte del control deslizante                    | Nombre                                |
    |--------------------------------|-------------------------------------|
    | Ventana deslizante                  | Control de texto estático usado como etiqueta |
    | Control deslizante                   | "Position"                          |
    | Área sombreada sobre el control deslizante | "Página anterior"                           |
    | Área sombreada debajo del control deslizante | "Página siguiente"                         |

    

     

    Las partes de un control deslizante horizontal tienen los nombres siguientes:

    

    | Parte del control deslizante                              | Nombre                                |
    |------------------------------------------|-------------------------------------|
    | Ventana deslizante                            | Control de texto estático usado como etiqueta |
    | Control deslizante                             | "Position"                          |
    | Área sombreada a la izquierda del control deslizante  | "Página izquierda"                         |
    | Área sombreada a la derecha del control deslizante | "Derecho de página"                        |

    

     

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la propiedad **Parent** de los botones de flecha, el control de desplazamiento y el área sombreada a cada lado del control es la ventana deslizante. La **propiedad Parent** de la ventana deslizante es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana.
-   [**get \_ accRole:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)la **propiedad Role** depende de la parte del control deslizante que se consulta. 

    | Parte del control deslizante                                     | [Rol](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Ventana deslizante                                   | [**CONTROL DESLIZANTE \_ DEL SISTEMA \_ DE ROLES**](object-roles.md)         |
    | Control deslizante                                    | [**INDICADOR \_ DEL SISTEMA DE \_ ROL**](object-roles.md)   |
    | Áreas sombreadas a cada lado del control deslizante | [**BOTÓN \_ PUSHBUTTON \_ DEL SISTEMA DE ROL**](object-roles.md) |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)[los valores](object-state-constants.md) de la propiedad **State** dependen de la parte del control deslizante que se consulta. 

    | Parte del control deslizante                                     | Valores de estado posibles                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana deslizante                                   | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) DEL SISTEMA DE ESTADO NO \| [**\_ \_ DISPONIBLE**](object-state-constants.md) \| [**SISTEMA \_ \_ DE**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) ESTADO CENTRADO SISTEMA DE ESTADO ENFOCADO SISTEMA DE ESTADO NORMAL |
    | Control deslizante                                    | Cero (0), lo que significa que el objeto está visible, o SISTEMA DE ESTADO [**\_ \_ INVISIBLE**](object-state-constants.md) SISTEMA DE ESTADO \| [**\_ NO \_ DISPONIBLE**](object-state-constants.md) \| [**SISTEMA DE ESTADO \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |
    | Áreas sombreadas a cada lado del control deslizante | Cero (0), lo que significa que el objeto está visible, o SISTEMA DE ESTADO [**\_ \_ INVISIBLE**](object-state-constants.md) SISTEMA DE ESTADO \| [**\_ NO \_ DISPONIBLE**](object-state-constants.md) \| [**SISTEMA DE ESTADO \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get \_ accValue:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)la propiedad **Value** de la ventana deslizante indica la posición del control y es una cadena que contiene un entero de "0" a "100".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de desplazamiento**](scroll-bar.md)
</dt> </dl>

 

 




