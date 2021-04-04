---
title: Barra de desplazamiento (referencia de elementos de interfaz de usuario de MSAA)
description: Las barras de desplazamiento permiten a un usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionados. El nombre de la clase de ventana de una barra de desplazamiento es \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078313"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barra de desplazamiento (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **barra de desplazamiento** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **barra de desplazamiento** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Las barras de desplazamiento permiten a un usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionados. El nombre de la clase de ventana de una barra de desplazamiento es "SCROLLBAR".

El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si la barra de desplazamiento es vertical u horizontal, y en cuál de las siguientes partes de la barra de desplazamiento está siendo consultada por el cliente:

-   Barra de desplazamiento
-   Botón de flecha superior o derecha
-   Botón de flecha inferior o izquierda
-   Cuadro de desplazamiento (Thumb)
-   La región de página arriba o derecha
-   La región de Av Pág o la página izquierda

## <a name="iaccessible-methods"></a>Métodos IAccessible

Una barra de desplazamiento admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): el propio objeto de barra de desplazamiento y el control de desplazamiento no admiten el método **accDoDefaultAction** .

    En el caso de las demás partes de la barra de desplazamiento de una barra de desplazamiento vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje de [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) con *wParam* establecido en los valores siguientes.

    

    | Botón o región       | Vaule        |
    |---------------------|--------------|
    | Botón de flecha superior    | \_línea SB   |
    | Botón de flecha abajo | SB \_ LINEDOWN |
    | Subir región      | \_Re Pág de SB   |
    | Zona abajo    | reavpág SB \_ |

    

     

    Para las demás partes de la barra de desplazamiento en una barra de desplazamiento horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje de [**\_ HSCROLL de WM**](/windows/desktop/Controls/wm-hscroll) con *wParam* establecido en los valores siguientes.

    

    | Botón o región      | Value         |
    |--------------------|---------------|
    | Botón de flecha izquierda  | SB \_ LINELEFT  |
    | Botón de flecha a la derecha | SB \_ LINERIGHT |
    | Región izquierda de la página   | SB \_ PAGELEFT  |
    | Región derecha de la página  | SB \_ anclada |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Una barra de desplazamiento admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propiedad **ChildCount** del objeto de barra de desplazamiento es cinco. En el caso de las demás partes de la barra de desplazamiento, la propiedad **ChildCount** es cero.
-   [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): el propio objeto de barra de desplazamiento y el control de desplazamiento no admiten la propiedad **DEFAULTACTION** . La propiedad **DEFAULTACTION** de los botones de flecha y las áreas sombreadas situadas a cada lado del control de desplazamiento es "Press".
-   [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription): la propiedad **Description** depende de la parte de la barra de desplazamiento que se consulta.

    Las partes de una barra de desplazamiento vertical tienen las siguientes descripciones.

    

    | Parte                | Descripción                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barra de desplazamiento   | "Se usa para cambiar el área de visualización vertical"                                          |
    | Botón de flecha superior    | "Mueve la posición vertical una línea hacia arriba"                                           |
    | Botón de flecha abajo | "Mueve la posición vertical una línea hacia abajo"                                         |
    | Control de desplazamiento        | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente" |
    | Subir región      | "Mueve la posición vertical a un par de líneas"                                  |
    | Zona abajo    | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente" |

    

     

    Las partes de una barra de desplazamiento horizontal tienen las siguientes descripciones.

    

    | Parte               | Descripción                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barra de desplazamiento  | "Se usa para cambiar el área de visualización horizontal"                                          |
    | Botón de flecha izquierda  | "Mueve la posición horizontal una columna hacia la izquierda"                                       |
    | Botón de flecha a la derecha | ' Mueve la posición horizontal una columna hacia la derecha '                                      |
    | Control de desplazamiento       | "Indica la posición horizontal actual y se puede arrastrar para cambiarla directamente" |
    | Región izquierda de la página   | "Mueve la posición horizontal a la izquierda un par de columnas"                              |
    | Región derecha de la página  | "Indica la posición vertical actual y se puede arrastrar para cambiarla directamente"   |

    

     

-   [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propiedad **Name** depende de la parte de la barra de desplazamiento que se consulta.

    Los elementos de una barra de desplazamiento vertical tienen los nombres siguientes.

    | Parte                | Nombre        |
    |---------------------|-------------|
    | Ventana de barra de desplazamiento   | Vertical  |
    | Botón de flecha superior    | "Alinear"   |
    | Botón de flecha abajo | "Línea abajo" |
    | Control de desplazamiento        | Localización  |
    | Subir región      | "Re Pág"   |
    | Zona abajo    | "Av Pág" |

    

     

    Los elementos de una barra de desplazamiento horizontal tienen los nombres siguientes.

    

    | Parte               | Nombre           |
    |--------------------|----------------|
    | Ventana de barra de desplazamiento  | Horizontal   |
    | Botón de flecha izquierda  | "Columna izquierda"  |
    | Botón de flecha a la derecha | "Columna derecha" |
    | Control de desplazamiento       | Localización     |
    | Región derecha de la página  | "Página derecha"   |
    | Región izquierda de la página   | "Página izquierda"    |

    

     

-   [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propiedad **primaria** de los botones de flecha, el control de desplazamiento y el área sombreada de cualquier lado del control es la ventana de la barra de desplazamiento. La propiedad **primaria** de la ventana de la barra de desplazamiento es una ventana ( \_ ventana del sistema \_ de roles) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana.
-   [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad **role** depende de la parte de la barra de desplazamiento que se consulta. Las partes de una barra de desplazamiento tienen los siguientes roles. 

    | Parte                                                  | Role                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barra de desplazamiento                                     | [**\_barra de desplazamiento del sistema de roles \_**](object-roles.md)   |
    | Botones de flecha arriba, abajo, izquierda y derecha              | [**\_PUSHBUTTON del sistema de roles \_**](object-roles.md) |
    | Control de desplazamiento                                          | [**\_indicador del sistema de roles \_**](object-roles.md)   |
    | Subir página, Av Pág, Av Pág y las regiones de la página a la derecha | [**\_PUSHBUTTON del sistema de roles \_**](object-roles.md) |

    

     

-   [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propiedad **Estado** de cada componente de barra de desplazamiento incluye una combinación de los [valores](object-state-constants.md)siguientes.

    | Estado                                                                                 | Value                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**sistema de estado \_ \_ invisible**](object-state-constants.md)     | En la barra de desplazamiento, esto indica que la barra de desplazamiento vertical u horizontal especificada no existe. En el caso de las regiones Re Pág o Av Pág, esto indica que el control está colocado de forma que la región no exista. |
    | [**sistema de estado \_ \_ oculto**](object-state-constants.md)     | Para la barra de desplazamiento en sí, esto indica que la ventana tiene el mismo tamaño que la barra de desplazamiento vertical u horizontal especificada no se muestra actualmente.                                                                         |
    | [**sistema de estado \_ \_ presionado**](object-state-constants.md)         | Se presiona el botón de flecha o el área de la página.                                                                                                                                                                                 |
    | [**ESTADO \_ del sistema \_ no disponible**](object-state-constants.md) | El componente está deshabilitado.                                                                                                                                                                                                  |

    

     

-   [**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propiedad **valor** de la ventana de la barra de desplazamiento indica la posición de la barra de desplazamiento y es una cadena que contiene un entero de "0" a "100".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 