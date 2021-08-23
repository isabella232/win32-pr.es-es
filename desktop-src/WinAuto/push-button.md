---
title: Botón De inserción (Referencia del elemento de la interfaz de usuario de MSAA)
description: Un botón de inserción es un objeto pequeño y rectangular que se usa para realizar una acción. Por ejemplo, los botones Aceptar y CANCELAR de un cuadro de diálogo son botones de inserción.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4056b1b2bd8f80e79916db0056de176962bd7d3d86c2b62420deaf57f90e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644495"
---
# <a name="push-button-msaa-ui-element-reference"></a>Botón De inserción (Referencia del elemento de la interfaz de usuario de MSAA)

Un botón de inserción es un objeto pequeño y rectangular que se usa para realizar una acción. Por ejemplo, los **botones Aceptar** **y CANCELAR** de un cuadro de diálogo son botones de inserción.

El nombre de clase de ventana para un botón de inserción es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un botón de inserción admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en el botón de inserción. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un botón de inserción admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es cero o más.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **propiedad DefaultAction** es "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del botón, que es un carácter subrayado en el texto del texto de la ventana del botón. Por ejemplo, "Alt+o" es la **propiedad KeyboardShortcut** para un **botón** Aceptar.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad** Name se obtiene del texto (o título) de la ventana del control, que se muestra en el botón de inserción. Por ejemplo, "Aceptar" es la **propiedad Nombre** de un **botón** Aceptar.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ DEFAULT**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casilla**](check-box.md)
</dt> <dt>

[**Cuadro de grupo**](group-box.md)
</dt> <dt>

[**Radio Button**](radio-button.md)
</dt> </dl>

 

 





