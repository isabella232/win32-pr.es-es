---
title: Historial de nivel de característica de DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104549202"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="c8bed-103">Historial de nivel de característica de DirectML</span><span class="sxs-lookup"><span data-stu-id="c8bed-103">DirectML feature level history</span></span>

<span data-ttu-id="c8bed-104">Para ver el historial de versiones de DirectML general, consulte [historial de versiones de DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c8bed-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="c8bed-105">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="c8bed-105">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="c8bed-106">Introducido en la versión de DirectML 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="c8bed-106">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="c8bed-107">Se ha agregado compatibilidad con los siguientes operadores.</span><span class="sxs-lookup"><span data-stu-id="c8bed-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="c8bed-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="c8bed-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="c8bed-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="c8bed-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="c8bed-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="c8bed-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="c8bed-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="c8bed-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="c8bed-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="c8bed-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="c8bed-115">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="c8bed-115">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="c8bed-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="c8bed-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="c8bed-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="c8bed-119">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-119">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="c8bed-120">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="c8bed-120">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="c8bed-121">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-121">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="c8bed-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="c8bed-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="c8bed-124">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-124">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="c8bed-125">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-125">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="c8bed-126">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-126">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="c8bed-127">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-127">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="c8bed-128">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="c8bed-128">Added the following enhancements.</span></span>

* <span data-ttu-id="c8bed-129">Se ha aumentado el número máximo de dimensiones de tensores de 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="c8bed-129">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="c8bed-130">Vea [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8bed-130">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="c8bed-131">Se ha agregado compatibilidad adicional con tipos de valores enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8bed-131">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="c8bed-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="c8bed-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="c8bed-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="c8bed-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="c8bed-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** y **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="c8bed-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="c8bed-135">**DML_OPERATOR_REDUCE**, cuando se usa **DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-135">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="c8bed-136">Se han agregado los siguientes tipos de datos de 64 bits y son compatibles con los operadores Select.</span><span class="sxs-lookup"><span data-stu-id="c8bed-136">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="c8bed-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="c8bed-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="c8bed-138">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="c8bed-138">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="c8bed-139">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="c8bed-139">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="c8bed-140">Funcionalidad desusada.</span><span class="sxs-lookup"><span data-stu-id="c8bed-140">Deprecated functionality.</span></span>

* <span data-ttu-id="c8bed-141">**DML_REDUCE_FUNCTION_ARGMAX** y **DML_REDUCE_FUNCTION_ARGMIN** han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="c8bed-141">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="c8bed-142">Prefiere usar los operadores independientes **DML_OPERATOR_ARGMIN** y **DML_OPERATOR_ARGMAX** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c8bed-142">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="c8bed-143">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="c8bed-143">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="c8bed-144">Introducido en la versión 1.2.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="c8bed-144">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="c8bed-145">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="c8bed-145">Added the following APIs.</span></span>

* [<span data-ttu-id="c8bed-146">Interfaz IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="c8bed-146">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="c8bed-147">Compatibilidad con gráficos de operador (vea [IDMLDevice1:: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="c8bed-147">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="c8bed-148">Se ha agregado compatibilidad con los siguientes operadores.</span><span class="sxs-lookup"><span data-stu-id="c8bed-148">Added support for the following operators.</span></span>

* <span data-ttu-id="c8bed-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="c8bed-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="c8bed-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="c8bed-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="c8bed-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="c8bed-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="c8bed-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="c8bed-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="c8bed-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="c8bed-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="c8bed-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="c8bed-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="c8bed-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="c8bed-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="c8bed-159">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="c8bed-159">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="c8bed-160">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="c8bed-160">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="c8bed-161">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="c8bed-161">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="c8bed-162">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="c8bed-162">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="c8bed-163">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-163">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="c8bed-164">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-164">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="c8bed-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="c8bed-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="c8bed-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="c8bed-168">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-168">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="c8bed-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="c8bed-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c8bed-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="c8bed-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="c8bed-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="c8bed-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="c8bed-173">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="c8bed-173">Added the following enhancements.</span></span>

* <span data-ttu-id="c8bed-174">Se ha agregado compatibilidad adicional con tipos de valores enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8bed-174">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="c8bed-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="c8bed-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="c8bed-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="c8bed-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="c8bed-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="c8bed-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="c8bed-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="c8bed-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="c8bed-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="c8bed-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="c8bed-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="c8bed-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="c8bed-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="c8bed-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="c8bed-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="c8bed-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c8bed-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="c8bed-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="c8bed-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="c8bed-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="c8bed-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="c8bed-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="c8bed-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="c8bed-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="c8bed-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="c8bed-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="c8bed-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="c8bed-194">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="c8bed-194">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="c8bed-195">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-195">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="c8bed-196">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-196">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="c8bed-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="c8bed-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="c8bed-199">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-199">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="c8bed-200">**DML_OPERATOR_TOP_K** y **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-200">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="c8bed-201">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-201">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="c8bed-202">**DML_OPERATOR_REDUCE**, cuando se usa una de las siguientes funciones de reducción.</span><span class="sxs-lookup"><span data-stu-id="c8bed-202">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="c8bed-203">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-203">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="c8bed-204">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-204">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="c8bed-205">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-205">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="c8bed-206">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-206">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="c8bed-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="c8bed-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="c8bed-208">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="c8bed-208">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="c8bed-209">Restricciones de forma tensores relajadas para **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-209">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="c8bed-210">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="c8bed-210">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="c8bed-211">Introducido en la versión 1.1.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="c8bed-211">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="c8bed-212">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="c8bed-212">Added the following APIs.</span></span>
* [<span data-ttu-id="c8bed-213">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="c8bed-213">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="c8bed-214">Enumeración DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="c8bed-214">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="c8bed-215">Consultas de nivel de característica (vea [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="c8bed-215">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="c8bed-216">Se ha agregado compatibilidad con los siguientes operadores.</span><span class="sxs-lookup"><span data-stu-id="c8bed-216">Added support for the following operators.</span></span>

* <span data-ttu-id="c8bed-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="c8bed-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="c8bed-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="c8bed-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="c8bed-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="c8bed-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="c8bed-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="c8bed-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="c8bed-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="c8bed-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="c8bed-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="c8bed-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="c8bed-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="c8bed-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="c8bed-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="c8bed-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="c8bed-229">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="c8bed-229">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="c8bed-230">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="c8bed-230">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="c8bed-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="c8bed-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="c8bed-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="c8bed-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="c8bed-233">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="c8bed-233">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="c8bed-234">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-234">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="c8bed-235">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="c8bed-235">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="c8bed-236">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="c8bed-236">Added the following enhancements.</span></span>

* <span data-ttu-id="c8bed-237">Al enlazar un recurso de entrada para el envío de un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), ahora es válido proporcionar un recurso con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (además de **D3D12_HEAP_TYPE_DEFAULT**), siempre y cuando también se establezcan las propiedades del montón adecuadas.</span><span class="sxs-lookup"><span data-stu-id="c8bed-237">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="c8bed-238">Consulte [enlace en DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="c8bed-238">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="c8bed-239">Los siguientes operadores booleanos lógicos ahora admiten decenas de salida de **UINT8** , además de la compatibilidad existente con **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="c8bed-239">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="c8bed-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="c8bed-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="c8bed-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="c8bed-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="c8bed-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="c8bed-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="c8bed-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="c8bed-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="c8bed-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="c8bed-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="c8bed-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="c8bed-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="c8bed-247">las funciones de activación de 5D ahora admiten el uso de los progresos en los idiomas de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="c8bed-247">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="c8bed-248">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="c8bed-248">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="c8bed-249">Nivel de características en el que se presentó DirectML.</span><span class="sxs-lookup"><span data-stu-id="c8bed-249">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8bed-250">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8bed-250">See also</span></span>

<span data-ttu-id="c8bed-251">Historial de versiones de [DirectML](./dml-version-history.md) 
 [Enumeración DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [DMLCreateDevice1 función](./directml/nf-directml-dmlcreatedevice1.md) 
 ) [Estructura de DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span><span class="sxs-lookup"><span data-stu-id="c8bed-251">[DirectML version history](./dml-version-history.md)
[DML_FEATURE_LEVEL enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
[DMLCreateDevice1 function](./directml/nf-directml-dmlcreatedevice1.md)
[DML_FEATURE_QUERY_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span></span>