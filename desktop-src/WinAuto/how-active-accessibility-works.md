---
title: Cómo funciona Active Accessibility trabajo
description: Microsoft Active Accessibility está diseñado para ayudar a que las ayuda de accesibilidad, denominadas clientes, interactúen con elementos de interfaz de usuario estándar y personalizados de otras aplicaciones y el sistema operativo.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7269042644cff139c9a554a93b3ede03952a8d5df5443bf34a74e5f07ba4742f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929565"
---
# <a name="how-active-accessibility-works"></a>Cómo funciona Active Accessibility trabajo

Microsoft Active Accessibility está diseñado para ayudar a que las ayuda de accesibilidad, denominadas *clientes,* interactúen con elementos de interfaz de usuario estándar y personalizados de otras aplicaciones y el sistema operativo. Un Microsoft Active Accessibility cliente es cualquier programa que usa Microsoft Active Accessibility para acceder, identificar o manipular los elementos de interfaz de usuario de una aplicación. Los clientes incluyen ayuda de accesibilidad, herramientas de prueba automatizadas y algunas aplicaciones de entrenamiento basadas en equipos.

Mediante Microsoft Active Accessibility, una aplicación cliente puede:

-   Consulta de información; por ejemplo, sobre un elemento de interfaz de usuario en una ubicación determinada.
-   Recibir notificaciones cuando cambie la información; por ejemplo, cuando un control aparece atenuado o cuando cambia una cadena de texto.
-   Llevar a cabo acciones que afecten al contenido de la interfaz de usuario o del documento; Por ejemplo, haga clic en un botón de inserción, coloque un menú y elija un comando de menú.

Las aplicaciones que interactúan con y proporcionan información para los clientes se *denominan servidores*. Un servidor usa Microsoft Active Accessibility para proporcionar información sobre sus elementos de interfaz de usuario a los clientes. Cualquier control, módulo o aplicación que use Microsoft Active Accessibility para exponer información sobre su interfaz de usuario se considera Microsoft Active Accessibility servidor. Los servidores se comunican con los clientes enviando notificaciones de eventos (por ejemplo, llamando a [**NotifyWinEvent)**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)y respondiendo a las solicitudes de cliente de acceso a elementos de la interfaz de usuario (por ejemplo, control de mensajes [**\_ WM GETOBJECT**](wm-getobject.md) enviados desde [*OLEACC).*](uiauto-glossary.md) Los servidores exponen información a través de [**la interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Mediante Microsoft Active Accessibility, una aplicación de servidor puede:

-   Proporcione información sobre sus objetos de interfaz de usuario personalizados y el contenido de sus ventanas cliente.
-   Enviar notificaciones cuando cambie su interfaz de usuario.

Por ejemplo, para permitir que un usuario seleccione comandos verbalmente desde una barra de herramientas personalizada de procesador de palabras, un programa de reconocimiento de voz debe tener información sobre esa barra de herramientas. Por lo tanto, el procesador de palabras tendría que hacer que esa información esté disponible. Microsoft Active Accessibility proporciona los medios para que el procesador de palabras exponga información sobre su barra de herramientas personalizada y para que el programa de reconocimiento de voz obtenga esa información.

### <a name="client-applications-and-active-accessibility"></a>Aplicaciones cliente y Active Accessibility

Un Microsoft Active Accessibility cliente debe recibir una notificación cuando la interfaz de usuario del servidor haya cambiado para que pueda transmitir esa información al usuario. Para asegurarse de que el cliente está informado sobre los cambios de la interfaz de usuario, usa un mecanismo denominado Eventos de ventana, o WinEvents, para registrarse para recibir notificaciones. Para obtener más información, vea [WinEvents](winevents-infrastructure.md).

Para obtener información sobre un elemento de interfaz de usuario determinado y manipularlo, los clientes usan la interfaz Microsoft Active Accessibility Component Object Model (COM), [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Un cliente puede recuperar un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un elemento de interfaz de usuario de las cuatro maneras siguientes:

-   Llame [**a AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y pase el identificador de ventana del elemento de la interfaz de usuario.
-   Llame [**a AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) y pase una ubicación de pantalla que se encuentra dentro del rectángulo delimitador del elemento de interfaz de usuario.
-   Establezca un enlace de WinEvent, reciba una notificación y llame a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) para recuperar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de interfaz de usuario que generó el evento.
-   Llame a [**un método IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) como [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) u [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) para moverse a otro **objeto IAccessible.**

 

 




