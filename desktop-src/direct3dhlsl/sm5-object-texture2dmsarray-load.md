---
title: 'Texture2DMSArray:: Load (int, int) (función)'
description: 'Obtiene un valor. | Texture2DMSArray:: Load (int, int) (función)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003711"
---
# <a name="texture2dmsarrayloadintint-function"></a><span data-ttu-id="5ea6b-105">Texture2DMSArray:: Load (int, int) (función)</span><span class="sxs-lookup"><span data-stu-id="5ea6b-105">Texture2DMSArray::Load(int,int) function</span></span>

<span data-ttu-id="5ea6b-106">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea6b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea6b-107">Syntax</span></span>

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="5ea6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea6b-109">*coordenadas* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ea6b-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6b-110">Tipo: **INT3**</span><span class="sxs-lookup"><span data-stu-id="5ea6b-110">Type: **int3**</span></span>

<span data-ttu-id="5ea6b-111">Ubicación de entrada.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="5ea6b-112">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ea6b-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6b-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5ea6b-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5ea6b-114">Índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea6b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea6b-115">Return value</span></span>

<span data-ttu-id="5ea6b-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="5ea6b-116">Type: **T**</span></span>

<span data-ttu-id="5ea6b-117">Un valor, cuyo tipo coincide con el tipo de plantilla de textura.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea6b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea6b-118">Remarks</span></span>

<span data-ttu-id="5ea6b-119">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="5ea6b-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="5ea6b-120">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5ea6b-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5ea6b-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="5ea6b-121">Vertex</span></span> | <span data-ttu-id="5ea6b-122">Casco</span><span class="sxs-lookup"><span data-stu-id="5ea6b-122">Hull</span></span> | <span data-ttu-id="5ea6b-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="5ea6b-123">Domain</span></span> | <span data-ttu-id="5ea6b-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="5ea6b-124">Geometry</span></span> | <span data-ttu-id="5ea6b-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="5ea6b-125">Pixel</span></span> | <span data-ttu-id="5ea6b-126">Compute</span><span class="sxs-lookup"><span data-stu-id="5ea6b-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5ea6b-127">x</span><span class="sxs-lookup"><span data-stu-id="5ea6b-127">x</span></span>     | <span data-ttu-id="5ea6b-128">x</span><span class="sxs-lookup"><span data-stu-id="5ea6b-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5ea6b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea6b-130">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="5ea6b-130">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="5ea6b-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5ea6b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
