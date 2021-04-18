---
description: La validación se realiza durante la compilación del efecto. Para validar la técnica actual, especifique NULL como el identificador de técnica que se va a validar.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714697"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="875aa-104">Validación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="875aa-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="875aa-105">La validación se realiza durante la compilación del efecto.</span><span class="sxs-lookup"><span data-stu-id="875aa-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="875aa-106">Para validar la técnica actual, especifique **null** como el identificador de técnica que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="875aa-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="875aa-107">Se producirá un error en la validación para cualquiera de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="875aa-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="875aa-108">Si el identificador de técnica especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="875aa-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="875aa-109">Si se produce un error en la aplicación de cualquier estado en cualquier paso de la técnica.</span><span class="sxs-lookup"><span data-stu-id="875aa-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="875aa-110">Si se produce un error en la validación del dispositivo después de la aplicación de todos los Estados en cualquier paso de la técnica.</span><span class="sxs-lookup"><span data-stu-id="875aa-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="875aa-111">Si los Estados de efecto u o VERTEXSHADER se asignan sombreadores no válidos en cualquier paso de la técnica.</span><span class="sxs-lookup"><span data-stu-id="875aa-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="875aa-112">Si las Cap del dispositivo no admiten la asignación de cubos y se asigna a un estado de efecto de textura un valor de tipo textureCUBE en cualquier paso de la técnica.</span><span class="sxs-lookup"><span data-stu-id="875aa-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="875aa-113">Si las Cap del dispositivo no admiten la asignación de volúmenes y se asigna a un estado de efecto de textura un valor de tipo texture3D en cualquier paso de la técnica.</span><span class="sxs-lookup"><span data-stu-id="875aa-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="875aa-114">Para obtener más información, vea [Estados de efectos (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="875aa-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="875aa-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="875aa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="875aa-116">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="875aa-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



