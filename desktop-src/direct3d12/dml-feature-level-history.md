---
title: Historial de nivel de característica de DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282554"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="78262-103">Historial de nivel de característica de DirectML</span><span class="sxs-lookup"><span data-stu-id="78262-103">DirectML feature level history</span></span>

<span data-ttu-id="78262-104">Para obtener información general sobre el historial de versiones de DirectML, [consulte Historial de versiones de DirectML.](./dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="78262-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="78262-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="78262-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="78262-106">Se introdujo en la versión 1.6.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="78262-107">Se ha agregado compatibilidad con los siguientes tipos de operador, documentados [**en DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-108">Para cada constante de tipo de operador, ese tema proporciona un vínculo a la estructura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78262-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="78262-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="78262-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="78262-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="78262-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="78262-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="78262-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="78262-112">Compatibilidad con el tipo de datos extendido y el recuento de dimensiones para los operadores siguientes, [**documentados DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-113">Para obtener más información sobre la compatibilidad específica agregada [**en DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), vea el tema sobre la estructura de cada operador.</span><span class="sxs-lookup"><span data-stu-id="78262-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="78262-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="78262-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="78262-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="78262-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="78262-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="78262-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="78262-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="78262-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="78262-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="78262-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="78262-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="78262-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="78262-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="78262-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="78262-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="78262-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="78262-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="78262-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="78262-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="78262-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="78262-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="78262-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="78262-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="78262-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="78262-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="78262-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="78262-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="78262-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="78262-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="78262-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="78262-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="78262-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="78262-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="78262-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="78262-132">Se introdujo en la versión 1.5.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="78262-133">Se ha agregado compatibilidad con los siguientes tipos de operador, documentados [**en DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-134">Para cada constante de tipo de operador, ese tema proporciona un vínculo a la estructura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78262-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="78262-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="78262-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="78262-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="78262-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="78262-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="78262-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="78262-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="78262-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="78262-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="78262-141">El número máximo de dimensiones admitidas para los operadores siguientes ha aumentado de 4 a 8.</span><span class="sxs-lookup"><span data-stu-id="78262-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="78262-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="78262-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="78262-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="78262-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="78262-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="78262-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="78262-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="78262-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="78262-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="78262-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="78262-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="78262-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="78262-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="78262-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="78262-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="78262-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="78262-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="78262-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="78262-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="78262-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="78262-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="78262-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="78262-154">Se introdujo en la versión 1.4.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="78262-155">Se ha agregado compatibilidad con los siguientes tipos de operador, documentados [**en DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-156">Para cada constante de tipo de operador, ese tema proporciona un vínculo a la estructura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78262-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="78262-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="78262-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="78262-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="78262-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="78262-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="78262-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="78262-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="78262-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="78262-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="78262-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="78262-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="78262-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="78262-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="78262-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="78262-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="78262-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="78262-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="78262-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="78262-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="78262-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="78262-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="78262-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="78262-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="78262-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="78262-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="78262-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="78262-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="78262-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="78262-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="78262-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="78262-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="78262-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="78262-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="78262-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="78262-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="78262-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="78262-177">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="78262-177">Added the following enhancements.</span></span>

* <span data-ttu-id="78262-178">El número máximo de dimensiones de tensor ha aumentado de 5 a 8.</span><span class="sxs-lookup"><span data-stu-id="78262-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="78262-179">Vea [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="78262-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="78262-180">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78262-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="78262-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="78262-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="78262-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="78262-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="78262-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** y **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="78262-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="78262-184">**DML_OPERATOR_REDUCE**, cuando se **usa DML_REDUCE_FUNCTION_ARGMIN** o **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="78262-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="78262-185">Se han agregado los siguientes tipos de datos de 64 bits y son compatibles con operadores select.</span><span class="sxs-lookup"><span data-stu-id="78262-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="78262-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="78262-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="78262-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="78262-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="78262-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="78262-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="78262-189">Funcionalidad en desuso.</span><span class="sxs-lookup"><span data-stu-id="78262-189">Deprecated functionality.</span></span>

* <span data-ttu-id="78262-190">**DML_REDUCE_FUNCTION_ARGMAX** y **DML_REDUCE_FUNCTION_ARGMIN** han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="78262-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="78262-191">Debe preferir usar los operadores **DML_OPERATOR_ARGMIN** y **DML_OPERATOR_ARGMAX** independientes en su lugar.</span><span class="sxs-lookup"><span data-stu-id="78262-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="78262-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="78262-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="78262-193">Se introdujo en la versión 1.2.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="78262-194">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="78262-194">Added the following APIs.</span></span>

* [<span data-ttu-id="78262-195">Interfaz IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="78262-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="78262-196">Compatibilidad con gráficos de operadores [(consulte IDMLDevice1::CompileGraph)](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="78262-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="78262-197">Se ha agregado compatibilidad con los siguientes tipos de operador, documentados [**en DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-198">Para cada constante de tipo de operador, ese tema proporciona un vínculo a la estructura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78262-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="78262-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="78262-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="78262-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="78262-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="78262-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="78262-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="78262-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="78262-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="78262-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="78262-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="78262-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="78262-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="78262-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="78262-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="78262-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="78262-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="78262-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="78262-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="78262-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="78262-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="78262-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="78262-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="78262-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="78262-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="78262-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="78262-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="78262-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="78262-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="78262-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="78262-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="78262-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="78262-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="78262-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="78262-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="78262-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="78262-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="78262-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="78262-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="78262-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="78262-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="78262-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="78262-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="78262-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="78262-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="78262-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="78262-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="78262-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="78262-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="78262-223">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="78262-223">Added the following enhancements.</span></span>

* <span data-ttu-id="78262-224">Se ha agregado compatibilidad adicional con tipos de datos enteros a los operadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78262-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="78262-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="78262-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="78262-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="78262-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="78262-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="78262-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="78262-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="78262-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="78262-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="78262-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="78262-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="78262-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="78262-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="78262-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="78262-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="78262-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="78262-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="78262-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="78262-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="78262-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="78262-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="78262-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="78262-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="78262-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="78262-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="78262-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="78262-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="78262-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="78262-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="78262-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="78262-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="78262-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="78262-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="78262-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="78262-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="78262-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="78262-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="78262-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="78262-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="78262-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="78262-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="78262-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="78262-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="78262-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="78262-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="78262-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="78262-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="78262-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="78262-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="78262-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="78262-250">**DML_OPERATOR_TOP_K** y **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="78262-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="78262-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="78262-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="78262-252">**DML_OPERATOR_REDUCE**, cuando se usa una de las siguientes funciones de reducción.</span><span class="sxs-lookup"><span data-stu-id="78262-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="78262-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="78262-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="78262-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="78262-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="78262-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="78262-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="78262-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="78262-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="78262-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="78262-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="78262-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="78262-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="78262-259">Restricciones de formas de tensor relajadas **para DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="78262-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="78262-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="78262-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="78262-261">Se introdujo en la versión 1.1.0 de DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="78262-262">Se han agregado las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="78262-262">Added the following APIs.</span></span>
* [<span data-ttu-id="78262-263">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="78262-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="78262-264">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="78262-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="78262-265">Consultas de nivel de característica (consulte [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="78262-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="78262-266">Se ha agregado compatibilidad con los siguientes tipos de operadores, documentados [**en DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="78262-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="78262-267">Para cada constante de tipo de operador, ese tema proporciona un vínculo a la estructura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78262-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="78262-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="78262-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="78262-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="78262-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="78262-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="78262-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="78262-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="78262-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="78262-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="78262-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="78262-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="78262-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="78262-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="78262-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="78262-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="78262-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="78262-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="78262-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="78262-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="78262-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="78262-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="78262-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="78262-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="78262-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="78262-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="78262-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="78262-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="78262-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="78262-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="78262-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="78262-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="78262-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="78262-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="78262-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="78262-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="78262-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="78262-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="78262-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="78262-287">Se han agregado las siguientes mejoras.</span><span class="sxs-lookup"><span data-stu-id="78262-287">Added the following enhancements.</span></span>

* <span data-ttu-id="78262-288">Al enlazar un recurso de entrada para el envío de un [IDMLOperatorInitializer,](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)ahora es legal proporcionar un recurso con [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (además de **D3D12_HEAP_TYPE_DEFAULT**), siempre que también se establezcan las propiedades de montón adecuadas.</span><span class="sxs-lookup"><span data-stu-id="78262-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="78262-289">Vea [Enlace en DirectML.](./dml-binding.md)</span><span class="sxs-lookup"><span data-stu-id="78262-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="78262-290">Los siguientes operadores booleanos lógicos ahora admiten tensores de salida **UINT8,** además de la compatibilidad existente con **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="78262-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="78262-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="78262-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="78262-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="78262-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="78262-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="78262-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="78262-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="78262-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="78262-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="78262-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="78262-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="78262-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="78262-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="78262-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="78262-298">Las funciones de activación 5D ahora admiten el uso de strides en sus tensores de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="78262-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="78262-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="78262-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="78262-300">Nivel de característica en el que se introdujo DirectML.</span><span class="sxs-lookup"><span data-stu-id="78262-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="78262-301">Vea también</span><span class="sxs-lookup"><span data-stu-id="78262-301">See also</span></span>

* [<span data-ttu-id="78262-302">Historial de versiones de DirectML</span><span class="sxs-lookup"><span data-stu-id="78262-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="78262-303">DML_FEATURE_LEVEL enumeración</span><span class="sxs-lookup"><span data-stu-id="78262-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="78262-304">Función DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="78262-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="78262-305">DML_FEATURE_QUERY_FEATURE_LEVELS estructura</span><span class="sxs-lookup"><span data-stu-id="78262-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
