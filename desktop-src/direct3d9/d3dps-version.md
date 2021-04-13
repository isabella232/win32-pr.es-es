---
description: Cree un token de versión del sombreador de píxeles.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362609"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="39649-103">D3DPS \_ versión (macro)</span><span class="sxs-lookup"><span data-stu-id="39649-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="39649-104">Cree un token de versión del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39649-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="39649-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39649-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="39649-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39649-107">*\_Principales*</span><span class="sxs-lookup"><span data-stu-id="39649-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="39649-108">Versión principal del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39649-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="39649-109">*\_Minor*</span><span class="sxs-lookup"><span data-stu-id="39649-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="39649-110">Versión secundaria del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39649-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39649-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39649-111">Return value</span></span>

<span data-ttu-id="39649-112">Devuelve un valor DWORD que es una versión de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39649-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="39649-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39649-113">Remarks</span></span>

<span data-ttu-id="39649-114">Números de versión</span><span class="sxs-lookup"><span data-stu-id="39649-114">Version Numbers</span></span>

<span data-ttu-id="39649-115">El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices secundarios.</span><span class="sxs-lookup"><span data-stu-id="39649-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="39649-116">Los números válidos se muestran en la tabla.</span><span class="sxs-lookup"><span data-stu-id="39649-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="39649-117">Principal</span><span class="sxs-lookup"><span data-stu-id="39649-117">Major</span></span> | <span data-ttu-id="39649-118">Minor</span><span class="sxs-lookup"><span data-stu-id="39649-118">Minor</span></span> | <span data-ttu-id="39649-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39649-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="39649-120">1</span><span class="sxs-lookup"><span data-stu-id="39649-120">1</span></span>     | <span data-ttu-id="39649-121">1</span><span class="sxs-lookup"><span data-stu-id="39649-121">1</span></span>     | <span data-ttu-id="39649-122">\_Versión de D3DPS (1,1)</span><span class="sxs-lookup"><span data-stu-id="39649-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="39649-123">1</span><span class="sxs-lookup"><span data-stu-id="39649-123">1</span></span>     | <span data-ttu-id="39649-124">2</span><span class="sxs-lookup"><span data-stu-id="39649-124">2</span></span>     | <span data-ttu-id="39649-125">\_Versión de D3DPS (1,2)</span><span class="sxs-lookup"><span data-stu-id="39649-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="39649-126">1</span><span class="sxs-lookup"><span data-stu-id="39649-126">1</span></span>     | <span data-ttu-id="39649-127">3</span><span class="sxs-lookup"><span data-stu-id="39649-127">3</span></span>     | <span data-ttu-id="39649-128">\_Versión de D3DPS (1,1)</span><span class="sxs-lookup"><span data-stu-id="39649-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="39649-129">1</span><span class="sxs-lookup"><span data-stu-id="39649-129">1</span></span>     | <span data-ttu-id="39649-130">4</span><span class="sxs-lookup"><span data-stu-id="39649-130">4</span></span>     | <span data-ttu-id="39649-131">\_Versión de D3DPS (1,1)</span><span class="sxs-lookup"><span data-stu-id="39649-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="39649-132">2</span><span class="sxs-lookup"><span data-stu-id="39649-132">2</span></span>     | <span data-ttu-id="39649-133">0</span><span class="sxs-lookup"><span data-stu-id="39649-133">0</span></span>     | <span data-ttu-id="39649-134">\_Versión de D3DPS (2,0)</span><span class="sxs-lookup"><span data-stu-id="39649-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="39649-135">3</span><span class="sxs-lookup"><span data-stu-id="39649-135">3</span></span>     | <span data-ttu-id="39649-136">0</span><span class="sxs-lookup"><span data-stu-id="39649-136">0</span></span>     | <span data-ttu-id="39649-137">\_Versión de D3DPS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="39649-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="39649-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39649-138">Requirements</span></span>



| <span data-ttu-id="39649-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="39649-139">Requirement</span></span> | <span data-ttu-id="39649-140">Value</span><span class="sxs-lookup"><span data-stu-id="39649-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39649-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39649-141">Header</span></span><br/> | <dl> <span data-ttu-id="39649-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="39649-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39649-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="39649-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39649-144">Macros</span><span class="sxs-lookup"><span data-stu-id="39649-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="39649-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="39649-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




