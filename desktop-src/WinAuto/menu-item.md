---
title: Elemento de menú (Referencia del elemento de interfaz de usuario de MSAA)
description: Un elemento de menú representa un elemento determinado en una barra de menús o un menú emergente.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b90162f386314ac495ed138ccf4d180d2f53b8b1e6126287c79a1d75d40be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644505"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Elemento de menú (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de elemento** de menú para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo crear objetos **de elemento** de menú en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un elemento de menú representa un elemento determinado en una barra de menús o un menú emergente. Por ejemplo, Microsoft Active Accessibility un objeto de elemento de menú para el **menú** Archivo en la barra de menús. De forma similar, Microsoft Active Accessibility un objeto de elemento de menú para el **elemento** de menú Abrir desde **el** menú emergente Archivo.

El nombre de clase de ventana de un elemento de menú es \# "32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un elemento de menú admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Para los elementos de menú de la barra de menús, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) muestra o cierra el menú en función del estado del menú. Para los elementos de menú de un menú emergente, **accDoDefaultAction** hace clic en el elemento de menú para ejecutar el comando de menú. |
| [**attest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un elemento de menú admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera la interfaz [**IDispatch**](idispatch-interface.md) en el objeto de menú emergente de este elemento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es una para los elementos de menú que muestran un menú o submenú; De lo **contrario, la propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **propiedad DefaultAction** para los elementos de menú que muestran un menú o submenú es "Abrir" o "Cerrar" en función del estado del menú. La **propiedad DefaultAction** para todos los demás elementos de menú es "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del elemento de menú, que es el carácter subrayado en el texto del nombre del elemento de menú. Por ejemplo, la **propiedad KeyboardShortcut** del elemento de menúFile es "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad** Name es la misma que el nombre del elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad** Parent es la barra de menús o el menú emergente que contiene el elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ MENUITEM**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) o una combinación de uno o varios de los valores siguientes: [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ CHECKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ DEFAULT**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ HOTTRACKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

-   Cuando se usa en un elemento de menú, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) devuelve S OK, pero no puede realizar la acción si el carácter usado en la clave de acceso es ?, !, @, o cualquier otro carácter que requiera la tecla MAYÚS u otra tecla \_ modificadora. Esto también sucede en teclados internacionales con un carácter de tecla de acceso que requiere que se presione la tecla ALT GR.
-   El [**método accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con [**SELFACTIVE \_ TAKEFOCUS**](selflag.md) no hace que un elemento de menú abra o cierre un menú emergente. Los clientes usan [**el método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para abrir o cerrar un menú emergente.
-   Un elemento de barra de menús que no muestra  un menú emergente devuelve "Aplicación" para la propiedad Nombre en lugar del nombre del elemento de menú.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menús**](menu-bar.md)
</dt> <dt>

[**Menú emergente**](pop-up-menu.md)
</dt> </dl>

 

 





