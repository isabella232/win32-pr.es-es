---
title: Modificar la página de propiedades de ejemplo echo
description: Modificar la página de propiedades de ejemplo echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418578"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="7a226-108">Modificar la página de propiedades de ejemplo echo</span><span class="sxs-lookup"><span data-stu-id="7a226-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="7a226-109">La implementación de la página de propiedades predeterminada que proporciona el ejemplo de complemento DSP del Asistente para complementos de Windows Media Player contiene un único control de cuadro de edición que recibe el factor de escala del usuario.</span><span class="sxs-lookup"><span data-stu-id="7a226-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="7a226-110">Debe modificar la página de propiedades para recibir los dos valores de propiedad que usa el ejemplo echo.</span><span class="sxs-lookup"><span data-stu-id="7a226-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="7a226-111">Para obtener información general sobre las páginas de propiedades del complemento DSP, vea [implementar un complemento de DSP de audio](implementing-an-audio-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="7a226-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="7a226-112">Las secciones siguientes le guían por el proceso de modificación de la página de propiedades de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7a226-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="7a226-113">Modificar el recurso de cuadro de diálogo echo</span><span class="sxs-lookup"><span data-stu-id="7a226-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="7a226-114">Agregar y modificar eventos</span><span class="sxs-lookup"><span data-stu-id="7a226-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="7a226-115">Cómo el ejemplo echo conserva los datos</span><span class="sxs-lookup"><span data-stu-id="7a226-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="7a226-116">Implementar CEchoPropPage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="7a226-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="7a226-117">Implementación de CEchoPropPage:: Apply</span><span class="sxs-lookup"><span data-stu-id="7a226-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="7a226-118">Implementación de CEcho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="7a226-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="7a226-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a226-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a226-120">**El ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="7a226-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




