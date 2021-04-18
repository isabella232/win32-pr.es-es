---
description: Cree un token de número de versión del sombreador de vértices.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718311"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="f06e4-103">D3DVS \_ versión (macro)</span><span class="sxs-lookup"><span data-stu-id="f06e4-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="f06e4-104">Cree un token de número de versión del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f06e4-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f06e4-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="f06e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f06e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f06e4-107">*\_Principales*</span><span class="sxs-lookup"><span data-stu-id="f06e4-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="f06e4-108">Versión principal del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f06e4-108">The major vertex shader version.</span></span> <span data-ttu-id="f06e4-109">Vea la sección Comentarios para obtener los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="f06e4-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="f06e4-110">*\_Minor*</span><span class="sxs-lookup"><span data-stu-id="f06e4-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="f06e4-111">Versión secundaria del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f06e4-111">The minor vertex shader version.</span></span> <span data-ttu-id="f06e4-112">Vea la sección Comentarios para obtener los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="f06e4-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f06e4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f06e4-113">Return value</span></span>

<span data-ttu-id="f06e4-114">Devuelve un valor DWORD que es una versión del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="f06e4-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="f06e4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f06e4-115">Remarks</span></span>

<span data-ttu-id="f06e4-116">Números de versión</span><span class="sxs-lookup"><span data-stu-id="f06e4-116">Version Numbers</span></span>

<span data-ttu-id="f06e4-117">El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices secundarios.</span><span class="sxs-lookup"><span data-stu-id="f06e4-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="f06e4-118">Los números válidos se muestran en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f06e4-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="f06e4-119">Principal</span><span class="sxs-lookup"><span data-stu-id="f06e4-119">Major</span></span> | <span data-ttu-id="f06e4-120">Minor</span><span class="sxs-lookup"><span data-stu-id="f06e4-120">Minor</span></span> | <span data-ttu-id="f06e4-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f06e4-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="f06e4-122">1</span><span class="sxs-lookup"><span data-stu-id="f06e4-122">1</span></span>     | <span data-ttu-id="f06e4-123">1</span><span class="sxs-lookup"><span data-stu-id="f06e4-123">1</span></span>     | <span data-ttu-id="f06e4-124">\_Versión de D3DVS (1,1)</span><span class="sxs-lookup"><span data-stu-id="f06e4-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="f06e4-125">2</span><span class="sxs-lookup"><span data-stu-id="f06e4-125">2</span></span>     | <span data-ttu-id="f06e4-126">0</span><span class="sxs-lookup"><span data-stu-id="f06e4-126">0</span></span>     | <span data-ttu-id="f06e4-127">\_Versión de D3DVS (2,0)</span><span class="sxs-lookup"><span data-stu-id="f06e4-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="f06e4-128">3</span><span class="sxs-lookup"><span data-stu-id="f06e4-128">3</span></span>     | <span data-ttu-id="f06e4-129">0</span><span class="sxs-lookup"><span data-stu-id="f06e4-129">0</span></span>     | <span data-ttu-id="f06e4-130">\_Versión de D3DVS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="f06e4-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f06e4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f06e4-131">Requirements</span></span>



| <span data-ttu-id="f06e4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f06e4-132">Requirement</span></span> | <span data-ttu-id="f06e4-133">Value</span><span class="sxs-lookup"><span data-stu-id="f06e4-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f06e4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f06e4-134">Header</span></span><br/> | <dl> <span data-ttu-id="f06e4-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f06e4-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f06e4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f06e4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06e4-137">Macros</span><span class="sxs-lookup"><span data-stu-id="f06e4-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




