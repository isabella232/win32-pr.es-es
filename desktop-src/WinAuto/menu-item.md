---
title: Elemento de menú (referencia de elementos de interfaz de usuario de MSAA)
description: Un elemento de menú representa un elemento determinado en una barra de menús o menú emergente.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb6621a14927cc4dc9af9f3384157e60ce6570d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075924"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Elemento de menú (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **elemento de menú** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **elemento de menú** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un elemento de menú representa un elemento determinado en una barra de menús o menú emergente. Por ejemplo, Microsoft Active Accessibility crea un objeto de elemento de menú para el menú **archivo** en la barra de menús. De forma similar, Microsoft Active Accessibility crea un objeto de elemento de menú para el elemento de menú **abrir** en el menú emergente **archivo** .

El nombre de clase de ventana para un elemento de menú es " \# 32768".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un elemento de menú admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | En el caso de los elementos de menú de la barra de menús, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) muestra o cierra el menú en función del estado del menú. En el caso de los elementos de menú de un menú emergente, **accDoDefaultAction** hace clic en el elemento de menú para ejecutar el comando de menú. |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un elemento de menú admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera la interfaz [**IDispatch**](idispatch-interface.md) en el objeto de menú emergente para este elemento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es una para los elementos de menú que muestran un menú o un submenú; de lo contrario, la propiedad **ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propiedad **DEFAULTACTION** para los elementos de menú que muestran un menú o un submenú es "Open" o "CLOSE", dependiendo del estado del menú. La propiedad **DEFAULTACTION** para todos los demás elementos de menú es "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del elemento de menú, que es el carácter subrayado en el texto del nombre del elemento de menú. Por ejemplo, la propiedad **KeyboardShortcut** del elemento de menú archivo es "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** es igual que el nombre del elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **principal** es la barra de menús o el menú emergente que contiene el elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad de **rol** es [**rol de \_ sistema \_ MenuItem**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **State** es el [**sistema de estado \_ \_ invisible**](object-state-constants.md) o una combinación de uno o varios de los siguientes valores: estado de sistema [**\_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ activado**](object-state-constants.md) sistema de estado HOTTRACKED sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Focused**](object-state-constants.md) System \| [**\_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

-   Cuando se usa en un elemento de menú, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) devuelve S \_ OK pero no realiza la acción si el carácter utilizado en la tecla de acceso es?,!, @, o cualquier otro carácter que requiera la tecla Mayús u otra tecla modificadora. Esto también sucede en teclados internacionales con un carácter de tecla de acceso que requiere que se presione la tecla ALT GR.
-   El método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con [**SELFLAG \_ TAKEFOCUS**](selflag.md) no hace que un elemento de menú abra o cierre un menú emergente. Los clientes utilizan el método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para abrir o cerrar un menú emergente.
-   Un elemento de barra de menús que no muestra un menú emergente devuelve "Application" para la propiedad **Name** en lugar del nombre del elemento de menú.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra de menús**](menu-bar.md)
</dt> <dt>

[**Menú emergente**](pop-up-menu.md)
</dt> </dl>

 

 





