---
title: 'Texture2DMS:: Load (int, int) (función)'
description: 'Obtiene un valor. | Texture2DMS:: Load (int, int) (función)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Función de carga de DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986455"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="c1c4d-105">Texture2DMS:: Load (int, int) (función)</span><span class="sxs-lookup"><span data-stu-id="c1c4d-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="c1c4d-106">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c4d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1c4d-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="c1c4d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1c4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c4d-109">*coordenadas* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1c4d-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4d-110">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="c1c4d-110">Type: **int2**</span></span>

<span data-ttu-id="c1c4d-111">Ubicación de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="c1c4d-112">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1c4d-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c4d-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c1c4d-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c1c4d-114">Índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c4d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1c4d-115">Return value</span></span>

<span data-ttu-id="c1c4d-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="c1c4d-116">Type: **T**</span></span>

<span data-ttu-id="c1c4d-117">Un valor, cuyo tipo coincide con el tipo de plantilla de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c4d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1c4d-118">Remarks</span></span>

<span data-ttu-id="c1c4d-119">Esta es una lista de las versiones sobrecargadas de este método.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="c1c4d-120">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c1c4d-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c1c4d-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="c1c4d-121">Vertex</span></span> | <span data-ttu-id="c1c4d-122">Casco</span><span class="sxs-lookup"><span data-stu-id="c1c4d-122">Hull</span></span> | <span data-ttu-id="c1c4d-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="c1c4d-123">Domain</span></span> | <span data-ttu-id="c1c4d-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="c1c4d-124">Geometry</span></span> | <span data-ttu-id="c1c4d-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="c1c4d-125">Pixel</span></span> | <span data-ttu-id="c1c4d-126">Compute</span><span class="sxs-lookup"><span data-stu-id="c1c4d-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c1c4d-127">x</span><span class="sxs-lookup"><span data-stu-id="c1c4d-127">x</span></span>     | <span data-ttu-id="c1c4d-128">x</span><span class="sxs-lookup"><span data-stu-id="c1c4d-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c1c4d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c4d-130">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="c1c4d-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="c1c4d-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c1c4d-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
