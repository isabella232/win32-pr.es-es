---
title: Ventana (Referencia del elemento de interfaz de usuario de MSAA)
description: Microsoft Active Accessibility crea un objeto de ventana genérico como contenedor para otro objeto. Los desarrolladores de cliente no transmiten la información de los objetos de ventana a los usuarios finales porque estos objetos no contienen información útil.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881eb863c6b12f8e72a9f48ba5ea290a2ad2f2471fa60683ee17e70c6271dad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413275"
---
# <a name="window-msaa-ui-element-reference"></a>Ventana (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos Window** para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **Window en** varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Microsoft Active Accessibility crea un objeto de ventana genérico como contenedor para otro objeto. Los desarrolladores de cliente no transmiten la información de los objetos de ventana a los usuarios finales porque estos objetos no contienen información útil.

Si una aplicación de servidor crea un control personalizado, Microsoft Active Accessibility crea un objeto de ventana que contiene el control personalizado, pero el servidor crea un objeto accesible para proporcionar información sobre el contenido del control. El sistema genera eventos de nivel de objeto para el objeto de ventana, pero el servidor debe enviar eventos para el objeto accesible que proporciona información sobre el control.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El objeto window admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

El objeto de ventana admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera la [interfaz IDispatch](idispatch-interface.md) del elemento secundario especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **propiedad ChildCount** es 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | El propio objeto de ventana no tiene una **propiedad Description.** La **propiedad Description** del objeto secundario se puede recuperar a través del objeto de ventana.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | El propio objeto de ventana no tiene una **propiedad KeyboardShortcut.** La **propiedad KeyboardShortcut** del objeto secundario se recupera a través del objeto de ventana.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **propiedad Name** del objeto de ventana es la misma que el objeto secundario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ WINDOW.**](object-roles.md) El **rol** del objeto secundario se recupera a través del objeto de ventana.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ SIZEABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ MOVEABLE**](object-state-constants.md) STATE SYSTEM \| [**FOCUSABLE STATE SYSTEM \_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

El objeto de ventana no envía los eventos [**EVENT \_ SYSTEM \_ DRAGDROPSTART,**](event-constants.md) [**EVENT SYSTEM \_ \_ DRAGDROPEND,**](event-constants.md) [**EVENT OBJECT \_ \_ HIDE**](event-constants.md)y [**EVENT OBJECT \_ \_ PARENTCHANGE.**](event-constants.md) Se trata de un problema conocido que se está abordando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





