---
title: Barra de desplazamiento (Referencia del elemento de la interfaz de usuario de MSAA)
description: Las barras de desplazamiento permiten al usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionado. El nombre de clase de ventana de una barra de desplazamiento es \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070636"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra de desplazamiento (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos De barra** de desplazamiento para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de barra de** desplazamiento en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Las barras de desplazamiento permiten al usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionado. El nombre de clase de ventana de una barra de desplazamiento es "SCROLLBAR".

El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si la barra de desplazamiento es vertical u horizontal y de cuál de las siguientes partes de la barra de desplazamiento está consultando el cliente:

-   La propia barra de desplazamiento
-   Botón de flecha superior o derecha
-   Botón de flecha inferior o izquierda
-   El cuadro de desplazamiento (thumb)
-   Región derecha de página arriba o página
-   Región izquierda de la página o hacia abajo

## <a name="iaccessible-methods"></a>Métodos IAccessible

Una barra de desplazamiento admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): el propio objeto de barra de desplazamiento y el control de desplazamiento no admiten **el método accDoDefaultAction.**

    Para las demás partes de la barra de desplazamiento de una barra de desplazamiento vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje [**\_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) de WM con *wParam* establecido en los valores siguientes.

    

    | Botón o región       | Vaule        |
    |---------------------|--------------|
    | Botón de flecha superior    | SB \_ LINEUP   |
    | Botón de flecha inferior | SB \_ LINEDOWN |
    | Página anterior región      | PÁGINA \_ DE SB   |
    | Página siguiente región    | SB \_ PAGEDOWN |

    

     

    Para las demás partes de la barra de desplazamiento de una barra de desplazamiento horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) con *wParam* establecido en los valores siguientes.

    

    | Botón o región      | Value         |
    |--------------------|---------------|
    | Botón de flecha izquierda  | SB \_ LINELEFT  |
    | Botón de flecha a la derecha | SB \_ LINERIGHT |
    | Región izquierda de la página   | SB \_ PAGELEFT  |
    | Región derecha de página  | SB \_ PAGERIGHT |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Una barra de desplazamiento admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la **propiedad ChildCount** del objeto de barra de desplazamiento es cinco. Para las demás partes de la barra de desplazamiento, **la propiedad ChildCount** es cero.
-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): el propio objeto de barra de desplazamiento y el control thumb de desplazamiento no admiten **la propiedad DefaultAction.** La **propiedad DefaultAction** para los botones de flecha y las áreas sombreadas a cada lado del control de desplazamiento es "Press".
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription): la **propiedad Description** depende de la parte de la barra de desplazamiento que se consulta.

    Las partes de una barra de desplazamiento vertical tienen las descripciones siguientes.

    

    | Parte                | Descripción                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra de desplazamiento en sí   | "Se usa para cambiar el área de visualización vertical"                                          |
    | Botón de flecha superior    | "Mueve la posición vertical hacia arriba una línea"                                           |
    | Botón de flecha inferior | "Mueve la posición vertical hacia abajo una línea"                                         |
    | Desplazamiento de la posición        | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente" |
    | Página anterior región      | "Mueve la posición vertical hacia arriba un par de líneas"                                  |
    | Página siguiente región    | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente" |

    

     

    Las partes de una barra de desplazamiento horizontal tienen las descripciones siguientes.

    

    | Parte               | Descripción                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra de desplazamiento en sí  | "Se usa para cambiar el área de visualización horizontal"                                          |
    | Botón de flecha izquierda  | "Mueve la posición horizontal a la izquierda de una columna"                                       |
    | Botón de flecha a la derecha | "Mueve la posición horizontal a la derecha de una columna"                                      |
    | Desplazamiento de la posición       | "Indica la posición horizontal actual y se puede arrastrar para cambiarla directamente" |
    | Región izquierda de la página   | "Mueve la posición horizontal a la izquierda de un par de columnas"                              |
    | Región derecha de página  | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente"   |

    

     

-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la **propiedad Name** depende de la parte de la barra de desplazamiento que se consulta.

    Las partes de una barra de desplazamiento vertical tienen los nombres siguientes.

    | Parte                | Nombre        |
    |---------------------|-------------|
    | Ventana barra de desplazamiento   | "Vertical"  |
    | Botón de flecha superior    | "Alineación"   |
    | Botón de flecha inferior | "Línea hacia abajo" |
    | Desplazamiento de la posición        | "Position"  |
    | Página anterior región      | "Página anterior"   |
    | Página siguiente región    | "Página siguiente" |

    

     

    Las partes de una barra de desplazamiento horizontal tienen los nombres siguientes.

    

    | Parte               | Nombre           |
    |--------------------|----------------|
    | Ventana barra de desplazamiento  | "Horizontal"   |
    | Botón de flecha izquierda  | "Columna izquierda"  |
    | Botón de flecha a la derecha | "Derecho de columna" |
    | Desplazamiento de la posición       | "Position"     |
    | Región derecha de página  | "Derecho de página"   |
    | Región izquierda de la página   | "Página izquierda"    |

    

     

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)la propiedad **Parent** de los botones de flecha, el control de desplazamiento y el área sombreada a cada lado del control es la ventana de la barra de desplazamiento. La **propiedad Parent** de la ventana de la barra de desplazamiento es una ventana (ROLE SYSTEM WINDOW) que rodea el control y tiene la misma propiedad Name y el mismo nombre de clase de \_ \_ ventana. 
-   [**get \_ accRole:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)la **propiedad Role** depende de la parte de la barra de desplazamiento que se consulta. Las partes de una barra de desplazamiento tienen los roles siguientes. 

    | Parte                                                  | Role                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barra de desplazamiento propiamente dicha                                     | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md)   |
    | Botones de flecha arriba, abajo, izquierda y derecha              | [**BOTÓN \_ PUSHBUTTON \_ DEL SISTEMA DE ROL**](object-roles.md) |
    | Desplazamiento de la posición                                          | [**INDICADOR \_ DEL SISTEMA DE \_ ROL**](object-roles.md)   |
    | Página anterior, abajo, página izquierda y región derecha de página | [**BOTÓN \_ PUSHBUTTON \_ DEL SISTEMA DE ROL**](object-roles.md) |

    

     

-   [**get \_ accState:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)la **propiedad State** de cada componente de barra de desplazamiento incluye una combinación de los valores [siguientes.](object-state-constants.md)

    | Estado                                                                                 | Value                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**SISTEMA \_ DE ESTADO \_ INVISIBLE**](object-state-constants.md)     | Para la propia barra de desplazamiento, indica que la barra de desplazamiento vertical u horizontal especificada no existe. En el caso de las regiones de página arriba o abajo, esto indica que el control de posición es tal que la región no existe. |
    | [**STATE \_ SYSTEM \_ OFFSCREEN**](object-state-constants.md)     | Para la propia barra de desplazamiento, esto indica que el tamaño de la ventana es tal que la barra de desplazamiento vertical u horizontal especificada no se muestra actualmente.                                                                         |
    | [**SISTEMA \_ DE \_ ESTADO PRESIONADO**](object-state-constants.md)         | Se presiona el botón de flecha o la región de la página.                                                                                                                                                                                 |
    | [**SISTEMA \_ DE ESTADO NO \_ DISPONIBLE**](object-state-constants.md) | El componente está deshabilitado.                                                                                                                                                                                                  |

    

     

-   [**get \_ accValue:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)la propiedad **Value** de la ventana de la barra de desplazamiento indica la posición de la barra de desplazamiento y es una cadena que contiene un entero de "0" a "100".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 