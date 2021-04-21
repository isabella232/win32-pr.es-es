---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Calcula la arcotangente de 2 argumentos para cada elemento de *ATensor* y *BTensor,* donde *ATensor* es el eje *Y* y *BTensor* es el eje *X,* colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804495"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="4a40b-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4a40b-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="4a40b-104">Calcula la arcotangente de 2 argumentos para cada elemento de *ATensor* y *BTensor,* donde *ATensor* es el eje *Y* y *BTensor* es el eje *X,* colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4a40b-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="4a40b-105">Este operador no está definido para el origen (es decir, cuando *ATensor* y *BTensor* son 0 para los elementos correspondientes).</span><span class="sxs-lookup"><span data-stu-id="4a40b-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="4a40b-107">Este operador admite la ejecución en contexto, lo que significa que se permite al tensor de salida el alias *ATensor* o *BTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="4a40b-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a40b-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="4a40b-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="4a40b-109">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4a40b-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a40b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a40b-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="4a40b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a40b-111">Members</span></span>

`ATensor`

<span data-ttu-id="4a40b-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4a40b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4a40b-113">Tensor de entrada del que se leerán los valores del eje Y.</span><span class="sxs-lookup"><span data-stu-id="4a40b-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="4a40b-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4a40b-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4a40b-115">Tensor de entrada del que se leerán los valores del eje X.</span><span class="sxs-lookup"><span data-stu-id="4a40b-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="4a40b-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4a40b-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4a40b-117">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="4a40b-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="4a40b-118">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="4a40b-118">Availability</span></span>
<span data-ttu-id="4a40b-119">Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="4a40b-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4a40b-120">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-120">Tensor constraints</span></span>
<span data-ttu-id="4a40b-121">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *DataType,* *DimensionCount* y *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="4a40b-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4a40b-122">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-122">Tensor support</span></span>
| <span data-ttu-id="4a40b-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-123">Tensor</span></span> | <span data-ttu-id="4a40b-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a40b-124">Kind</span></span> | <span data-ttu-id="4a40b-125">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="4a40b-125">Supported dimension counts</span></span> | <span data-ttu-id="4a40b-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="4a40b-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4a40b-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-127">ATensor</span></span> | <span data-ttu-id="4a40b-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a40b-128">Input</span></span> | <span data-ttu-id="4a40b-129">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4a40b-129">1 to 8</span></span> | <span data-ttu-id="4a40b-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4a40b-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4a40b-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-131">BTensor</span></span> | <span data-ttu-id="4a40b-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="4a40b-132">Input</span></span> | <span data-ttu-id="4a40b-133">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4a40b-133">1 to 8</span></span> | <span data-ttu-id="4a40b-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4a40b-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4a40b-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4a40b-135">OutputTensor</span></span> | <span data-ttu-id="4a40b-136">Resultados</span><span class="sxs-lookup"><span data-stu-id="4a40b-136">Output</span></span> | <span data-ttu-id="4a40b-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4a40b-137">1 to 8</span></span> | <span data-ttu-id="4a40b-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4a40b-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="4a40b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a40b-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4a40b-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="4a40b-140">**Header**</span></span> | <span data-ttu-id="4a40b-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="4a40b-141">directml.h</span></span> |
