---
title: Historial de nivel de característica de DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: fdc489184b3220afd0b8c75738fa1d40de207c8d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387054"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="34bfb-103">Historial de nivel de característica de DirectML</span><span class="sxs-lookup"><span data-stu-id="34bfb-103">DirectML feature level history</span></span>

<span data-ttu-id="34bfb-104">Para obtener el historial general de versiones de DirectML, [consulte Historial de versiones de DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="34bfb-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="34bfb-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="34bfb-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="34bfb-106">Se introdujo en la versión 1.5.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bfb-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="34bfb-107">Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="34bfb-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="34bfb-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="34bfb-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="34bfb-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="34bfb-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="34bfb-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="34bfb-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="34bfb-114">El número máximo de dimensiones admitidas para los operadores siguientes ha aumentado de 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="34bfb-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="34bfb-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="34bfb-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="34bfb-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="34bfb-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="34bfb-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="34bfb-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="34bfb-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="34bfb-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="34bfb-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="34bfb-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="34bfb-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="34bfb-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="34bfb-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="34bfb-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="34bfb-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="34bfb-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="34bfb-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="34bfb-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="34bfb-127">Se introdujo en la versión 1.4.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bfb-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="34bfb-128">Se ha agregado compatibilidad con los operadores [siguientes.](/windows/win32/api/directml/ne-directml-dml_operator_type)</span><span class="sxs-lookup"><span data-stu-id="34bfb-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="34bfb-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="34bfb-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="34bfb-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="34bfb-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="34bfb-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="34bfb-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="34bfb-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="34bfb-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="34bfb-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="34bfb-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="34bfb-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="34bfb-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="34bfb-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="34bfb-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="34bfb-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="34bfb-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="34bfb-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="34bfb-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="34bfb-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="34bfb-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="34bfb-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="34bfb-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="34bfb-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="34bfb-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="34bfb-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="34bfb-149">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="34bfb-149">Added the following enhancements.</span></span>

* <span data-ttu-id="34bfb-150">El número máximo de dimensiones de tensor ha aumentado de 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="34bfb-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="34bfb-151">Vea [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34bfb-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="34bfb-152">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34bfb-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="34bfb-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="34bfb-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="34bfb-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="34bfb-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="34bfb-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** y **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="34bfb-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="34bfb-156">**DML_OPERATOR_REDUCE**, al usar **DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="34bfb-157">Se han agregado los siguientes tipos de datos de 64 bits y son compatibles con operadores select.</span><span class="sxs-lookup"><span data-stu-id="34bfb-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="34bfb-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="34bfb-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="34bfb-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="34bfb-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="34bfb-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="34bfb-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="34bfb-161">Funcionalidad en desuso.</span><span class="sxs-lookup"><span data-stu-id="34bfb-161">Deprecated functionality.</span></span>

* <span data-ttu-id="34bfb-162">**DML_REDUCE_FUNCTION_ARGMAX** y **DML_REDUCE_FUNCTION_ARGMIN** han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="34bfb-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="34bfb-163">Debe preferir usar los operadores de **DML_OPERATOR_ARGMIN** y **DML_OPERATOR_ARGMAX** independientes en su lugar.</span><span class="sxs-lookup"><span data-stu-id="34bfb-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="34bfb-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="34bfb-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="34bfb-165">Se introdujo en la versión 1.2.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bfb-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="34bfb-166">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="34bfb-166">Added the following APIs.</span></span>

* [<span data-ttu-id="34bfb-167">Interfaz IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="34bfb-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="34bfb-168">Compatibilidad con gráficos de operadores [(vea IDMLDevice1::CompileGraph)](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="34bfb-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="34bfb-169">Se ha agregado compatibilidad con los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34bfb-169">Added support for the following operators.</span></span>

* <span data-ttu-id="34bfb-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="34bfb-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="34bfb-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="34bfb-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="34bfb-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="34bfb-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="34bfb-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="34bfb-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="34bfb-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="34bfb-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="34bfb-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="34bfb-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="34bfb-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="34bfb-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="34bfb-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="34bfb-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="34bfb-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="34bfb-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="34bfb-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="34bfb-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="34bfb-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="34bfb-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="34bfb-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="34bfb-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="34bfb-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="34bfb-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="34bfb-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="34bfb-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="34bfb-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="34bfb-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="34bfb-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="34bfb-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="34bfb-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="34bfb-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="34bfb-194">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="34bfb-194">Added the following enhancements.</span></span>

* <span data-ttu-id="34bfb-195">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34bfb-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="34bfb-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="34bfb-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="34bfb-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="34bfb-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="34bfb-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="34bfb-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="34bfb-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="34bfb-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="34bfb-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="34bfb-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="34bfb-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="34bfb-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="34bfb-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="34bfb-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="34bfb-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="34bfb-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="34bfb-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="34bfb-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="34bfb-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="34bfb-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="34bfb-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="34bfb-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="34bfb-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="34bfb-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="34bfb-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="34bfb-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="34bfb-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="34bfb-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="34bfb-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="34bfb-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="34bfb-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="34bfb-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="34bfb-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="34bfb-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="34bfb-221">**DML_OPERATOR_TOP_K** y **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="34bfb-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="34bfb-223">**DML_OPERATOR_REDUCE**, cuando se usa una de las siguientes funciones de reducción.</span><span class="sxs-lookup"><span data-stu-id="34bfb-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="34bfb-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="34bfb-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="34bfb-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="34bfb-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="34bfb-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="34bfb-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="34bfb-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="34bfb-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="34bfb-230">Restricciones de forma de tensor relajada **para DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="34bfb-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="34bfb-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="34bfb-232">Se introdujo en la versión 1.1.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bfb-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="34bfb-233">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="34bfb-233">Added the following APIs.</span></span>
* [<span data-ttu-id="34bfb-234">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="34bfb-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="34bfb-235">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="34bfb-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="34bfb-236">Consultas de nivel de característica [(consulte DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="34bfb-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="34bfb-237">Se ha agregado compatibilidad con los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34bfb-237">Added support for the following operators.</span></span>

* <span data-ttu-id="34bfb-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="34bfb-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="34bfb-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="34bfb-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="34bfb-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="34bfb-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="34bfb-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="34bfb-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="34bfb-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="34bfb-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="34bfb-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="34bfb-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="34bfb-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="34bfb-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="34bfb-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="34bfb-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="34bfb-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="34bfb-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="34bfb-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="34bfb-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="34bfb-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="34bfb-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="34bfb-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="34bfb-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="34bfb-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="34bfb-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="34bfb-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="34bfb-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="34bfb-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="34bfb-257">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="34bfb-257">Added the following enhancements.</span></span>

* <span data-ttu-id="34bfb-258">Al enlazar un recurso de entrada para el envío de un [IDMLOperatorInitializer,](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)ahora es legal proporcionar un recurso con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (además de **D3D12_HEAP_TYPE_DEFAULT**), siempre y cuando también se establezcan las propiedades del montón adecuadas.</span><span class="sxs-lookup"><span data-stu-id="34bfb-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="34bfb-259">Vea [Enlace en DirectML.](./dml-binding.md)</span><span class="sxs-lookup"><span data-stu-id="34bfb-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="34bfb-260">Los siguientes operadores booleanos lógicos ahora admiten tensores de salida **UINT8,** además de la compatibilidad existente con **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="34bfb-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="34bfb-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="34bfb-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="34bfb-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="34bfb-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="34bfb-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="34bfb-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="34bfb-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="34bfb-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="34bfb-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="34bfb-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="34bfb-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="34bfb-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="34bfb-268">Las funciones de activación 5D ahora admiten el uso de strides en sus tensores de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="34bfb-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="34bfb-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="34bfb-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="34bfb-270">Nivel de característica en el que se introdujo DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bfb-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="34bfb-271">Vea también</span><span class="sxs-lookup"><span data-stu-id="34bfb-271">See also</span></span>

* [<span data-ttu-id="34bfb-272">Historial de versiones de DirectML</span><span class="sxs-lookup"><span data-stu-id="34bfb-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="34bfb-273">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="34bfb-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="34bfb-274">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="34bfb-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="34bfb-275">DML_FEATURE_QUERY_FEATURE_LEVELS estructura</span><span class="sxs-lookup"><span data-stu-id="34bfb-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
