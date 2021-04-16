---
title: Barra de menús (referencia de elementos de interfaz de usuario de MSAA)
description: Una barra de menús es el área de una ventana que se encuentra inmediatamente debajo de la barra de título que contiene elementos de menú como archivo, edición, ventana y ayuda.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532146"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra de menús (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **barra de menú** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **barra de menús** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Una barra de menús es el área de una ventana que se encuentra inmediatamente debajo de la barra de título que contiene elementos de menú como **archivo**, **edición**, **ventana** y **ayuda**. Microsoft Active Accessibility también crea un objeto de barra de menús para un menú del sistema, que es el menú de la esquina superior izquierda de la barra de título y contiene elementos de menú, como **restaurar** **, cambiar** de **tamaño**, **minimizar** y **maximizar**.

> [!Note]  
> Dado que los controles de barra de menús no reciben el foco, no se admiten los métodos [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y [**Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) para este control.

 

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de barra de menús admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Los controles de barra de menús admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera [**IDispatch**](idispatch-interface.md) para el elemento de menú especificado. Los identificadores secundarios de los elementos de menú se numeran secuencialmente de izquierda a derecha a partir de uno.                                                                                                                                                                                             |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es el número de elementos de menú en la barra de menús. La propiedad **ChildCount** para un menú del sistema es una.                                                                                                                                                                                                                                                   |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | La propiedad **Description** de una barra de menús es "contiene comandos para manipular la vista o el documento actual". La propiedad **Description** de un menú del sistema es "contiene comandos para manipular la ventana".                                                                                                                                                                   |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** de una barra de menús situada debajo de la barra de título es "Alt". La propiedad **KeyboardShortcut** de un menú del sistema es "alt + barra espaciadora".                                                                                                                                                                                                                             |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** de una barra de menús situada debajo de la barra de título es "Application". La propiedad **Name** de un menú del sistema es "System".                                                                                                                                                                                                                                                |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es la [**barra de \_ \_ menús del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): sistema de estado [**\_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="notes"></a>Notas

El sistema desencadena más de un evento [**\_ \_ MENUSTART del sistema de eventos**](event-constants.md) que no siempre tiene un evento [**\_ \_ MENUEND del sistema de eventos**](event-constants.md) correspondiente. Además, el sistema no desencadena los eventos [**\_ System \_ MENUPOPUPSTART**](event-constants.md) y Event [**\_ System \_ MENUPOPUPEND**](event-constants.md) de forma coherente. Se trata de un problema conocido y se está solucionando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Elemento de menú**](menu-item.md)
</dt> <dt>

[**Menú emergente**](pop-up-menu.md)
</dt> </dl>

 

 





