---
title: Cuadro combinado (Referencia del elemento de la interfaz de usuario de MSAA)
description: Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3a8d26fa5b8cb264c06e7aa64c672e0a80e8ada7e90a152b3b941ea207cade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071845"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Cuadro combinado (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de cuadro** combinado para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe **cómo crear objetos de cuadro** combinado en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado. La parte del cuadro de lista del control se muestra en todo momento o solo en la lista desplegable cuando el usuario selecciona la flecha desplegable (que es un botón de inserción) junto al control. Si el campo de selección es un control de edición, el usuario puede escribir información que no esté en la lista. De lo contrario, el usuario solo puede seleccionar elementos de la lista.

El nombre de clase de ventana de un cuadro combinado es "COMBOBOX".

El contenido de las [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de cuál de las siguientes partes del cuadro combinado consulta el cliente:

-   Ventana del cuadro combinado
-   Control de edición o control de texto estático
-   La flecha desplegable (que es un botón de inserción)
-   El cuadro de lista
-   Elementos de lista del cuadro de lista

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los cuadros combinados admiten los [**siguientes métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los cuadros combinados admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)en la tabla siguiente se muestra el valor de recuento secundario de las distintas partes del cuadro combinado. 

    | Parte del cuadro combinado   | ChildCount               |
    |------------------|--------------------------|
    | Ventana cuadro combinado | 3                        |
    | Edit (control)     | 0                        |
    | Flecha desplegable  | 0                        |
    | Cuadro de lista         | Número de elementos de lista |
    | Elemento de lista        | 0                        |

    

     

-   [**get \_ accDefaultAction:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)en la tabla siguiente se muestra **la propiedad DefaultAction** para diferentes partes de un cuadro combinado. 

    | Parte del cuadro combinado   | DefaultAction                                                  |
    |------------------|----------------------------------------------------------------|
    | Ventana cuadro combinado | Ninguno                                                           |
    | Edit (control)     | Ninguno                                                           |
    | Flecha desplegable  | "Abrir" o "Cerrar" en función del estado de la lista desplegable |
    | Cuadro de lista         | Ninguno                                                           |
    | Elemento de lista        | "Doble clic"                                                 |

    

     

-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)en la tabla siguiente se muestra la **propiedad KeyboardShortcut** para distintas partes de un cuadro combinado. 

    | Parte del cuadro combinado   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Ventana cuadro combinado | Clave de acceso de la etiqueta asociada |
    | Edit (control)     | Ninguno                           |
    | Flecha desplegable  | "Alt+Flecha abajo"               |
    | Cuadro de lista         | Ninguno                           |
    | Elemento de lista        | Ninguno                           |

    

     

    La clave de acceso de un cuadro combinado es el carácter subrayado en el texto de un control de texto estático asociado que etiqueta el cuadro combinado. Por ejemplo, en un cuadro de diálogo Estándar Abrir que abre archivos, como en Microsoft WordPad, el cuadro combinado con la etiqueta "Files of type:" (Archivos de tipo:) tiene **keyboardShortcut** "Alt+t".

-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): en la tabla siguiente se muestra **la propiedad Name** para las distintas partes de un cuadro combinado. 

    | Parte del cuadro combinado   | Nombre                                                           |
    |------------------|----------------------------------------------------------------|
    | Ventana cuadro combinado | Control de texto estático usado como etiqueta                            |
    | Edit (control)     | Control de texto estático usado como etiqueta                            |
    | Flecha desplegable  | "Abrir" o "Cerrar" en función del estado de la lista desplegable |
    | Cuadro de lista         | Etiqueta asociada                                               |
    | Elemento de lista        | Texto del elemento de lista                                          |

    

     

    La **propiedad Name** de un cuadro combinado, su control de edición secundario y su cuadro de lista secundario es el texto de un control de texto estático asociado que etiqueta el cuadro combinado. Por ejemplo, en un cuadro de diálogo Estándar Abrir que  abre archivos, como en WordPad, las propiedades Nombre de los dos cuadros combinados son "Buscar en:" y "Archivos de tipo:".

