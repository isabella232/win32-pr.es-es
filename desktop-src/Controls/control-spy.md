---
title: Controlar Spy v 2.0
description: Controlar Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes sobre cómo aplicarles estilos y cómo responden a los mensajes y las notificaciones.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078536"
---
# <a name="control-spy-v20"></a><span data-ttu-id="af8b6-103">Controlar Spy v 2.0</span><span class="sxs-lookup"><span data-stu-id="af8b6-103">Control Spy v2.0</span></span>

<span data-ttu-id="af8b6-104">Controlar Spy es una herramienta que ayuda a los desarrolladores a comprender los controles comunes: Cómo aplicarles estilos y cómo responden a los mensajes y las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="af8b6-104">Control Spy is a tool that helps developers understand common controls: how to apply styles to them, and how they respond to messages and notifications.</span></span> <span data-ttu-id="af8b6-105">Con control Spy, puede ver inmediatamente el modo en que los distintos estilos afectan al comportamiento y la apariencia de cada control y también cómo puede cambiar el estado de cada control mediante el envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="af8b6-105">Using Control Spy, you can immediately see how different styles affect the behavior and appearance of each control, and also how you can change the state of each control by sending messages.</span></span>

<span data-ttu-id="af8b6-106">Hay disponibles dos versiones de control Spy, una para [Comctl32.dll versión 5. x](common-control-versions.md) y otra para Comctl32.dll versión 6,0 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="af8b6-106">Two versions of Control Spy are available, one for [Comctl32.dll version 5.x](common-control-versions.md) and one for Comctl32.dll version 6.0 and later.</span></span> <span data-ttu-id="af8b6-107">ControlSpyV6.exe tiene un manifiesto de aplicación integrado para que use los controles con control de versiones más recientes.</span><span class="sxs-lookup"><span data-stu-id="af8b6-107">ControlSpyV6.exe has a built-in application manifest so that it uses the newer, themed controls.</span></span> <span data-ttu-id="af8b6-108">ControlSpyV5.exe no tiene este manifiesto y, de forma predeterminada, es la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="af8b6-108">ControlSpyV5.exe does not have this manifest and so defaults to the older version.</span></span>

