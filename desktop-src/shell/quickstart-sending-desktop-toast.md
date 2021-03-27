---
description: En esta guía de inicio rápido se muestra cómo generar una notificación del sistema desde una aplicación de escritorio.
title: Envío de una notificación del sistema desde el escritorio
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910766"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Inicio rápido: envío de una notificación del sistema desde el escritorio

En esta guía de inicio rápido se muestra cómo generar una notificación del sistema desde una aplicación de escritorio.

## <a name="prerequisites"></a>Requisitos previos

-   Bibliotecas
    -   C++: Runtime. Object. lib
    -   C \# : Windows. Winmd
-   Un acceso directo a la aplicación, con un [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), debe instalarse en la pantalla Inicio. Sin embargo, tenga en cuenta que no es necesario anclarlo a la pantalla Inicio. Para obtener más información, vea [Cómo habilitar las notificaciones del sistema de escritorio a través de un AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Una versión de Microsoft Visual Studio que admita al menos Windows 8

## <a name="instructions"></a>Instrucciones

### <a name="1-create-your-toast-content"></a>1. cree el contenido del sistema.

> [!Note]  
> Cuando se especifica una plantilla de notificación del sistema que incluye una imagen, tenga en cuenta que las aplicaciones de escritorio solo pueden usar imágenes locales. no se admiten imágenes Web. Además, la ruta de acceso al archivo de imagen local se debe proporcionar como una ruta de acceso absoluta (no relativa).

 


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



### <a name="2-create-and-attach-the-event-handlers"></a>2. crear y adjuntar los controladores de eventos

Registre Controladores para los eventos del sistema: activado, descartado y con errores. Una aplicación de escritorio debe suscribirse al menos al evento activado para que pueda controlar la activación esperada de la aplicación desde la notificación del sistema cuando el usuario la seleccione.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. enviar la notificación del sistema

> [!IMPORTANT]
> Debe incluir el [AppUserModelID](../properties/props-system-appusermodel-id.md) del acceso directo de la aplicación en la pantalla Inicio cada vez que llame a [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Si no lo hace, no se mostrará la notificación del sistema.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. controlar las devoluciones de llamada

Coloque la ventana de la aplicación en primer plano si recibe una devolución de llamada "activada" de la notificación del sistema. Cuando un usuario selecciona una notificación del sistema, la expectativa es que la aplicación se inicie en una vista relacionada con el contenido de ese sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo sobre cómo enviar notificaciones del sistema de aplicaciones de escritorio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Esquema XML del sistema de notificación](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Introducción a las notificaciones del sistema](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Inicio rápido: envío de una notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Inicio rápido: envío de una notificación de notificaciones de envío](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Directrices y lista de comprobación para las notificaciones del sistema](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Cómo elegir y usar una plantilla de notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Cómo controlar la activación desde una notificación del sistema](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Cómo participar en las notificaciones del sistema](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Elección de una plantilla de notificación del sistema](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opciones de audio del sistema](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
