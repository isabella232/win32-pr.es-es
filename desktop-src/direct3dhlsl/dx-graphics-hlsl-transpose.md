---
title: transponer
description: Transpone la matriz de entrada especificada.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- transponer HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420824"
---
# <a name="transpose"></a><span data-ttu-id="950d0-104">transponer</span><span class="sxs-lookup"><span data-stu-id="950d0-104">transpose</span></span>

<span data-ttu-id="950d0-105">Transpone la matriz de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="950d0-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="950d0-106">RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="950d0-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="950d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="950d0-107">Parameters</span></span>



| <span data-ttu-id="950d0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="950d0-108">Item</span></span>                                                   | <span data-ttu-id="950d0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="950d0-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="950d0-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="950d0-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="950d0-111">\[en \] la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="950d0-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="950d0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="950d0-112">Return Value</span></span>

<span data-ttu-id="950d0-113">Valor transpuesto del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="950d0-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="950d0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="950d0-114">Remarks</span></span>

<span data-ttu-id="950d0-115">Si las dimensiones de la matriz de origen son *columnas* de *filas* , la matriz resultante es *filas* de *columnas* .</span><span class="sxs-lookup"><span data-stu-id="950d0-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="950d0-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="950d0-116">Type Description</span></span>



| <span data-ttu-id="950d0-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="950d0-117">Name</span></span> | [<span data-ttu-id="950d0-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="950d0-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="950d0-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="950d0-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="950d0-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="950d0-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="950d0-121">*x*</span><span class="sxs-lookup"><span data-stu-id="950d0-121">*x*</span></span>  | [<span data-ttu-id="950d0-122">**matrices**</span><span class="sxs-lookup"><span data-stu-id="950d0-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="950d0-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="950d0-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="950d0-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="950d0-124">any</span></span>                                                                                    |
| <span data-ttu-id="950d0-125">direcc</span><span class="sxs-lookup"><span data-stu-id="950d0-125">ret</span></span>  | [<span data-ttu-id="950d0-126">**matrices**</span><span class="sxs-lookup"><span data-stu-id="950d0-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="950d0-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="950d0-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="950d0-128">filas = el mismo número de columnas que la entrada *x*, columnas = el mismo número de filas que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="950d0-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="950d0-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="950d0-129">Minimum Shader Model</span></span>

<span data-ttu-id="950d0-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="950d0-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="950d0-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="950d0-131">Shader Model</span></span>                                                                       | <span data-ttu-id="950d0-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="950d0-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="950d0-133">Modelador [modelo 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="950d0-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="950d0-134">sí</span><span class="sxs-lookup"><span data-stu-id="950d0-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="950d0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="950d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950d0-136">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="950d0-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

