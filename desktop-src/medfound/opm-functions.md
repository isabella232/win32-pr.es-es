---
description: Las siguientes funciones se usan con el administrador de protección de salida (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funciones de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715532"
---
# <a name="opm-functions"></a><span data-ttu-id="1f0b5-103">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="1f0b5-103">OPM Functions</span></span>

<span data-ttu-id="1f0b5-104">Las siguientes funciones se usan con el [Administrador de protección de salida](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="1f0b5-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="1f0b5-105">Función</span><span class="sxs-lookup"><span data-stu-id="1f0b5-105">Function</span></span>                                                                                             | <span data-ttu-id="1f0b5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f0b5-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f0b5-107">**OPMGetVideoOutputForTarget**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="1f0b5-108">Devuelve un objeto de salida de vídeo para el destino de VidPN en el adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="1f0b5-109">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="1f0b5-110">Crea un objeto de administrador de protección de salida (OPM) para cada monitor físico que está asociado a un identificador de **HMONITOR** determinado.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="1f0b5-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="1f0b5-112">Crea un objeto OPM para cada monitor físico que está asociado a un dispositivo Direct3D determinado.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="1f0b5-113">OPM usa las siguientes funciones para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="1f0b5-114">Las aplicaciones no deben llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="1f0b5-115">**ConfigureOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="1f0b5-116">**CreateOPMProtectedOutputs**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="1f0b5-117">**DestroyOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="1f0b5-118">**GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="1f0b5-119">**GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="1f0b5-120">**GetCOPPCompatibleOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="1f0b5-121">**GetOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="1f0b5-122">**GetOPMRandomNumber**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="1f0b5-123">**GetSuggestedOPMProtectedOutputArraySize**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="1f0b5-124">**SetOPMSigningKeyAndSequenceNumbers**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="1f0b5-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f0b5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f0b5-126">Referencia de programación de OPM</span><span class="sxs-lookup"><span data-stu-id="1f0b5-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="1f0b5-127">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="1f0b5-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



