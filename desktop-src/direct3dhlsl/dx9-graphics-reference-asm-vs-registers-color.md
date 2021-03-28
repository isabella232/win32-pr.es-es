---
title: Registro de color
description: Estos registros de salida del sombreador de vértices contienen un valor de color.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104361773"
---
# <a name="color-register"></a><span data-ttu-id="6c077-103">Registro de color</span><span class="sxs-lookup"><span data-stu-id="6c077-103">Color Register</span></span>

<span data-ttu-id="6c077-104">Estos registros de salida del sombreador de vértices contienen un valor de color.</span><span class="sxs-lookup"><span data-stu-id="6c077-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="6c077-105">Registrarse</span><span class="sxs-lookup"><span data-stu-id="6c077-105">Register</span></span> | <span data-ttu-id="6c077-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c077-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="6c077-107">oD0</span><span class="sxs-lookup"><span data-stu-id="6c077-107">oD0</span></span>      | <span data-ttu-id="6c077-108">registro de color difuso.</span><span class="sxs-lookup"><span data-stu-id="6c077-108">diffuse color register.</span></span>  |
| <span data-ttu-id="6c077-109">oD1</span><span class="sxs-lookup"><span data-stu-id="6c077-109">oD1</span></span>      | <span data-ttu-id="6c077-110">registro de color especular.</span><span class="sxs-lookup"><span data-stu-id="6c077-110">specular color register.</span></span> |



 

<span data-ttu-id="6c077-111">El valor oD0 se interpola y se escribe en el registro de color del sombreador de píxeles 0 (V0).</span><span class="sxs-lookup"><span data-stu-id="6c077-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="6c077-112">El valor oD1 se interpola y se escribe en el registro de color del sombreador de píxeles 1 (V1).</span><span class="sxs-lookup"><span data-stu-id="6c077-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="6c077-113">Para obtener más información sobre los registros de color del sombreador de píxeles, vea el tema [registro del color de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6c077-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c077-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c077-114">Remarks</span></span>

<span data-ttu-id="6c077-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c077-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="6c077-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c077-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c077-117">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="6c077-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




