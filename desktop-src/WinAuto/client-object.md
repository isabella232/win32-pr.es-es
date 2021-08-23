---
title: Objeto de cliente (referencia de elemento de la interfaz de usuario de MSAA)
description: El área de cliente es la parte de una ventana donde la aplicación muestra la salida, como texto o gráficos. Por ejemplo, una aplicación de publicación de escritorio muestra la página actual de un documento en el área cliente.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645065"
---
# <a name="client-object-msaa-ui-element-reference"></a>Objeto de cliente (referencia de elemento de la interfaz de usuario de MSAA)

El área de cliente es la parte de una ventana donde la aplicación muestra la salida, como texto o gráficos. Por ejemplo, una aplicación de publicación de escritorio muestra la página actual de un documento en el área cliente.

Los desarrolladores de aplicaciones de servidor son responsables de crear objetos accesibles que proporcionan información sobre el contenido del área cliente de la aplicación.

Si una aplicación cliente solicita información sobre un elemento de interfaz de usuario personalizado dentro de una aplicación y el elemento de interfaz de usuario personalizado que no admite la interfaz [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Microsoft Active Accessibility crea un objeto accesible predeterminado con información mínima.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El área de cliente admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

El área de cliente admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Envía el [**mensaje \_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) para recuperar el texto de la ventana.                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **propiedad Role** es ROLE SYSTEM [**\_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

