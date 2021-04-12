---
title: Interfaces de complemento de DSP
description: Interfaces de complemento de DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Complementos de Windows Media Player, interfaces DSP
- Complementos de Windows Media Player, interfaces
- complementos, interfaces DSP
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos de procesamiento de señal digital, interfaz ISpecifyPropertyPage
- Complementos DSP, interfaces
- Complementos DSP, interfaz ISpecifyPropertyPage
- interfaces, Complementos DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420433"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="bc10a-113">Interfaces de complemento de DSP</span><span class="sxs-lookup"><span data-stu-id="bc10a-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="bc10a-114">Las interfaces de complemento de procesamiento de señal digital (DSP) se usan para administrar la transferencia de datos entre Windows Media Player y el complemento.</span><span class="sxs-lookup"><span data-stu-id="bc10a-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="bc10a-115">Todos los complementos de DSP pueden implementar opcionalmente la interfaz **ISpecifyPropertyPage** para proporcionar una implementación de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bc10a-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="bc10a-116">Se requieren las siguientes interfaces para crear complementos de DSP.</span><span class="sxs-lookup"><span data-stu-id="bc10a-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="bc10a-117">Interfaz</span><span class="sxs-lookup"><span data-stu-id="bc10a-117">Interface</span></span>                                                | <span data-ttu-id="bc10a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc10a-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc10a-119">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="bc10a-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="bc10a-120">Administra el intercambio de datos con Windows Media Player y realiza tareas de procesamiento de señal digital.</span><span class="sxs-lookup"><span data-stu-id="bc10a-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="bc10a-121">La documentación detallada se incluye con el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="bc10a-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="bc10a-122">IWMPMediaPluginRegistrar</span><span class="sxs-lookup"><span data-stu-id="bc10a-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="bc10a-123">Administra el registro del complemento.</span><span class="sxs-lookup"><span data-stu-id="bc10a-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="bc10a-124">IWMPPlugin</span><span class="sxs-lookup"><span data-stu-id="bc10a-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="bc10a-125">Administra la conexión a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bc10a-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="bc10a-126">IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="bc10a-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="bc10a-127">Almacena si el complemento está habilitado actualmente por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc10a-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="bc10a-128">IWMPServices</span><span class="sxs-lookup"><span data-stu-id="bc10a-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="bc10a-129">Recupera información del reproductor sobre el estado de flujo y la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="bc10a-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="bc10a-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc10a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc10a-131">**Referencia de programación de complementos DSP**</span><span class="sxs-lookup"><span data-stu-id="bc10a-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