-   [**get \_ accParent:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)en la tabla siguiente se muestra el valor primario de las distintas partes de un cuadro combinado. 

    | Parte del cuadro combinado                        | Parent                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana cuadro combinado                      | Ventana con la **propiedad Role** de ROLE [**SYSTEM \_ \_ WINDOW**](object-roles.md) que rodea el cuadro combinado y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el cuadro combinado. |
    | Editar control (o control de texto estático) | Ventana del cuadro combinado.                                                                                                                                                                                          |
    | Flecha desplegable                       | Ventana del cuadro combinado.                                                                                                                                                                                          |
    | Ventana primaria del cuadro de lista                | Ventana del cuadro combinado. Esta ventana rodea el cuadro de lista.                                                                                                                                                      |
    | Cuadro de lista                              | Ventana primaria del cuadro de lista.                                                                                                                                                                                    |
    | Elemento de lista                             | Cuadro de lista.                                                                                                                                                                                                  |

    

     

-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): en la tabla siguiente se muestra **la propiedad Role** para diferentes partes de un cuadro combinado. 

    | Elemento de cuadro combinado                        | [Rol](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana cuadro combinado                      | [**CUADRO \_ COMBINADO DEL SISTEMA DE \_ ROLES**](object-roles.md)                                                                    |
    | Editar control (o control de texto estático) | [**ROLE \_ TEXTO \_ DEL SISTEMA**](object-roles.md) O TEXTO ESTÁTICO DEL SISTEMA DE [ **\_ \_ ROLES**](object-roles.md) |
    | Flecha de lista desplegable                       | [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md)                                                                |
    | Cuadro de lista                              | [**LISTA \_ DEL SISTEMA DE \_ ROLES**](object-roles.md)                                                                            |
    | Elemento de lista                             | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)                                                                    |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): en la tabla siguiente se muestra **la propiedad State** para diferentes partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | [Estados posibles](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Ventana cuadro combinado | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) DEL SISTEMA DE ESTADO \| [**\_ \_ NO**](object-state-constants.md) DISPONIBLE \| [**\_ \_ SISTEMA**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) DE ESTADO CENTRADO SISTEMA DE ESTADO ENFOCADO SISTEMA DE ESTADO NORMAL SISTEMA DE ESTADO NORMAL SISTEMA DE ESTADO EXPANDIDO CONTRAÍDO |
    | Edit (control)     | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) DEL SISTEMA DE ESTADO NO \| [**\_ \_ DISPONIBLE**](object-state-constants.md) SISTEMA DE ESTADO \| [**\_ \_ ENFOCADO**](object-state-constants.md) SISTEMA DE ESTADO \| [**ENFOCADO \_ \_ NORMAL**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) DEL SISTEMA DE ESTADO ENFOCADO                                                                                                                                                                         |
    | Flecha de lista desplegable  | 0, lo que significa que el botón está visible y no presionado; o [**STATE \_ SYSTEM \_ PRESSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| STATE SYSTEM \_ \_ NORMAL                                                                                                                                                                                                                                                                                                                                                    |
    | Cuadro de lista         | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) DEL SISTEMA DE ESTADO NO \| [**\_ \_ DISPONIBLE**](object-state-constants.md) SISTEMA \| [**\_ \_ DE**](object-state-constants.md) ESTADO ENFOCADO SISTEMA DE ESTADO ENFOCADO SISTEMA \| [**\_ \_ DE**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) ESTADO FLOTANTE DEL SISTEMA NORMAL                                                                                      |
    | Elemento de lista        | [**STATE \_ SISTEMA \_ DE ESTADO INVISIBLE**](object-state-constants.md) SISTEMA DE ESTADO ENFOCADO SISTEMA DE ESTADO ENFOCADO SISTEMA DE ESTADO \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ SELECCIONABLE**](object-state-constants.md) \| [**SISTEMA DE ESTADO SELECCIONADO \_ SISTEMA \_ DE**](object-state-constants.md) \| [**ESTADO SELECCIONADO NORMAL DEL SISTEMA \_ DE \_ ESTADO**](object-state-constants.md)                                                                                        |

    

     

-   [**get \_ accValue :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)en la tabla siguiente se muestra la propiedad **Value** para diferentes partes de un cuadro combinado. 

    | Elemento de cuadro combinado   | Valor                                |
    |------------------|--------------------------------------|
    | Ventana cuadro combinado | Texto del elemento de lista seleccionado actualmente |
    | Edit (control)     | Texto del elemento de lista seleccionado actualmente |
    | Flecha de lista desplegable  | Ninguno                                 |
    | Cuadro de lista         | Ninguno                                 |
    | Elemento de lista        | Ninguno                                 |

    

     

## <a name="notes"></a>Notas

-   Cuando se llama a [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) con la marca [**NAVDIR \_ NEXT**](navigation-constants.md) en la parte del cuadro de lista de un cuadro combinado, navega incorrectamente a la ventana de bandeja cuando debe devolver **VT \_ EMPTY**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




