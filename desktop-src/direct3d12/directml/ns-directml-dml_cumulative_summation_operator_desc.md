---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Suma los elementos de una tensores a lo largo de un eje, escribiendo el recuento de ejecución de la suma en el tensores de salida.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721288"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="da078-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="da078-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="da078-104">Suma los elementos de una tensores a lo largo de un eje, escribiendo el recuento de ejecución de la suma en el tensores de salida.</span><span class="sxs-lookup"><span data-stu-id="da078-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da078-105">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="da078-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="da078-106">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="da078-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da078-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da078-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="da078-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="da078-108">Members</span></span>

`InputTensor`

<span data-ttu-id="da078-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="da078-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="da078-110">Tensores de entrada que contiene los elementos que se van a sumar.</span><span class="sxs-lookup"><span data-stu-id="da078-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="da078-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="da078-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="da078-112">Tensores de salida en el que se van a escribir las sumas acumulativas resultantes.</span><span class="sxs-lookup"><span data-stu-id="da078-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="da078-113">Este tensores debe tener los mismos tamaños y tipo de datos que *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="da078-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="da078-114">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="da078-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="da078-115">Índice de la dimensión de la que se van a sumar los elementos.</span><span class="sxs-lookup"><span data-stu-id="da078-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="da078-116">Este valor debe ser menor que el valor de *DimensionCount* de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="da078-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="da078-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="da078-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="da078-118">Uno de los valores de la enumeración [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="da078-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="da078-119">Si se establece en **DML_AXIS_DIRECTION_INCREASING**, la suma se produce recorriendo el tensores a lo largo del eje especificado por el índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="da078-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="da078-120">Si se establece en **DML_AXIS_DIRECTION_DECREASING**, el valor de inverso es true y la suma se produce recorriendo los elementos por índice descendente.</span><span class="sxs-lookup"><span data-stu-id="da078-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="da078-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da078-121">Remarks</span></span>
<span data-ttu-id="da078-122">Este operador es compatible con la ejecución en contexto, lo que significa que se permite que el *OutputTensor* alias del *InputTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="da078-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="da078-123">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="da078-123">Availability</span></span>
<span data-ttu-id="da078-124">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="da078-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="da078-125">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="da078-125">Tensor constraints</span></span>
<span data-ttu-id="da078-126">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="da078-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="da078-127">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="da078-127">Tensor support</span></span>
| <span data-ttu-id="da078-128">Tensores</span><span class="sxs-lookup"><span data-stu-id="da078-128">Tensor</span></span> | <span data-ttu-id="da078-129">Clase</span><span class="sxs-lookup"><span data-stu-id="da078-129">Kind</span></span> | <span data-ttu-id="da078-130">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="da078-130">Supported dimension counts</span></span> | <span data-ttu-id="da078-131">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="da078-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="da078-132">InputTensor</span><span class="sxs-lookup"><span data-stu-id="da078-132">InputTensor</span></span> | <span data-ttu-id="da078-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="da078-133">Input</span></span> | <span data-ttu-id="da078-134">4</span><span class="sxs-lookup"><span data-stu-id="da078-134">4</span></span> | <span data-ttu-id="da078-135">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="da078-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="da078-136">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="da078-136">OutputTensor</span></span> | <span data-ttu-id="da078-137">Output</span><span class="sxs-lookup"><span data-stu-id="da078-137">Output</span></span> | <span data-ttu-id="da078-138">4</span><span class="sxs-lookup"><span data-stu-id="da078-138">4</span></span> | <span data-ttu-id="da078-139">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="da078-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="da078-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da078-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="da078-141">**Header**</span><span class="sxs-lookup"><span data-stu-id="da078-141">**Header**</span></span> | <span data-ttu-id="da078-142">directml. h</span><span class="sxs-lookup"><span data-stu-id="da078-142">directml.h</span></span> |