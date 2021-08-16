---
description: En este inicio rápido se muestra cómo generar una notificación del sistema desde una aplicación de escritorio.
title: Envío de una notificación del sistema desde el escritorio
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 79f8f65b18fd6774f318541b15d1649b7c25526f46bf3ab57f02edc4788687c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858659"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Inicio rápido: Envío de una notificación del sistema desde el escritorio

En este inicio rápido se muestra cómo generar una notificación del sistema desde una aplicación de escritorio.

## <a name="prerequisites"></a>Requisitos previos

-   Bibliotecas
    -   C++: Runtime.object.lib
    -   C \# : Windows. Winmd
-   Se debe instalar un acceso directo a [la aplicación, System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), en el pantalla Inicio. Sin embargo, tenga en cuenta que no es necesario anclarse al pantalla Inicio. Para más información, consulte [Habilitación de notificaciones del sistema de escritorio a través de AppUserModelID.](enable-desktop-toast-with-appusermodelid.md)
-   Una versión de Microsoft Visual Studio admite al menos Windows 8

## <a name="instructions"></a>Instructions

### <a name="1-create-your-toast-content"></a>1. Creación del contenido del sistema

> [!Note]  
> Cuando especifique una plantilla del sistema que incluya una imagen, tenga en cuenta que las aplicaciones de escritorio solo pueden usar imágenes locales. no se admiten imágenes web. Además, la ruta de acceso al archivo de imagen local debe proporcionarse como una ruta de acceso absoluta (no relativa).

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. Creación y asociación de los controladores de eventos

Registre controladores para los eventos del sistema: Activado, Descartado y Error. Una aplicación de escritorio debe suscribirse al menos al evento Activated para que pueda controlar la activación esperada de la aplicación desde el sistema cuando el usuario la selecciona.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. Envío del sistema

> [!IMPORTANT]
> Debe incluir el [AppUserModelID](../properties/props-system-appusermodel-id.md) del acceso directo de la aplicación en el pantalla Inicio cada vez que llame a [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Si no lo hace, no se mostrará el sistema.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. Controlar las devoluciones de llamada

Poner la ventana de la aplicación en primer plano si recibe una devolución de llamada "activada" de la notificación del sistema. Cuando un usuario selecciona un sistema, la expectativa es que la aplicación se inicia en una vista relacionada con el contenido de ese sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo sobre cómo enviar notificaciones del sistema de aplicaciones de escritorio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Esquema XML del sistema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Introducción a las notificaciones del sistema](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Inicio rápido: Envío de una notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Inicio rápido: Envío de una notificación push del sistema](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Directrices y lista de comprobación para notificaciones del sistema](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Cómo elegir y usar una plantilla del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Cómo controlar la activación desde una notificación del sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Cómo participar en las notificaciones del sistema](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Elección de una plantilla del sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opciones de audio del sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
