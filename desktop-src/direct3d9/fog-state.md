---
description: Los efectos de niebla pueden dar mayor realismo a una escena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422732"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="4cd91-103">Estado de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4cd91-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="4cd91-104">Los efectos de niebla pueden dar mayor realismo a una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="4cd91-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="4cd91-105">Puede usar efectos de niebla para más que simular la niebla.</span><span class="sxs-lookup"><span data-stu-id="4cd91-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="4cd91-106">También pueden reducir la claridad de una escena con distancia.</span><span class="sxs-lookup"><span data-stu-id="4cd91-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="4cd91-107">Esto refleja lo que sucede en el mundo real; a medida que los objetos van más alejados del usuario, sus detalles son menos distintos.</span><span class="sxs-lookup"><span data-stu-id="4cd91-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="4cd91-108">Para obtener más información sobre el uso de la niebla en la aplicación, vea [niebla (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="4cd91-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="4cd91-109">Una aplicación de C++ controla la niebla a través de los Estados de representación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4cd91-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="4cd91-110">El tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye los Estados para controlar si se usa la niebla de píxel (tabla) o de vértices, el color que tiene, la fórmula de niebla que aplica el sistema y los parámetros de la fórmula.</span><span class="sxs-lookup"><span data-stu-id="4cd91-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="4cd91-111">Para habilitar la niebla, establezca el \_ Estado de representación de FOGENABLE de D3DRS en **true**.</span><span class="sxs-lookup"><span data-stu-id="4cd91-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="4cd91-112">El color de niebla se puede establecer en cualquier valor de color mediante el \_ Estado de representación de D3DRS FOGCOLOR; se omite el componente alfa del color de niebla.</span><span class="sxs-lookup"><span data-stu-id="4cd91-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="4cd91-113">Los \_ Estados de representación D3DRS FOGTABLEMODE y D3DRS \_ FOGVERTEXMODE controlan la fórmula de niebla aplicada para los cálculos de niebla y controlan indirectamente qué tipo de niebla se aplica.</span><span class="sxs-lookup"><span data-stu-id="4cd91-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="4cd91-114">Ambos Estados de representación se pueden establecer en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd91-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="4cd91-115">Al establecer el estado de representación en D3DFOG \_ None, se deshabilita la niebla de píxel o de vértices, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4cd91-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="4cd91-116">Si ambos Estados de representación están establecidos en modos válidos, el sistema aplica solo los efectos de niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4cd91-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="4cd91-117">Los \_ \_ parámetros de la fórmula de niebla de control D3DRS FOGSTART y D3DRS FOGEND para el \_ modo lineal D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="4cd91-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="4cd91-118">El estado de representación de D3DRS \_ FOGDENSITY controla la densidad de niebla en los modos de niebla exponencial.</span><span class="sxs-lookup"><span data-stu-id="4cd91-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="4cd91-119">Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4cd91-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cd91-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cd91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd91-121">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="4cd91-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
