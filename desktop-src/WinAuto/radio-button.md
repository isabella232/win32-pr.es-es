---
title: Botón de radio (Referencia del elemento de la interfaz de usuario de MSAA)
description: Los botones de radio se usan para seleccionar una de varias opciones, normalmente dentro de un cuadro de diálogo.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c560e4efa57790980d852ab2716248d5b1d7faff535592f3f2ca892f3dff0715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998145"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Botón de radio (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de botón** de radio para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo crear **objetos de botón** de radio en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Los botones de radio se usan para seleccionar una de varias opciones, normalmente dentro de un cuadro de diálogo. Un botón de radio contiene un círculo pequeño con texto junto a él. Cuando se selecciona, el círculo tiene un círculo más pequeño y relleno dentro de él. Al seleccionar un botón de un conjunto, se anula la selección del botón seleccionado previamente, por lo que solo se selecciona una de las opciones del conjunto a la vez.

El nombre de clase de ventana para un botón de radio es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un botón de radio admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en el botón de radio. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un botón de radio admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **propiedad DefaultAction** de un botón de radio es "Check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **propiedad KeyboardShortcut** es la tecla de acceso del botón de radio, que es un carácter subrayado en el texto de la ventana del control. Esta cadena contiene el carácter de clave de acceso anexado a la cadena "Alt+".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad** Name se obtiene del texto de ventana (o título) del control, que se muestra con el botón de radio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **propiedad Parent** es una ventana ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ RADIOBUTTON**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ CHECKED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casilla**](check-box.md)
</dt> <dt>

[**Cuadro de grupo**](group-box.md)
</dt> <dt>

[**Botón**](push-button.md)
</dt> </dl>

 

 





