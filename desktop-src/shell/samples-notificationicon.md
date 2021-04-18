---
description: Muestra cómo usar las API de Shell \_ NotifyIcon y Shell \_ NotifyIconGetRect para mostrar un icono de notificación.
title: Ejemplo de NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985578"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="4f3d5-103">Ejemplo de NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="4f3d5-103">NotificationIcon Sample</span></span>

<span data-ttu-id="4f3d5-104">Muestra cómo usar las API de Shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) y [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) para mostrar un icono de notificación.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="4f3d5-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4f3d5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f3d5-106">Description</span></span>](#description)
-   [<span data-ttu-id="4f3d5-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3d5-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4f3d5-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4f3d5-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4f3d5-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="4f3d5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f3d5-111">Description</span></span>

<span data-ttu-id="4f3d5-112">Además del uso de los comandos [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) y [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) de Shell para mostrar un icono de notificación, en este ejemplo también se muestra cómo mostrar una ventana flotante enriquecida, un menú contextual y una notificación de globo.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="4f3d5-113">[**Shell \_ de NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) solo está disponible en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f3d5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3d5-114">Requirements</span></span>



| <span data-ttu-id="4f3d5-115">Producto</span><span class="sxs-lookup"><span data-stu-id="4f3d5-115">Product</span></span>                                | <span data-ttu-id="4f3d5-116">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="4f3d5-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4f3d5-117">Windows</span><span class="sxs-lookup"><span data-stu-id="4f3d5-117">Windows</span></span>                                | <span data-ttu-id="4f3d5-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f3d5-118">Windows 7</span></span>               |
| <span data-ttu-id="4f3d5-119">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="4f3d5-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4f3d5-120">7.0</span><span class="sxs-lookup"><span data-stu-id="4f3d5-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4f3d5-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-121">Downloading the Sample</span></span>

| <span data-ttu-id="4f3d5-122">Ubicación</span><span class="sxs-lookup"><span data-stu-id="4f3d5-122">Location</span></span>      | <span data-ttu-id="4f3d5-123">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4f3d5-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3d5-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="4f3d5-124">GitHub</span></span>  | [<span data-ttu-id="4f3d5-125">Ejemplo de NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="4f3d5-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="4f3d5-126">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-126">Building the Sample</span></span>

<span data-ttu-id="4f3d5-127">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="4f3d5-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="4f3d5-128">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="4f3d5-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="4f3d5-129">Escriba `msbuild NotificationIcon.sln`.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="4f3d5-130">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="4f3d5-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="4f3d5-131">Abra el explorador de Windows y navegue hasta el directorio del proyecto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="4f3d5-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="4f3d5-132">Haga doble clic en el icono del archivo NotificationIcon. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4f3d5-133">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4f3d5-134">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f3d5-134">Running the Sample</span></span>

1.  <span data-ttu-id="4f3d5-135">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="4f3d5-136">En la línea de comandos, escriba `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="4f3d5-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="4f3d5-137">Como alternativa, en el explorador de Windows, haga doble clic en el icono de NotificationIcon.exe.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="4f3d5-138">Los iconos de notificación especificados con un GUID están protegidos contra la suplantación de identidad mediante la validación de que solo una única aplicación los registra.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="4f3d5-139">Este registro se realiza la primera vez que se llama a NotifyIcon del shell \_ (Nim \_ Add,...) y se almacena el nombre de la ruta de acceso completa de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="4f3d5-140">Si posteriormente mueve el archivo binario a una ubicación diferente, el sistema no permitirá que el icono se vuelva a agregar.</span><span class="sxs-lookup"><span data-stu-id="4f3d5-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="4f3d5-141">Para obtener más información, consulte [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="4f3d5-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



