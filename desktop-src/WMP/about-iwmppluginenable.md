---
title: Acerca de IWMPPluginEnable
description: Acerca de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IWMPPluginEnable
- complementos, interfaz IWMPPluginEnable
- Complementos de procesamiento de señal digital, interfaz IWMPPluginEnable
- Complementos DSP, interfaz IWMPPluginEnable
- Interfaz IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993953"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="7875b-113">Acerca de IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="7875b-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="7875b-114">La interfaz **IWMPPluginEnable** es necesaria para los complementos DSP de Windows Media Player. **IWMPPluginEnable** contiene dos métodos que almacenan si Windows Media Player ha habilitado el complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="7875b-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="7875b-115">Windows Media Player llama a **IWMPPluginEnable:: SetEnable** cuando crea una instancia del complemento de DSP, pasando un valor de **true** si ha habilitado el complemento o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7875b-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="7875b-116">Los complementos de DSP pueden permanecer cargados incluso cuando el usuario decide deshabilitarlos.</span><span class="sxs-lookup"><span data-stu-id="7875b-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="7875b-117">Cuando está deshabilitado, un complemento debe copiar los datos del búfer de entrada en el búfer de salida, realizando solo el procesamiento de la conversión de formato, si procede.</span><span class="sxs-lookup"><span data-stu-id="7875b-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="7875b-118">Windows Media Player también llama a este método antes de liberar una instancia del complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="7875b-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="7875b-119">Esto resulta útil para permitir que los clientes del complemento comprueben si el complemento está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="7875b-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="7875b-120">Por ejemplo, un complemento de la interfaz de usuario podría cambiar la apariencia de sus controles para avisar al usuario de que el complemento DSP no está conectado.</span><span class="sxs-lookup"><span data-stu-id="7875b-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7875b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7875b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7875b-122">**Interfaces necesarias**</span><span class="sxs-lookup"><span data-stu-id="7875b-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