<span data-ttu-id="af8b6-109">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="af8b6-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="af8b6-110">Información general</span><span class="sxs-lookup"><span data-stu-id="af8b6-110">Overview</span></span>](#overview)
-   [<span data-ttu-id="af8b6-111">Estilos</span><span class="sxs-lookup"><span data-stu-id="af8b6-111">Styles</span></span>](#styles)
-   [<span data-ttu-id="af8b6-112">Mensajes</span><span class="sxs-lookup"><span data-stu-id="af8b6-112">Messages</span></span>](#messages)
-   [<span data-ttu-id="af8b6-113">Tamaño/color</span><span class="sxs-lookup"><span data-stu-id="af8b6-113">Size/Color</span></span>](#sizecolor)
-   [<span data-ttu-id="af8b6-114">Dónde obtener el control Spy</span><span class="sxs-lookup"><span data-stu-id="af8b6-114">Where to Get Control Spy</span></span>](#where-to-get-control-spy)
-   [<span data-ttu-id="af8b6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af8b6-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="af8b6-116">Información general</span><span class="sxs-lookup"><span data-stu-id="af8b6-116">Overview</span></span>

<span data-ttu-id="af8b6-117">Control Spy hospeda un control común seleccionado en el centro de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="af8b6-117">Control Spy hosts a selected common control in the center of its application window.</span></span> <span data-ttu-id="af8b6-118">Puede cambiar el control que se muestra seleccionando distintos controles en el cuadro de lista en el lado izquierdo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="af8b6-118">You can change which control is shown by selecting different controls from the list box at the left side of the window.</span></span> <span data-ttu-id="af8b6-119">Los mensajes o las notificaciones recibidas por el control se mostrarán en la parte derecha de la ventana cuando lleguen.</span><span class="sxs-lookup"><span data-stu-id="af8b6-119">Messages or notifications received by the control will be listed at the right side of the window as they arrive.</span></span> <span data-ttu-id="af8b6-120">Puede habilitar o deshabilitar esta funcionalidad mediante las casillas **mensajes recibidos** y **notificaciones recibidas** .</span><span class="sxs-lookup"><span data-stu-id="af8b6-120">You can enable or disable this functionality by using the **Messages Received** and **Notifications Received** check boxes.</span></span>

<span data-ttu-id="af8b6-121">En la imagen siguiente se muestra la aplicación control Spy.</span><span class="sxs-lookup"><span data-stu-id="af8b6-121">The following image shows the Control Spy application.</span></span>

![ventana controlar Spy](images/controlspy-main.png)

<span data-ttu-id="af8b6-123">En la parte inferior de la ventana, hay varias pestañas que presentan más funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="af8b6-123">At the bottom of the window, there are several tabs that present more functionality.</span></span>

## <a name="styles"></a><span data-ttu-id="af8b6-124">Estilos</span><span class="sxs-lookup"><span data-stu-id="af8b6-124">Styles</span></span>

<span data-ttu-id="af8b6-125">La pestaña **estilos** permite cambiar el estilo de ventana actual del control.</span><span class="sxs-lookup"><span data-stu-id="af8b6-125">The **Styles** tab enables you to change the current window style of the control.</span></span> <span data-ttu-id="af8b6-126">Seleccione o anule la selección de cualquiera de los estilos de la lista y, a continuación, haga clic en el botón **aplicar** para cambiar el estilo del control mostrado.</span><span class="sxs-lookup"><span data-stu-id="af8b6-126">Select or deselect any of the listed styles, then click the **Apply** button to change the style of the displayed control.</span></span> <span data-ttu-id="af8b6-127">Como alternativa, puede usar el botón **volver a crear** para crear un nuevo control con los estilos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="af8b6-127">Alternately, you can use the **Recreate** button to create a new control with the selected styles.</span></span> <span data-ttu-id="af8b6-128">El botón **restablecer** devolverá el control a los estilos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="af8b6-128">The **Reset** button will return the control to the default styles.</span></span>

<span data-ttu-id="af8b6-129">Los botones **copiar estilo** y **copiar** estilo que se encuentran debajo de la ficha copiarán las constantes de estilo seleccionadas en el portapapeles como una lista delimitada OR bit a bit ( \| ).</span><span class="sxs-lookup"><span data-stu-id="af8b6-129">The **Copy Style** and **Copy ExStyle** buttons below the tab will copy the selected style constants to the Clipboard as a bitwise OR (\|) delimited list.</span></span> <span data-ttu-id="af8b6-130">Puede pegar esta lista directamente en la llamada a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para proporcionar un control en su propia aplicación con el mismo estilo.</span><span class="sxs-lookup"><span data-stu-id="af8b6-130">You can paste this list directly into your call to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to provide a control in your own application with the same style.</span></span>

<span data-ttu-id="af8b6-131">En la imagen siguiente se muestra la pestaña **estilos** de un control botón.</span><span class="sxs-lookup"><span data-stu-id="af8b6-131">The following image shows the **Styles** tab for a button control.</span></span>

![controlar la pestaña de estilos de Spy](images/controlspy-styles.png)

## <a name="messages"></a><span data-ttu-id="af8b6-133">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="af8b6-133">Messages</span></span>

<span data-ttu-id="af8b6-134">La pestaña **mensajes** le permite enviar casi cualquier mensaje a un control.</span><span class="sxs-lookup"><span data-stu-id="af8b6-134">The **Messages** tab enables you to send almost any message to a control.</span></span> <span data-ttu-id="af8b6-135">Después de seleccionar un mensaje en el cuadro de lista, puede especificar los datos que se envían como los parámetros *wParam* y *lParam* de la llamada a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="af8b6-135">After selecting a message from the list box, you can enter data which is sent as the *wParam* and *lParam* parameters of the call to [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="af8b6-136">Después de hacer clic en **Enviar**, el mensaje se envía al control y los resultados se muestran en el cuadro de texto de la parte inferior de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="af8b6-136">After you click **Send**, the message is sent to the control and any result is displayed in the text box at the bottom of the tab.</span></span>

<span data-ttu-id="af8b6-137">La siguiente imagen muestra la ficha mensajes cuando se selecciona un mensaje determinado.</span><span class="sxs-lookup"><span data-stu-id="af8b6-137">The following image shows the messages tab when a particular message is selected.</span></span>

![pestaña controlar mensajes de Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a><span data-ttu-id="af8b6-139">Tamaño/color</span><span class="sxs-lookup"><span data-stu-id="af8b6-139">Size/Color</span></span>

<span data-ttu-id="af8b6-140">La pestaña **tamaño/color** se puede usar para cambiar el tamaño del control y el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="af8b6-140">The **Size/Color** tab can be used to change the size of the control as well as the color of its background.</span></span>

## <a name="where-to-get-control-spy"></a><span data-ttu-id="af8b6-141">Dónde obtener el control Spy</span><span class="sxs-lookup"><span data-stu-id="af8b6-141">Where to Get Control Spy</span></span>

<span data-ttu-id="af8b6-142">Puede descargar el [control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="af8b6-142">You can download [Control Spy 2.0](https://www.microsoft.com/download/details.aspx?id=4635) from MSDN.</span></span> <span data-ttu-id="af8b6-143">Ambas versiones están contenidas en la descarga.</span><span class="sxs-lookup"><span data-stu-id="af8b6-143">Both versions are contained in the download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8b6-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af8b6-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="af8b6-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="af8b6-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="af8b6-146">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="af8b6-146">Windows Controls</span></span>](window-controls.md)
</dt> <dt>

[<span data-ttu-id="af8b6-147">Habilitar los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="af8b6-147">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> </dl>

 

 