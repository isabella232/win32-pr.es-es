---
title: Historial de nivel de característica de DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521221"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="fdd6a-103">Historial de nivel de característica de DirectML</span><span class="sxs-lookup"><span data-stu-id="fdd6a-103">DirectML feature level history</span></span>

<span data-ttu-id="fdd6a-104">Para obtener información general sobre el historial de versiones de DirectML, [consulte Historial de versiones de DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="fdd6a-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="fdd6a-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="fdd6a-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="fdd6a-106">Se introdujo en la versión 1.5.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="fdd6a-107">Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="fdd6a-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="fdd6a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="fdd6a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="fdd6a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="fdd6a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="fdd6a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="fdd6a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="fdd6a-114">El número máximo de dimensiones admitidas para los operadores siguientes ha aumentado de 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="fdd6a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="fdd6a-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="fdd6a-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="fdd6a-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="fdd6a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="fdd6a-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="fdd6a-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="fdd6a-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="fdd6a-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="fdd6a-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="fdd6a-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="fdd6a-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="fdd6a-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="fdd6a-127">Se introdujo en la versión 1.4.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="fdd6a-128">Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="fdd6a-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="fdd6a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="fdd6a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="fdd6a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="fdd6a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="fdd6a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="fdd6a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="fdd6a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="fdd6a-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="fdd6a-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="fdd6a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="fdd6a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="fdd6a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="fdd6a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="fdd6a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="fdd6a-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="fdd6a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="fdd6a-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="fdd6a-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="fdd6a-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="fdd6a-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="fdd6a-149">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-149">Added the following enhancements.</span></span>

* <span data-ttu-id="fdd6a-150">El número máximo de dimensiones de tensor ha aumentado de 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="fdd6a-151">Vea [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fdd6a-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="fdd6a-152">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="fdd6a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="fdd6a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="fdd6a-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** y **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="fdd6a-156">**DML_OPERATOR_REDUCE**, cuando se **usa DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="fdd6a-157">Se han agregado los siguientes tipos de datos de 64 bits y son compatibles con operadores select.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="fdd6a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="fdd6a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="fdd6a-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="fdd6a-161">Funcionalidad en desuso.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-161">Deprecated functionality.</span></span>

* <span data-ttu-id="fdd6a-162">**DML_REDUCE_FUNCTION_ARGMAX** y **DML_REDUCE_FUNCTION_ARGMIN** han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="fdd6a-163">Debe preferir usar los operadores **DML_OPERATOR_ARGMIN** y **DML_OPERATOR_ARGMAX** independientes en su lugar.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="fdd6a-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="fdd6a-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="fdd6a-165">Se introdujo en la versión 1.2.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="fdd6a-166">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-166">Added the following APIs.</span></span>

* [<span data-ttu-id="fdd6a-167">Interfaz IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="fdd6a-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="fdd6a-168">Compatibilidad con gráficos de operadores [(vea IDMLDevice1::CompileGraph)](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="fdd6a-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="fdd6a-169">Se ha agregado compatibilidad con los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-169">Added support for the following operators.</span></span>

* <span data-ttu-id="fdd6a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="fdd6a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="fdd6a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="fdd6a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="fdd6a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="fdd6a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="fdd6a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="fdd6a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="fdd6a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="fdd6a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="fdd6a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="fdd6a-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="fdd6a-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="fdd6a-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="fdd6a-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="fdd6a-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="fdd6a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="fdd6a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="fdd6a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="fdd6a-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="fdd6a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="fdd6a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="fdd6a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="fdd6a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="fdd6a-194">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-194">Added the following enhancements.</span></span>

* <span data-ttu-id="fdd6a-195">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="fdd6a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="fdd6a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="fdd6a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="fdd6a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="fdd6a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="fdd6a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="fdd6a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="fdd6a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="fdd6a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="fdd6a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="fdd6a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="fdd6a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="fdd6a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="fdd6a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="fdd6a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="fdd6a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="fdd6a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="fdd6a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="fdd6a-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="fdd6a-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="fdd6a-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="fdd6a-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="fdd6a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="fdd6a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="fdd6a-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="fdd6a-221">**DML_OPERATOR_TOP_K** y **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="fdd6a-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="fdd6a-223">**DML_OPERATOR_REDUCE**, cuando se usa una de las siguientes funciones de reducción.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="fdd6a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="fdd6a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="fdd6a-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="fdd6a-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="fdd6a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="fdd6a-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="fdd6a-230">Restricciones de formas de tensor relajadas **para DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="fdd6a-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="fdd6a-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="fdd6a-232">Se introdujo en la versión 1.1.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="fdd6a-233">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-233">Added the following APIs.</span></span>
* [<span data-ttu-id="fdd6a-234">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="fdd6a-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="fdd6a-235">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="fdd6a-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="fdd6a-236">Consultas de nivel de característica (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="fdd6a-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="fdd6a-237">Se ha agregado compatibilidad con los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-237">Added support for the following operators.</span></span>

* <span data-ttu-id="fdd6a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="fdd6a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="fdd6a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="fdd6a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="fdd6a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="fdd6a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="fdd6a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="fdd6a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="fdd6a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="fdd6a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="fdd6a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="fdd6a-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="fdd6a-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="fdd6a-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="fdd6a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="fdd6a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="fdd6a-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="fdd6a-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="fdd6a-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="fdd6a-257">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-257">Added the following enhancements.</span></span>

* <span data-ttu-id="fdd6a-258">Al enlazar un recurso de entrada para el envío de un [IDMLOperatorInitializer,](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)ahora es legal proporcionar un recurso con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (además de **D3D12_HEAP_TYPE_DEFAULT**), siempre que también se establezcan las propiedades de montón adecuadas.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="fdd6a-259">Vea [Enlace en DirectML.](./dml-binding.md)</span><span class="sxs-lookup"><span data-stu-id="fdd6a-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="fdd6a-260">Los siguientes operadores booleanos lógicos ahora admiten tensores de salida **UINT8,** además de la compatibilidad existente con **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="fdd6a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="fdd6a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="fdd6a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="fdd6a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="fdd6a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="fdd6a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="fdd6a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="fdd6a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="fdd6a-268">Las funciones de activación 5D ahora admiten el uso de strides en sus tensores de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="fdd6a-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="fdd6a-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="fdd6a-270">Nivel de característica en el que se introdujo DirectML.</span><span class="sxs-lookup"><span data-stu-id="fdd6a-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdd6a-271">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdd6a-271">See also</span></span>

* [<span data-ttu-id="fdd6a-272">Historial de versiones de DirectML</span><span class="sxs-lookup"><span data-stu-id="fdd6a-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="fdd6a-273">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="fdd6a-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="fdd6a-274">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="fdd6a-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="fdd6a-275">DML_FEATURE_QUERY_FEATURE_LEVELS estructura</span><span class="sxs-lookup"><span data-stu-id="fdd6a-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
