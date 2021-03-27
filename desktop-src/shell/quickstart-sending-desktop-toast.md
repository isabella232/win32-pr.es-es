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
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="9b161-103">Inicio rápido: envío de una notificación del sistema desde el escritorio</span><span class="sxs-lookup"><span data-stu-id="9b161-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="9b161-104">En esta guía de inicio rápido se muestra cómo generar una notificación del sistema desde una aplicación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="9b161-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9b161-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b161-105">Prerequisites</span></span>

-   <span data-ttu-id="9b161-106">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="9b161-106">Libraries</span></span>
    -   <span data-ttu-id="9b161-107">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="9b161-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="9b161-108">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="9b161-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="9b161-109">Un acceso directo a la aplicación, con un [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), debe instalarse en la pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="9b161-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="9b161-110">Sin embargo, tenga en cuenta que no es necesario anclarlo a la pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="9b161-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="9b161-111">Para obtener más información, vea [Cómo habilitar las notificaciones del sistema de escritorio a través de un AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="9b161-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="9b161-112">Una versión de Microsoft Visual Studio que admita al menos Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b161-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="9b161-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="9b161-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="9b161-114">1. cree el contenido del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b161-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="9b161-115">Cuando se especifica una plantilla de notificación del sistema que incluye una imagen, tenga en cuenta que las aplicaciones de escritorio solo pueden usar imágenes locales. no se admiten imágenes Web.</span><span class="sxs-lookup"><span data-stu-id="9b161-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="9b161-116">Además, la ruta de acceso al archivo de imagen local se debe proporcionar como una ruta de acceso absoluta (no relativa).</span><span class="sxs-lookup"><span data-stu-id="9b161-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


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



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="9b161-117">2. crear y adjuntar los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="9b161-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="9b161-118">Registre Controladores para los eventos del sistema: activado, descartado y con errores.</span><span class="sxs-lookup"><span data-stu-id="9b161-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="9b161-119">Una aplicación de escritorio debe suscribirse al menos al evento activado para que pueda controlar la activación esperada de la aplicación desde la notificación del sistema cuando el usuario la seleccione.</span><span class="sxs-lookup"><span data-stu-id="9b161-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="9b161-120">3. enviar la notificación del sistema</span><span class="sxs-lookup"><span data-stu-id="9b161-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b161-121">Debe incluir el [AppUserModelID](../properties/props-system-appusermodel-id.md) del acceso directo de la aplicación en la pantalla Inicio cada vez que llame a [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="9b161-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="9b161-122">Si no lo hace, no se mostrará la notificación del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b161-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="9b161-123">4. controlar las devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="9b161-123">4. Handle the callbacks</span></span>

<span data-ttu-id="9b161-124">Coloque la ventana de la aplicación en primer plano si recibe una devolución de llamada "activada" de la notificación del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b161-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="9b161-125">Cuando un usuario selecciona una notificación del sistema, la expectativa es que la aplicación se inicie en una vista relacionada con el contenido de ese sistema.</span><span class="sxs-lookup"><span data-stu-id="9b161-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b161-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b161-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b161-127">Ejemplo sobre cómo enviar notificaciones del sistema de aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="9b161-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="9b161-128">Cómo habilitar las notificaciones del sistema del escritorio a través de AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="9b161-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="9b161-129">Esquema XML del sistema de notificación</span><span class="sxs-lookup"><span data-stu-id="9b161-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="9b161-130">[Introducción a las notificaciones del sistema](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-131">[Inicio rápido: envío de una notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-132">[Inicio rápido: envío de una notificación de notificaciones de envío](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="9b161-133">Directrices y lista de comprobación para las notificaciones del sistema</span><span class="sxs-lookup"><span data-stu-id="9b161-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="9b161-134">[Cómo elegir y usar una plantilla de notificación del sistema](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-135">[Cómo controlar la activación desde una notificación del sistema](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-136">[Cómo participar en las notificaciones del sistema](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-137">[Elección de una plantilla de notificación del sistema](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="9b161-138">[Opciones de audio del sistema](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9b161-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
