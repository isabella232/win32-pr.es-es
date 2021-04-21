---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcula los pesos actualizados (parámetros) mediante los degradados proporcionados, basándose en el algoritmo Adam (estimación de M **oment** ptive de **ADA).** Este operador es un optimizador y normalmente se usa en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803524"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="6faea-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="6faea-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6faea-105">Calcula los pesos actualizados (parámetros) mediante los degradados proporcionados, basándose en el algoritmo Adam (estimación de M **oment** ptive de **ADA).**</span><span class="sxs-lookup"><span data-stu-id="6faea-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="6faea-106">Este operador es un optimizador y normalmente se usa en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.</span><span class="sxs-lookup"><span data-stu-id="6faea-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="6faea-107">Este operador realiza el cálculo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6faea-107">This operator performs the following computation:</span></span>

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

<span data-ttu-id="6faea-108">Además de calcular los parámetros de peso actualizados (devueltos en *OutputParametersTensor),* este operador también devuelve las estimaciones actualizadas del primer y segundo momento en *OutputFirstMomentTensor* y *OutputSecondMomentTensor,* respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6faea-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="6faea-109">Normalmente, debe almacenar estas estimaciones de primer y segundo momento y proporcionarlas como entradas durante el paso de entrenamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="6faea-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6faea-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="6faea-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="6faea-111">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="6faea-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6faea-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6faea-112">Syntax</span></span>
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="6faea-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="6faea-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="6faea-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-115">Tensor que contiene los parámetros (pesos) a los que se va a aplicar este optimizador.</span><span class="sxs-lookup"><span data-stu-id="6faea-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="6faea-116">Este operador usa las estimaciones de gradiente, primer y segundo momento, el paso de entrenamiento actual, así como los hiperparámetros *LearningRate,* *Beta1* y *Beta2,* para realizar el descenso de gradiente en los valores de peso proporcionados en este tensor.</span><span class="sxs-lookup"><span data-stu-id="6faea-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="6faea-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-118">Tensor que contiene la estimación del primer momento del degradado para cada valor de peso.</span><span class="sxs-lookup"><span data-stu-id="6faea-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="6faea-119">Normalmente, estos valores se obtienen como resultado de una ejecución anterior de este operador, a través de *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="6faea-120">Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensor normalmente se deben inicializar en cero.</span><span class="sxs-lookup"><span data-stu-id="6faea-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="6faea-121">Las ejecuciones posteriores deben usar los valores devueltos *en OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="6faea-122">Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="6faea-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-124">Tensor que contiene la estimación del segundo momento del degradado para cada valor de peso.</span><span class="sxs-lookup"><span data-stu-id="6faea-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="6faea-125">Normalmente, estos valores se obtienen como resultado de una ejecución anterior de este operador, a través de *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="6faea-126">Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensor normalmente se deben inicializar en cero.</span><span class="sxs-lookup"><span data-stu-id="6faea-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="6faea-127">Las ejecuciones posteriores deben usar los valores devueltos *en OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="6faea-128">Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="6faea-129">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-130">Degradados que se aplicarán a los parámetros de entrada (pesos) para el descenso de gradiente.</span><span class="sxs-lookup"><span data-stu-id="6faea-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="6faea-131">Los degradados normalmente se obtienen en un paso de apropagación posterior durante el entrenamiento.</span><span class="sxs-lookup"><span data-stu-id="6faea-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="6faea-132">Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="6faea-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="6faea-133">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-134">Tensor escalar que contiene un valor entero único que representa el recuento de pasos de entrenamiento actual.</span><span class="sxs-lookup"><span data-stu-id="6faea-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="6faea-135">Este valor junto con *Beta1* y *Beta2* se usa para calcular la decadencia exponencial de los tensores de estimación de primer y segundo momento.</span><span class="sxs-lookup"><span data-stu-id="6faea-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="6faea-136">Normalmente, el valor del paso de entrenamiento comienza en 0 al principio del entrenamiento y se incrementa en 1 en cada paso de entrenamiento sucesivo.</span><span class="sxs-lookup"><span data-stu-id="6faea-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="6faea-137">Este operador no actualiza el valor del paso de entrenamiento; debe hacerlo manualmente, por ejemplo, mediante [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6faea-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="6faea-138">Este tensor debe ser escalar (es decir, todos *los tamaños* iguales a 1) y tener el tipo de [**datos DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="6faea-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="6faea-139">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-140">Tensor de salida que contiene los valores actualizados del parámetro (peso) después de aplicar el descenso de gradiente.</span><span class="sxs-lookup"><span data-stu-id="6faea-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="6faea-141">Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor.</span><span class="sxs-lookup"><span data-stu-id="6faea-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="6faea-142">Consulte la [sección Comentarios para](#remarks) obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="6faea-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="6faea-143">Los *tamaños* y *el tipo de datos* de este tensor deben coincidir exactamente con los de *InputParametersTensor.*</span><span class="sxs-lookup"><span data-stu-id="6faea-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="6faea-144">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-145">Tensor de salida que contiene estimaciones actualizadas del primer momento.</span><span class="sxs-lookup"><span data-stu-id="6faea-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="6faea-146">Debe almacenar los valores de este tensor y proporcionarlos en *InputFirstMomentTensor* durante el paso de entrenamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="6faea-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="6faea-147">Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor.</span><span class="sxs-lookup"><span data-stu-id="6faea-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="6faea-148">Consulte la [sección Comentarios para](#remarks) obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="6faea-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="6faea-149">Los *tamaños* y *el tipo de datos* de este tensor deben coincidir exactamente con los de *InputParametersTensor.*</span><span class="sxs-lookup"><span data-stu-id="6faea-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="6faea-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6faea-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6faea-151">Tensor de salida que contiene estimaciones actualizadas del segundo momento.</span><span class="sxs-lookup"><span data-stu-id="6faea-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="6faea-152">Debe almacenar los valores de este tensor y proporcionarlos en *InputSecondMomentTensor* durante el paso de entrenamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="6faea-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="6faea-153">Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor.</span><span class="sxs-lookup"><span data-stu-id="6faea-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="6faea-154">Consulte la [sección Comentarios para](#remarks) obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="6faea-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="6faea-155">Los *tamaños* y *el tipo de datos* de este tensor deben coincidir exactamente con los de *InputParametersTensor.*</span><span class="sxs-lookup"><span data-stu-id="6faea-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="6faea-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6faea-156">Type: **float**</span></span>

<span data-ttu-id="6faea-157">La velocidad de aprendizaje, también conocida comúnmente como el tamaño *del paso*.</span><span class="sxs-lookup"><span data-stu-id="6faea-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="6faea-158">La velocidad de aprendizaje es un hiperparámetro que determina la magnitud de la actualización de peso a lo largo del vector de degradado en cada paso de entrenamiento.</span><span class="sxs-lookup"><span data-stu-id="6faea-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="6faea-159">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6faea-159">Type: **float**</span></span>

<span data-ttu-id="6faea-160">Hiperparámetro que representa la tasa de decadencia exponencial de la estimación del primer momento del degradado.</span><span class="sxs-lookup"><span data-stu-id="6faea-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="6faea-161">Este valor debe estar entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="6faea-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="6faea-162">Un valor de 0,9f es típico.</span><span class="sxs-lookup"><span data-stu-id="6faea-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="6faea-163">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6faea-163">Type: **float**</span></span>

<span data-ttu-id="6faea-164">Hiperparámetro que representa la tasa de decadencia exponencial de la estimación del segundo momento del degradado.</span><span class="sxs-lookup"><span data-stu-id="6faea-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="6faea-165">Este valor debe estar entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="6faea-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="6faea-166">Un valor de 0,999f es típico.</span><span class="sxs-lookup"><span data-stu-id="6faea-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="6faea-167">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6faea-167">Type: **float**</span></span>

<span data-ttu-id="6faea-168">Valor pequeño que se usa para ayudar a la estabilidad numérica evitando la división por cero.</span><span class="sxs-lookup"><span data-stu-id="6faea-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="6faea-169">Para las entradas de punto flotante de 32 bits, los valores típicos incluyen 1e-8 o `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="6faea-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6faea-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6faea-170">Remarks</span></span>
<span data-ttu-id="6faea-171">Este operador admite la ejecución en contexto, lo que significa que cada tensor de salida puede crear un alias para un tensor de entrada apto durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="6faea-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="6faea-172">Por ejemplo, es posible enlazar el mismo recurso para *InputParametersTensor* y *OutputParametersTensor* con el fin de lograr de forma eficaz una actualización local de los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="6faea-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="6faea-173">Todos los tensores de entrada de este operador, a excepción de *TrainingStepTensor,* pueden tener alias de esta manera.</span><span class="sxs-lookup"><span data-stu-id="6faea-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="6faea-174">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6faea-174">Availability</span></span>
<span data-ttu-id="6faea-175">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6faea-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6faea-176">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="6faea-176">Tensor constraints</span></span>
* <span data-ttu-id="6faea-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor y* *TrainingStepTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="6faea-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="6faea-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* y *OutputSecondMomentTensor* deben tener los mismos *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="6faea-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6faea-179">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="6faea-179">Tensor support</span></span>
| <span data-ttu-id="6faea-180">Tensor</span><span class="sxs-lookup"><span data-stu-id="6faea-180">Tensor</span></span> | <span data-ttu-id="6faea-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="6faea-181">Kind</span></span> | <span data-ttu-id="6faea-182">Dimensions</span><span class="sxs-lookup"><span data-stu-id="6faea-182">Dimensions</span></span> | <span data-ttu-id="6faea-183">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="6faea-183">Supported dimension counts</span></span> | <span data-ttu-id="6faea-184">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="6faea-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="6faea-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-185">InputParametersTensor</span></span> | <span data-ttu-id="6faea-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faea-186">Input</span></span> | <span data-ttu-id="6faea-187">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-188">4</span><span class="sxs-lookup"><span data-stu-id="6faea-188">4</span></span> | <span data-ttu-id="6faea-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="6faea-191">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faea-191">Input</span></span> | <span data-ttu-id="6faea-192">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-193">4</span><span class="sxs-lookup"><span data-stu-id="6faea-193">4</span></span> | <span data-ttu-id="6faea-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="6faea-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faea-196">Input</span></span> | <span data-ttu-id="6faea-197">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-198">4</span><span class="sxs-lookup"><span data-stu-id="6faea-198">4</span></span> | <span data-ttu-id="6faea-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-200">GradientTensor</span></span> | <span data-ttu-id="6faea-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faea-201">Input</span></span> | <span data-ttu-id="6faea-202">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-203">4</span><span class="sxs-lookup"><span data-stu-id="6faea-203">4</span></span> | <span data-ttu-id="6faea-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-205">TrainingStepTensor</span></span> | <span data-ttu-id="6faea-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="6faea-206">Input</span></span> | <span data-ttu-id="6faea-207">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="6faea-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="6faea-208">4</span><span class="sxs-lookup"><span data-stu-id="6faea-208">4</span></span> | <span data-ttu-id="6faea-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-210">OutputParametersTensor</span></span> | <span data-ttu-id="6faea-211">Resultados</span><span class="sxs-lookup"><span data-stu-id="6faea-211">Output</span></span> | <span data-ttu-id="6faea-212">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-213">4</span><span class="sxs-lookup"><span data-stu-id="6faea-213">4</span></span> | <span data-ttu-id="6faea-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="6faea-216">Resultados</span><span class="sxs-lookup"><span data-stu-id="6faea-216">Output</span></span> | <span data-ttu-id="6faea-217">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-218">4</span><span class="sxs-lookup"><span data-stu-id="6faea-218">4</span></span> | <span data-ttu-id="6faea-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6faea-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="6faea-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="6faea-221">Resultados</span><span class="sxs-lookup"><span data-stu-id="6faea-221">Output</span></span> | <span data-ttu-id="6faea-222">{ D0, D1, D2, D3 }</span><span class="sxs-lookup"><span data-stu-id="6faea-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="6faea-223">4</span><span class="sxs-lookup"><span data-stu-id="6faea-223">4</span></span> | <span data-ttu-id="6faea-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6faea-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6faea-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6faea-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6faea-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="6faea-226">**Header**</span></span> | <span data-ttu-id="6faea-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="6faea-227">directml.h</span></span> |