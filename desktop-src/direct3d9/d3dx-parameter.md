---
description: Estas marcas proporcionan información adicional sobre los parámetros de efecto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718273"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="53b07-103">\_Parámetro D3DX</span><span class="sxs-lookup"><span data-stu-id="53b07-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="53b07-104">Estas marcas proporcionan información adicional sobre los parámetros de efecto.</span><span class="sxs-lookup"><span data-stu-id="53b07-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="53b07-105">[**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)usa las constantes de parámetro Effect.</span><span class="sxs-lookup"><span data-stu-id="53b07-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="53b07-106">Constante</span><span class="sxs-lookup"><span data-stu-id="53b07-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="53b07-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="53b07-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="53b07-108"><dt>**\_Anotación del parámetro D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53b07-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="53b07-109">Este parámetro se marca como una anotación.</span><span class="sxs-lookup"><span data-stu-id="53b07-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="53b07-110">Consulte [Agregar información a los parámetros de efectos con anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="53b07-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="53b07-111"><dt>**\_Literal de parámetro de D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53b07-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="53b07-112">Este parámetro se marca como un valor literal.</span><span class="sxs-lookup"><span data-stu-id="53b07-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="53b07-113">Los parámetros literales no pueden cambiar después de la compilación, lo que permite al compilador optimizar su uso.</span><span class="sxs-lookup"><span data-stu-id="53b07-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="53b07-114">Los parámetros compartidos no se pueden marcar como literal.</span><span class="sxs-lookup"><span data-stu-id="53b07-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="53b07-115">Vea [usos y literales (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="53b07-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="53b07-116"><dt>**Parámetro de D3DX \_ \_ compartido**</dt></span><span class="sxs-lookup"><span data-stu-id="53b07-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="53b07-117">Todos los efectos del mismo espacio de nombres compartirán el valor de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="53b07-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="53b07-118">Cambiar el valor de un efecto lo cambiará en todos los efectos compartidos.</span><span class="sxs-lookup"><span data-stu-id="53b07-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="53b07-119">Consulte [uso compartido de parámetros](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="53b07-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="53b07-120">**D3DX \_ Los parámetros \_ compartidos** no se pueden combinar con el **literal de \_ parámetro \_ de d3dx** o la **\_ \_ anotación de parámetro d3dx**.</span><span class="sxs-lookup"><span data-stu-id="53b07-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53b07-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53b07-121">Requirements</span></span>



| <span data-ttu-id="53b07-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="53b07-122">Requirement</span></span> | <span data-ttu-id="53b07-123">Value</span><span class="sxs-lookup"><span data-stu-id="53b07-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b07-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53b07-124">Header</span></span><br/> | <dl> <span data-ttu-id="53b07-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b07-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b07-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="53b07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b07-127">Constantes de efecto</span><span class="sxs-lookup"><span data-stu-id="53b07-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




