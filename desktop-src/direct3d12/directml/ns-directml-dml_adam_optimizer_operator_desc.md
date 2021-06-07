---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcula los pesos actualizados (parámetros) mediante los degradados proporcionados, en función del algoritmo Adam (estimación de M **oment** ptive de **ADA).** Este operador es un optimizador y normalmente se usa en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418035"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC estructura (directml.h)

Calcula los pesos actualizados (parámetros) mediante los degradados proporcionados, en función del algoritmo Adam (estimación de M **oment** ptive de **ADA).** Este operador es un optimizador y normalmente se usa en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.

Este operador realiza el cálculo siguiente:

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

Además de calcular los parámetros de peso actualizados (devueltos en *OutputParametersTensor),* este operador también devuelve las estimaciones actualizadas del primer y segundo momento en *OutputFirstMomentTensor* y *OutputSecondMomentTensor,* respectivamente. Normalmente, debe almacenar estas estimaciones de primer y segundo momento y proporcionarlas como entradas durante el paso de entrenamiento posterior.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
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

## <a name="members"></a>Miembros

`InputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los parámetros (pesos) a los que se va a aplicar este optimizador. Este operador usa las estimaciones de gradiente, primero y segundo momento, el paso de entrenamiento actual, así como los hiperparámetros *LearningRate,* *Beta1* y *Beta2,* para realizar el descenso de gradiente en los valores de peso proporcionados en este tensor.

`InputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene la estimación del primer momento del degradado para cada valor de peso. Normalmente, estos valores se obtienen como resultado de una ejecución anterior de este operador, a través de *OutputFirstMomentTensor*.

Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensor normalmente se deben inicializar en cero. Las ejecuciones posteriores deben usar los valores devueltos *en OutputFirstMomentTensor*.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`InputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene la estimación del segundo momento del degradado para cada valor de peso. Normalmente, estos valores se obtienen como resultado de una ejecución anterior de este operador, a través de *OutputSecondMomentTensor*.

Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensor normalmente se deben inicializar en cero. Las ejecuciones posteriores deben usar los valores devueltos *en OutputSecondMomentTensor*.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`GradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Degradados que se aplicarán a los parámetros de entrada (pesos) para el descenso de gradiente. Los degradados normalmente se obtienen en un paso de apropagación posterior durante el entrenamiento.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`TrainingStepTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor escalar que contiene un valor entero único que representa el recuento de pasos de entrenamiento actual. Este valor junto con *Beta1* y *Beta2* se usa para calcular la decadencia exponencial de los tensores de estimación de primer y segundo momento.

Normalmente, el valor del paso de entrenamiento comienza en 0 al principio del entrenamiento y se incrementa en 1 en cada paso de entrenamiento sucesivo. Este operador no actualiza el valor del paso de entrenamiento; debe hacerlo manualmente, por ejemplo, mediante [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Este tensor debe ser escalar (es decir, todos *los tamaños* iguales a 1) y tener el tipo de [**datos DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los valores de parámetro actualizados (peso) después de aplicar el descenso de gradiente.

Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor. Consulte la [sección Comentarios](#remarks) para obtener más detalles.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`OutputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensor de salida que contiene las estimaciones actualizadas del primer momento. Debe almacenar los valores de este tensor y suministrarlos en *InputFirstMomentTensor* durante el paso de entrenamiento posterior.

Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor. Consulte la [sección Comentarios](#remarks) para obtener más detalles.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`OutputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensor de salida que contiene las estimaciones actualizadas del segundo momento. Debe almacenar los valores de este tensor y suministrarlos en *InputSecondMomentTensor* durante el paso de entrenamiento posterior.

Durante el enlace, este tensor puede crear un alias para un tensor de entrada apto, que se puede usar para realizar una actualización local de este tensor. Consulte la [sección Comentarios](#remarks) para obtener más detalles.

Los *tamaños* y *datatype* de este tensor deben coincidir exactamente con los de *InputParametersTensor*.

`LearningRate`

Tipo: **float**

La velocidad de aprendizaje, también conocida comúnmente como el tamaño *del paso*. La velocidad de aprendizaje es un hiperparámetro que determina la magnitud de la actualización de peso a lo largo del vector de degradado en cada paso de entrenamiento.

`Beta1`

Tipo: **float**

Hiperparámetro que representa la tasa de decadencia exponencial de la estimación del primer momento del degradado. Este valor debe estar entre 0,0 y 1,0. Un valor de 0,9f es típico.

`Beta2`

Tipo: **float**

Hiperparámetro que representa la tasa de decadencia exponencial de la estimación del segundo momento del degradado. Este valor debe estar entre 0,0 y 1,0. Un valor de 0,999f es típico.

`Epsilon`

Tipo: **float**

Valor pequeño que se usa para ayudar a la estabilidad numérica evitando la división por cero. Para las entradas de punto flotante de 32 bits, los valores típicos incluyen 1e-8 o `FLT_EPSILON` .

## <a name="remarks"></a>Comentarios
Este operador admite la ejecución en contexto, lo que significa que cada tensor de salida puede crear un alias para un tensor de entrada válido durante el enlace. Por ejemplo, es posible enlazar el mismo recurso para *InputParametersTensor* y *OutputParametersTensor* con el fin de lograr de forma eficaz una actualización local de los parámetros de entrada. Todos los tensores de entrada de este operador, a excepción de *TrainingStepTensor,* pueden tener alias de esta manera.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor y* *TrainingStepTensor* deben tener el mismo *DataType.*
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* y *OutputSecondMomentTensor* deben tener los mismos *tamaños.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Dimensions | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Entrada | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Entrada | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Entrada | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Entrada | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Entrada | { 1, 1, 1, 1 } | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Resultados | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Resultados | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Resultados | { D0, D1, D2, D3 } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |