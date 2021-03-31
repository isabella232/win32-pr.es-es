---
title: Error de D1109 Draw
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Error en una llamada a Draw por un destino de representación
keywords:
- Error de D1109 Draw Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793708"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="e550e-104">D1109: error de dibujo</span><span class="sxs-lookup"><span data-stu-id="e550e-104">D1109: Draw Failure</span></span>

<span data-ttu-id="e550e-105">Una llamada a Draw de un recurso de destino de representación produjo un error \[  \] .</span><span class="sxs-lookup"><span data-stu-id="e550e-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="e550e-106">Tags \[ *TAG1*, *etiqueta2* \] .</span><span class="sxs-lookup"><span data-stu-id="e550e-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="e550e-107">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="e550e-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="e550e-108"><span id="resource"></span><span id="RESOURCE"></span>*recurso*</span><span class="sxs-lookup"><span data-stu-id="e550e-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="e550e-109">Dirección del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="e550e-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="e550e-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="e550e-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="e550e-111">El primer valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="e550e-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="e550e-112"><span id="tag2"></span><span id="TAG2"></span>*etiqueta2*</span><span class="sxs-lookup"><span data-stu-id="e550e-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="e550e-113">El segundo valor de etiqueta (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="e550e-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="e550e-114">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="e550e-114">Error Level</span></span> | <span data-ttu-id="e550e-115">Advertencia</span><span class="sxs-lookup"><span data-stu-id="e550e-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="e550e-116">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="e550e-116">Possible Causes</span></span>

<span data-ttu-id="e550e-117">Hay muchas razones por las que se puede producir un error en una llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="e550e-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="e550e-118">Para obtener más información, consulte la documentación del SDK de Direct2D para el método en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="e550e-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 