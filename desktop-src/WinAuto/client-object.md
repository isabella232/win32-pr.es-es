---
title: Objeto de cliente (referencia de elementos de interfaz de usuario de MSAA)
description: El área cliente es la parte de una ventana donde la aplicación muestra la salida, como texto o gráficos. Por ejemplo, una aplicación de publicación de escritorio muestra la página actual de un documento en el área cliente.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149394"
---
# <a name="client-object-msaa-ui-element-reference"></a>Objeto de cliente (referencia de elementos de interfaz de usuario de MSAA)

El área cliente es la parte de una ventana donde la aplicación muestra la salida, como texto o gráficos. Por ejemplo, una aplicación de publicación de escritorio muestra la página actual de un documento en el área cliente.

Los desarrolladores de aplicaciones de servidor son responsables de crear objetos accesibles que proporcionan información sobre el contenido del área de cliente de la aplicación.

Si una aplicación cliente solicita información sobre un elemento de interfaz de usuario personalizado dentro de una aplicación y el elemento de la interfaz de usuario personalizado que no admite la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Microsoft Active Accessibility crea un objeto accesible predeterminado con información mínima.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El área cliente admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

El área cliente admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Envía el [**mensaje \_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) para recuperar el texto de la ventana.                                                                                                                                                                                                                                                                                                                                                                                |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

