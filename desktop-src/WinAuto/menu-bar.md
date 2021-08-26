---
title: Barra de menús (Referencia de elementos de la interfaz de usuario de MSAA)
description: Una barra de menús es el área de una ventana inmediatamente debajo de la barra de título que contiene elementos de menú como Archivo, Edición, Ventana y Ayuda.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1212ba3c56673ab638e5aeedcc0ce20aea68dda2ad55e0904906d9f809c234ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998415"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra de menús (Referencia de elementos de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de barra** de menús para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo crear objetos **de barra** de menús en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Una barra de menús es el área de una ventana inmediatamente debajo de la barra de título que contiene elementos de menú como **Archivo,** **Edición,** **Ventana** y **Ayuda.** Microsoft Active Accessibility también crea un objeto de barra de menús para un menú del sistema, que es el menú de la esquina superior izquierda de la barra de título y contiene elementos de menú como **Restaurar**, **Mover,** **Tamaño,** **Minimizar** y **Maximizar**.

> [!Note]  
> Dado que los controles de barra de menús no reciben el foco, los métodos [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) no se admiten para este control.

 

## <a name="iaccessible-methods"></a>Métodos IAccessible

Los controles de barra de menús admiten los [**siguientes métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Los controles de barra de menús admiten las [**siguientes propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera el [**IDispatch para**](idispatch-interface.md) el elemento de menú especificado. Los identificaciónes secundarios de los elementos de menú se numeran secuencialmente de izquierda a derecha, empezando por uno.                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es el número de elementos de menú de la barra de menús. La **propiedad ChildCount** de un menú del sistema es una.                                                                                                                                                                                                                                                   |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | La **propiedad Description** de una barra de menús es "Contiene comandos para manipular la vista o el documento actuales". La **propiedad Description** de un menú del sistema es "Contiene comandos para manipular la ventana".                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** de una barra de menús debajo de la barra de título es "Alt". La **propiedad KeyboardShortcut** de un menú del sistema es "Alt+Espacio".                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Nombre** de una barra de menús debajo de la barra de título es "Aplicación". La **propiedad** Nombre de un menú del sistema es "Sistema".                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ MENUBAR**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores [siguientes:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

El sistema desencadena más de un [**evento \_ \_ MENUSTART**](event-constants.md) DEL SISTEMA DE EVENTOS que no siempre tiene un evento [**\_ \_ MENUEND del SISTEMA DE**](event-constants.md) EVENTOS correspondiente. Además, el sistema no desencadena los eventos [**\_ \_ MENUPOPUPSTART**](event-constants.md) y [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) de forma coherente. Se trata de un problema conocido que se está abordando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Elemento de menú**](menu-item.md)
</dt> <dt>

[**Menú emergente**](pop-up-menu.md)
</dt> </dl>

 

 





