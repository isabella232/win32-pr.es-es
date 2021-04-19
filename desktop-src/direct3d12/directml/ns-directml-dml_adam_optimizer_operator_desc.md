---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcula pesos actualizados (parámetros) mediante los degradados proporcionados, según el algoritmo de la estimación de Adam (**ADA** ptive **M** oment). Este operador es un optimizador y se utiliza normalmente en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.
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
ms.openlocfilehash: a4acd26f5174bf6c6ae53f5edfdc28cc6c9b1a3d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721213"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>DML_ADAM_OPTIMIZER_OPERATOR_DESC estructura (directml. h)

Calcula pesos actualizados (parámetros) mediante los degradados proporcionados, según el algoritmo de la estimación de Adam (**ADA** ptive **M** oment). Este operador es un optimizador y se utiliza normalmente en el paso de actualización de peso de un bucle de entrenamiento para realizar el descenso de gradiente.

Este operador realiza el siguiente cálculo:

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

Además de calcular los parámetros de peso actualizados (devueltos en *OutputParametersTensor*), este operador también devuelve las estimaciones de primer y segundo momento actualizadas en *OutputFirstMomentTensor* y *OutputSecondMomentTensor*, respectivamente. Normalmente, debe almacenar estas estimaciones en el primer y el segundo momento y proporcionarlas como entradas durante el paso de entrenamiento subsiguiente.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores que contiene los parámetros (pesos) a los que se va a aplicar este optimizador. Este operador usa las estimaciones de degradado, primer y segundo momento, el paso de entrenamiento actual, así como los hiperparámetros *LearningRate*, *beta1* y *beta2*, para realizar descensos de degradado en los valores de peso proporcionados en este tensores.

`InputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene la estimación del primer momento del degradado para cada valor de peso. Estos valores se obtienen normalmente como resultado de una ejecución anterior de este operador, a través de *OutputFirstMomentTensor*.

Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensores normalmente se deben inicializar en cero. Las ejecuciones posteriores deben usar los valores devueltos en *OutputFirstMomentTensor*.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`InputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene la estimación del segundo momento del degradado para cada valor de peso. Estos valores se obtienen normalmente como resultado de una ejecución anterior de este operador, a través de *OutputSecondMomentTensor*.

Al aplicar este optimizador a un conjunto de pesos por primera vez (por ejemplo, durante el paso de entrenamiento inicial), los valores de este tensores normalmente se deben inicializar en cero. Las ejecuciones posteriores deben usar los valores devueltos en *OutputSecondMomentTensor*.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`GradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Degradados que se van a aplicar a los parámetros de entrada (pesos) del descenso de gradiente. Normalmente, los degradados se obtienen en una fase de propagación de una inestación durante el entrenamiento.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`TrainingStepTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores escalar que contiene un valor entero único que representa el número de pasos de entrenamiento actual. Este valor, junto con *beta1* y *beta2* , se usa para calcular la caída exponencial del primer y el segundo.

Normalmente, el valor del paso de entrenamiento comienza en 0 al principio del entrenamiento y se incrementa en 1 en cada paso de entrenamiento sucesivo. Este operador no actualiza el valor del paso de entrenamiento; debe hacerlo manualmente, por ejemplo, mediante [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Este tensores debe ser un escalar (es decir, todos los *tamaños* son iguales a 1) y tener el tipo de datos [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene los valores del parámetro actualizado (peso) tras aplicar el descenso del degradado.

Durante el enlace, se permite a este tensores alias de un tensores de entrada válido, que se puede usar para realizar una actualización en contexto de este tensores. Vea la sección [comentarios](#remarks) para obtener más detalles.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`OutputFirstMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene estimaciones del primer momento actualizadas. Debe almacenar los valores de este tensores y proporcionarlos en *InputFirstMomentTensor* durante el siguiente paso de entrenamiento.

Durante el enlace, se permite a este tensores alias de un tensores de entrada válido, que se puede usar para realizar una actualización en contexto de este tensores. Vea la sección [comentarios](#remarks) para obtener más detalles.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`OutputSecondMomentTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene estimaciones del segundo momento actualizadas. Debe almacenar los valores de este tensores y proporcionarlos en *InputSecondMomentTensor* durante el siguiente paso de entrenamiento.

Durante el enlace, se permite a este tensores alias de un tensores de entrada válido, que se puede usar para realizar una actualización en contexto de este tensores. Vea la sección [comentarios](#remarks) para obtener más detalles.

Los *tamaños* y el tipo de los *tipos* de tensores deben coincidir exactamente con los de *InputParametersTensor*.

`LearningRate`

Tipo: **float**

La velocidad de aprendizaje, que también se conoce comúnmente como el *tamaño del paso*. La velocidad de aprendizaje es un hiperparámetro que determina la magnitud de la actualización del peso a lo largo del vector de degradado en cada paso del entrenamiento.

`Beta1`

Tipo: **float**

Hiperparámetro que representa la tasa exponencial de caída de la estimación del primer momento del degradado. Este valor debe estar comprendido entre 0,0 y 1,0. Un valor de 0.9 f es típico.

`Beta2`

Tipo: **float**

Hiperparámetro que representa la tasa exponencial de caída de la estimación del segundo momento del degradado. Este valor debe estar comprendido entre 0,0 y 1,0. Un valor de 0,999 f es típico.

`Epsilon`

Tipo: **float**

Valor pequeño que se usa para ayudar a la estabilidad numérica evitando la división por cero. En el caso de las entradas de punto flotante de 32 bits, los valores típicos incluyen 1E-8 o `FLT_EPSILON` .

## <a name="remarks"></a>Observaciones
Este operador admite la ejecución en contexto, lo que significa que cada tensores de salida tiene permiso para dar alias a un tensores de entrada válido durante el enlace. Por ejemplo, es posible enlazar el mismo recurso para *InputParametersTensor* y *OutputParametersTensor* con el fin de lograr de forma eficaz una actualización en contexto de los parámetros de entrada. Todos los datos de la entrada de este operador, con la excepción de *TrainingStepTensor*, son válidos para incluirse en el alias de esta manera.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* y *TrainingStepTensor* deben tener el mismo *tipo de texto*.
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* y *OutputSecondMomentTensor* deben tener el mismo *tamaño*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Entrada | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Entrada | {1, 1, 1, 1} | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Output | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |