---
title: Control Tab (Referencia de elementos de la interfaz de usuario de MSAA)
description: Un control de pestaña define varias páginas para la misma área de una ventana o cuadro de diálogo.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cc8381a668701446e06df81694941ece9f5f259
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567340"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Control Tab (Referencia de elementos de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control** tab para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de control de tabulación** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control de pestaña define varias páginas para la misma área de una ventana o cuadro de diálogo. Cada página consta de un conjunto de información o un grupo de controles que una aplicación muestra cuando el usuario selecciona la pestaña correspondiente. El Windows operativo usa controles de pestaña para mostrar los botones de la barra de tareas, a excepción del **botón** Iniciar.

El nombre de clase de ventana de un control de pestaña es WC TABCONTROL, que se define como \_ "SysTabControl" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de pestaña admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en la pestaña de la página. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un control de pestaña admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **propiedad DefaultAction** es "Switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del control de pestaña, que es un carácter subrayado en el texto de la ventana del control. Esta cadena contiene el carácter de clave de acceso anexado a la cadena "Alt+".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad** Name se obtiene del texto de ventana (o título) del control, que se muestra en el control de ficha.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana [**(ROLE SYSTEM \_ \_ PAGETABLIST)**](object-roles.md) que rodea el control y tiene el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ PAGETAB**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ SELECTABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ SELECTED**](object-state-constants.md) STATE SYSTEM \| FOCUSABLE STATE SYSTEM [**\_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

Los controles tab devuelven incorrectamente S \_ OK desde el método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) cuando se llama con la [**marca \_ TAKEFOCUS DE SELFANDER.**](selflag.md) Los controles de tabulación no pueden tomar el foco del teclado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





