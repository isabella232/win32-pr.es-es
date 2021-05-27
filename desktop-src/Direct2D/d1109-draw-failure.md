---
title: Error de dibujo D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Error al llamar a Draw de un destino de representación
keywords:
- Error de dibujo D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549970"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="add03-104">D1109: Error de dibujo</span><span class="sxs-lookup"><span data-stu-id="add03-104">D1109: Draw Failure</span></span>

<span data-ttu-id="add03-105">Error al llamar a Draw de un recurso de destino de \[ *representación.* \]</span><span class="sxs-lookup"><span data-stu-id="add03-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="add03-106">Etiquetas \[ *tag1,* *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="add03-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="add03-107">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="add03-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="add03-108"><span id="resource"></span><span id="RESOURCE"></span>*Recursos*</span><span class="sxs-lookup"><span data-stu-id="add03-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="add03-109">Dirección del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="add03-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="add03-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="add03-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="add03-111">Primer valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) más para obtener información).</span><span class="sxs-lookup"><span data-stu-id="add03-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="add03-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="add03-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="add03-113">Segundo valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) más para obtener información).</span><span class="sxs-lookup"><span data-stu-id="add03-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="add03-114">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="add03-114">Error Level</span></span> | <span data-ttu-id="add03-115">Advertencia</span><span class="sxs-lookup"><span data-stu-id="add03-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="add03-116">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="add03-116">Possible Causes</span></span>

<span data-ttu-id="add03-117">Hay muchas razones por las que una llamada a Draw podría producir un error.</span><span class="sxs-lookup"><span data-stu-id="add03-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="add03-118">Para obtener más información, consulte la documentación del SDK de Direct2D para el método que ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="add03-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 