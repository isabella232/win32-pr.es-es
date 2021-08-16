---
title: Control deslizante (Referencia del elemento de interfaz de usuario de MSAA)
description: Un control deslizante, también denominado control de barra de seguimiento, permite al usuario seleccionar entre un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d92799a8a644d5e5e00c695d628cb827ba60f73cc3a0d7b7f5dc505a6c2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564433"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Control deslizante (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos control deslizante** para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **control deslizante** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control deslizante, también denominado control de barra de seguimiento, permite al usuario seleccionar entre un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.

El nombre de clase de ventana de un control deslizante es TRACKBAR CLASS, que se define como \_ "msctls \_ trackbar" en Commctrl.h.

El contenido de las [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si el control deslizante es vertical u horizontal y de cuál de las siguientes partes del control deslizante consulta el cliente:

-   Ventana control deslizante
-   Control deslizante
-   Área sombreada por encima de (o para
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
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la propiedad **KeyboardShortcut** es la tecla de acceso de la ventana deslizante, que es un carácter subrayado en el texto de la etiqueta del control deslizante. La cadena devuelta contiene el carácter de clave de acceso anexado a la cadena "Alt+".
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la **propiedad Name** depende de la parte del control deslizante que se consulta.

    Las partes de un control deslizante vertical tienen los nombres siguientes:

    

    | Elemento de control deslizante                    | Nombre                                |
    |--------------------------------|-------------------------------------|
    | Ventana control deslizante                  | Control de texto estático usado como etiqueta |
    | Control deslizante                   | "Position"                          |
    | Área sombreada sobre el control deslizante | "Página anterior"                           |
    | Área sombreada debajo del control deslizante | "Página siguiente"                         |

    

     

    Las partes de un control deslizante horizontal tienen los nombres siguientes:

    

    | Elemento de control deslizante                              | Nombre                                |
    |------------------------------------------|-------------------------------------|
    | Ventana control deslizante                            | Control de texto estático usado como etiqueta |
    | Control deslizante                             | "Position"                          |
    | Área sombreada a la izquierda del control deslizante  | "Página izquierda"                         |
    | Área sombreada a la derecha del control deslizante | "Derecho de página"                        |

    

     

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la propiedad **Parent** de los botones de flecha, el control de desplazamiento y el área sombreada a ambos lados del control es la ventana deslizante. La **propiedad Parent** de la ventana deslizante es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la **propiedad Role** depende de la parte del control deslizante que se consulta. 

    | Elemento de control deslizante                                     | [Rol](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Ventana control deslizante                                   | [**CONTROL DESLIZANTE \_ DEL SISTEMA \_ DE ROLES**](object-roles.md)         |
    | Control deslizante                                    | [**INDICADOR \_ DEL SISTEMA DE \_ ROL**](object-roles.md)   |
    | Áreas sombreadas a cada lado del control deslizante | [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md) |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)[los valores](object-state-constants.md) de la propiedad **State** dependen de la parte del control deslizante que se consulta. 

    | Elemento de control deslizante                                     | Valores de estado posibles                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana control deslizante                                   | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) DEL SISTEMA DE ESTADO NO \| [**\_ \_ DISPONIBLE**](object-state-constants.md) SISTEMA DE ESTADO \| [**\_ \_ ENFOCADO**](object-state-constants.md) SISTEMA DE ESTADO \| [**ENFOCADO \_ \_ NORMAL**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) DEL SISTEMA DE ESTADO ENFOCADO |
    | Control deslizante                                    | Cero (0), lo que significa que el objeto está visible, o SISTEMA DE ESTADO [**\_ \_ INVISIBLE**](object-state-constants.md) SISTEMA DE ESTADO NO DISPONIBLE \| [**\_ \_ SISTEMA**](object-state-constants.md) \| [**DE ESTADO \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |
    | Áreas sombreadas a cada lado del control deslizante | Cero (0), lo que significa que el objeto está visible, o SISTEMA DE ESTADO [**\_ \_ INVISIBLE**](object-state-constants.md) SISTEMA DE ESTADO NO DISPONIBLE \| [**\_ \_ SISTEMA**](object-state-constants.md) \| [**DE ESTADO \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propiedad **Value** de la ventana deslizante indica la posición del control thumb y es una cadena que contiene un entero de "0" a "100".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de desplazamiento**](scroll-bar.md)
</dt> </dl>

 

 




