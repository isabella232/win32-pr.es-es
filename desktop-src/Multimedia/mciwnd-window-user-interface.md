---
title: Interfaz de usuario de la ventana MCIWnd
description: Interfaz de usuario de la ventana MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075338"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="5c69f-103">Interfaz de usuario de la ventana MCIWnd</span><span class="sxs-lookup"><span data-stu-id="5c69f-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="5c69f-104">MCIWnd proporciona características adicionales para ajustar la apariencia de la ventana de MCIWnd, personalizar el comportamiento de la aplicación y optimizar el rendimiento de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5c69f-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="5c69f-105">En la ventana de MCIWnd se incluyen las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="5c69f-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="5c69f-106">Barra de herramientas con botones **reproducir**, **detener**, **grabar** y **menú**</span><span class="sxs-lookup"><span data-stu-id="5c69f-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="5c69f-107">Barra de control que controla el posicionamiento del contenido de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5c69f-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="5c69f-108">Menú emergente que contiene comandos comunes</span><span class="sxs-lookup"><span data-stu-id="5c69f-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="5c69f-109">Un área de reproducción para vídeo y otros dispositivos que muestran imágenes</span><span class="sxs-lookup"><span data-stu-id="5c69f-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="5c69f-110">En la ilustración siguiente se muestra el estado inicial de la reproducción de vídeo controlada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5c69f-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="5c69f-111">El archivo de ejemplo utilizado es CLOCK.AVI.</span><span class="sxs-lookup"><span data-stu-id="5c69f-111">The sample file used is CLOCK.AVI.</span></span>

![Imagen de clock.avi](images/mciwnd1.gif)

<span data-ttu-id="5c69f-113">La ventana MCIWnd incluye un área de reproducción para vídeo y otros dispositivos que muestran imágenes durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5c69f-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="5c69f-114">MCIWnd omite el área de reproducción de los dispositivos de audio de onda, secuenciadores MIDI y otros dispositivos que no escriben en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5c69f-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="5c69f-115">En la ilustración siguiente se muestra el área de reproducción de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="5c69f-115">The following illustration shows the waveform-audio playback area.</span></span>

![imagen de la ventana de mciwnd](images/mciwnd4.gif)

<span data-ttu-id="5c69f-117">El botón **reproducir** se encuentra en la esquina inferior izquierda de la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5c69f-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="5c69f-118">Aparece cuando se detiene el contenido.</span><span class="sxs-lookup"><span data-stu-id="5c69f-118">It appears when the content is stopped.</span></span> <span data-ttu-id="5c69f-119">El usuario puede reproducir el contenido de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c69f-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="5c69f-120">Para reproducir el contenido desde la posición de reproducción actual, seleccione el botón **reproducir** .</span><span class="sxs-lookup"><span data-stu-id="5c69f-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="5c69f-121">Para reproducir el contenido a pantalla completa desde la posición de reproducción actual, seleccione el botón **reproducir** mientras mantiene presionada la tecla Ctrl.</span><span class="sxs-lookup"><span data-stu-id="5c69f-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="5c69f-122">Para reproducir el contenido hacia atrás desde la posición de reproducción actual, seleccione el botón **reproducir** mientras mantiene presionada la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="5c69f-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="5c69f-123">El botón de **menú** , situado junto al botón **reproducir** , activa un menú que permite al usuario abrir y cerrar archivos de audio y vídeo intercalados (AVI), y ajustar el tamaño de la imagen, la velocidad de reproducción y el volumen.</span><span class="sxs-lookup"><span data-stu-id="5c69f-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="5c69f-124">(El usuario también puede activar el menú haciendo clic con el botón secundario del mouse siempre que el cursor se encuentra en el área cliente de la ventana). El menú también incluye comandos para cambiar la configuración del dispositivo actual, copiar el contenido de reproducción en el portapapeles y emitir comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="5c69f-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="5c69f-125">La barra de menús a la derecha del botón de **menú** representa la duración del contenido de reproducción (o grabado).</span><span class="sxs-lookup"><span data-stu-id="5c69f-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="5c69f-126">El control deslizante de la barra de desplazamiento representa la posición de reproducción actual dentro del contenido.</span><span class="sxs-lookup"><span data-stu-id="5c69f-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="5c69f-127">Cuando el control deslizante se coloca en el extremo izquierdo de la barra de desplazamiento, la posición de reproducción actual es el principio del contenido.</span><span class="sxs-lookup"><span data-stu-id="5c69f-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="5c69f-128">El usuario puede desplazarse a diferentes ubicaciones del contenido arrastrando el control deslizante a lo largo de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="5c69f-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="5c69f-129">El botón **detener** se encuentra en la esquina inferior izquierda de la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5c69f-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="5c69f-130">Aparece cuando se reproduce el contenido.</span><span class="sxs-lookup"><span data-stu-id="5c69f-130">It appears when the content is played.</span></span> <span data-ttu-id="5c69f-131">En la ilustración siguiente se muestra la reproducción de vídeo en curso.</span><span class="sxs-lookup"><span data-stu-id="5c69f-131">The following illustration shows video playback in progress.</span></span>

![imagen de reproducción de vídeo](images/mciwnd2.gif)

<span data-ttu-id="5c69f-133">Los controles de MCIWnd también pueden incluir un botón de **registro** para los dispositivos que pueden grabar.</span><span class="sxs-lookup"><span data-stu-id="5c69f-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="5c69f-134">El botón **grabar** está marcado con un círculo rojo y solo aparece cuando el dispositivo es capaz de grabar.</span><span class="sxs-lookup"><span data-stu-id="5c69f-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="5c69f-135">La ventana de reproducción debe estar alineada en un límite de cuatro píxeles para obtener el mejor rendimiento de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5c69f-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="5c69f-136">Normalmente, Windows alinea la ventana automáticamente cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="5c69f-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="5c69f-137">Si un usuario mueve o estira la ventana desde su posición inicial, la velocidad de reproducción de vídeo podría reducirse a la mitad.</span><span class="sxs-lookup"><span data-stu-id="5c69f-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




