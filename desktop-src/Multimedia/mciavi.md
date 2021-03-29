---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivos MCI, controlador MCIAVI
- Comandos MCI, controlador MCIAVI
- Controlador MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486898"
---
# <a name="mciavi"></a><span data-ttu-id="dd9b3-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="dd9b3-106">MCIAVI</span></span>

<span data-ttu-id="dd9b3-107">Un archivo AVI puede contener más de dos secuencias, por ejemplo, una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="dd9b3-108">La aplicación puede utilizar una secuencia independientemente de las demás secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="dd9b3-109">El tipo de dispositivo **DigitalVideo** controla los archivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="dd9b3-110">Para obtener una lista de los comandos MCI reconocidos por los dispositivos de vídeo digital, consulte [conjunto de comandos de vídeo digital](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="dd9b3-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="dd9b3-111">El controlador MCIAVI reproduce secuencias de vídeo y otros flujos de datos bajo el control de los comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="dd9b3-112">Los flujos de datos pueden contener imágenes, audio y paletas.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="dd9b3-113">Los datos de imagen pueden constar de imágenes con paletas de colores o información de color verdadero.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="dd9b3-114">El audio se sincroniza con el vídeo dentro de un trigésima de segundo.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="dd9b3-115">Sin embargo, si el hardware de audio no está disponible, el controlador solo reproduce la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="dd9b3-116">El controlador MCIAVI puede quitar fotogramas de vídeo, si es necesario, para reproducir un flujo sin interrupción de audio.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="dd9b3-117">La aplicación puede usar los servicios de clase de ventana MCIWnd en lugar de la interfaz de comandos MCI para controlar cualquier controlador MCI.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="dd9b3-118">Esta clase de ventana administra muchos de los detalles de la administración de la ventana que admite el dispositivo MCI y simplifica la programación necesaria para enviar los comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="dd9b3-119">La aplicación puede usar los servicios de biblioteca MCIWnd directamente para controlar el dispositivo MCI, o bien puede tener MCIWnd mostrar una barra de herramientas, una barra de desplazamiento y menús que permitan al usuario controlar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd9b3-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="dd9b3-120">Para obtener más información sobre la clase de ventana MCIWnd, consulte [clase de ventana MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="dd9b3-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




