---
title: Cómo funciona Active Accessibility
description: Microsoft Active Accessibility está diseñado para ayudar a las ayudas de accesibilidad, denominadas clientes, interactuar con elementos de interfaz de usuario estándar y personalizados de otras aplicaciones y del sistema operativo.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103904380"
---
# <a name="how-active-accessibility-works"></a>Cómo funciona Active Accessibility

Microsoft Active Accessibility está diseñado para ayudar a las ayudas de accesibilidad, denominadas *clientes*, interactuar con elementos de interfaz de usuario estándar y personalizados de otras aplicaciones y del sistema operativo. Un cliente de Microsoft Active Accessibility es cualquier programa que utiliza Microsoft Active Accessibility para tener acceso, identificar o manipular los elementos de la interfaz de usuario de una aplicación. Los clientes incluyen ayudas para la accesibilidad, herramientas de pruebas automatizadas y algunas aplicaciones de aprendizaje basadas en equipos.

Con Microsoft Active Accessibility, una aplicación cliente puede:

-   Consulta para obtener información; por ejemplo, acerca de un elemento de la interfaz de usuario en una ubicación determinada.
-   Recibir notificaciones cuando cambie la información; por ejemplo, cuando un control se atenúa o cuando cambia una cadena de texto.
-   Llevar a cabo acciones que afectan al contenido de la interfaz de usuario o del documento; por ejemplo, haga clic en un botón de comando, desplegar un menú y elegir un comando de menú.

Las aplicaciones que interactúan con y proporcionan información para los clientes de se denominan *servidores* de. Un servidor utiliza Microsoft Active Accessibility para proporcionar información sobre los elementos de la interfaz de usuario a los clientes. Cualquier control, módulo o aplicación que use Microsoft Active Accessibility para exponer información sobre su interfaz de usuario se considera un servidor de Microsoft Active Accessibility. Los servidores se comunican con los clientes mediante el envío de notificaciones de eventos (como llamar a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)) y responder a las solicitudes de cliente para el acceso a los elementos de la interfaz de usuario (por ejemplo, el control de los mensajes de [**WM \_ GETOBJECT**](wm-getobject.md) enviados desde [*OLEACC*](uiauto-glossary.md)). Los servidores exponen información a través de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Con Microsoft Active Accessibility, una aplicación de servidor puede:

-   Proporcionar información sobre los objetos de interfaz de usuario personalizados y el contenido de las ventanas de cliente.
-   Enviar notificaciones cuando cambia la interfaz de usuario.

Por ejemplo, para permitir que un usuario seleccione comandos verbalmente desde una barra de herramientas personalizada del procesador de textos, un programa de reconocimiento de voz debe tener información sobre esa barra de herramientas. Por lo tanto, el procesador de textos debe hacer que esa información esté disponible. Microsoft Active Accessibility proporciona el medio para que el procesador de textos exponga información sobre su barra de herramientas personalizada y para que el programa de reconocimiento de voz obtenga esa información.

### <a name="client-applications-and-active-accessibility"></a>Aplicaciones cliente y Active Accessibility

Un cliente de Microsoft Active Accessibility debe recibir una notificación cuando haya cambiado la interfaz de usuario del servidor para que pueda transmitir esa información al usuario. Para asegurarse de que el cliente está informado sobre los cambios de la interfaz de usuario, usa un mecanismo denominado eventos de ventana, o WinEvents, para registrarse y recibir notificaciones. Para obtener más información, vea [WinEvents](winevents-infrastructure.md).

Para obtener información sobre un elemento de la interfaz de usuario determinado, los clientes utilizan la interfaz del modelo de objetos componentes (COM) de Microsoft Active Accessibility, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Un cliente puede recuperar un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un elemento de la interfaz de usuario de las cuatro maneras siguientes:

-   Llame a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y pase el identificador de ventana del elemento de la interfaz de usuario.
-   Llame a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) y pase una ubicación de pantalla que se encuentre dentro del rectángulo delimitador del elemento de la interfaz de usuario.
-   Establezca un enlace WinEvent, reciba una notificación y llame a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) para recuperar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento de la interfaz de usuario que generó el evento.
-   Llame a un método [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) como [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) o [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) para desplace a un objeto **IAccessible** diferente.

 

 




