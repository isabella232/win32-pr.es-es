---
description: Muestra cómo reproducir contenido multimedia protegido en Microsoft Media Foundation.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Ejemplo de ProtectedPlayback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811576"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="d4a48-103">Ejemplo de ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="d4a48-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="d4a48-104">Muestra cómo reproducir contenido multimedia protegido en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d4a48-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="d4a48-105">Uso</span><span class="sxs-lookup"><span data-stu-id="d4a48-105">Usage</span></span>

<span data-ttu-id="d4a48-106">En el ejemplo ProtectedPlayback se compila una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="d4a48-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="d4a48-107">Para reproducir un archivo multimedia local, seleccione **Abrir archivo** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="d4a48-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="d4a48-108">Para especificar un archivo por dirección URL, seleccione **abrir dirección URL** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="d4a48-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="d4a48-109">Después de seleccionar un archivo, la reproducción se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d4a48-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="d4a48-110">Para pausar la reproducción, presione la barra ESPACIAdora.</span><span class="sxs-lookup"><span data-stu-id="d4a48-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="d4a48-111">Para reanudar la reproducción, vuelva a presionar la barra ESPACIAdora.</span><span class="sxs-lookup"><span data-stu-id="d4a48-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="d4a48-112">API mostradas</span><span class="sxs-lookup"><span data-stu-id="d4a48-112">APIs Demonstrated</span></span>

<span data-ttu-id="d4a48-113">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d4a48-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="d4a48-114">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="d4a48-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="d4a48-115">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="d4a48-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="d4a48-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4a48-116">Requirements</span></span>



| <span data-ttu-id="d4a48-117">Producto</span><span class="sxs-lookup"><span data-stu-id="d4a48-117">Product</span></span>                                                        | <span data-ttu-id="d4a48-118">Versión</span><span class="sxs-lookup"><span data-stu-id="d4a48-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d4a48-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d4a48-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d4a48-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4a48-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d4a48-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4a48-121">Downloading the Sample</span></span>

<span data-ttu-id="d4a48-122">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span><span class="sxs-lookup"><span data-stu-id="d4a48-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4a48-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4a48-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a48-124">Cómo reproducir archivos multimedia protegidos</span><span class="sxs-lookup"><span data-stu-id="d4a48-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="d4a48-125">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4a48-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="d4a48-126">[Ejemplo de MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d4a48-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
