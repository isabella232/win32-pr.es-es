---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Rellena un tensores de salida con bits distribuidos de forma determinista, pseudoaleatorios y con un formato uniforme. Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 19e01ec8dc47e65ace996deef5954c35e21bf5bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721202"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC estructura (directml. h)

Rellena un tensores de salida con bits distribuidos de forma determinista, pseudoaleatorios y con un formato uniforme. Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.

Este operador es determinista y se comporta como si fuera una función pura &mdash; , su ejecución no produce efectos secundarios y no utiliza ningún estado global. La salida pseudoaleatorios generada por este operador depende únicamente de los valores proporcionados en *InputStateTensor*.

Los generadores implementados por este operador no son seguros criptográficamente; por lo tanto, este operador no debe usarse para el cifrado, la generación de claves ni otras aplicaciones que requieren la generación de números aleatorios criptográficamente segura.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a>Miembros

`InputStateTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de entrada que contiene el estado interno del generador. El tamaño y el formato de este tensores de entrada depende de la [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, este tensores debe ser de tipo **UINT32** y tener tamaños `{1,1,1,6}` . Los primeros valores de 4 32 bits contienen un contador de 128 bits que aumenta de una vez. Los últimos valores de 2 32 bits contienen el valor de clave de 64 bits para el generador.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Al inicializar el estado de entrada del generador por primera vez, normalmente el contador de 128 bits (los primeros valores UINT32 de 4 32 bits) se debe inicializar en 0. La clave se puede elegir arbitrariamente; los distintos valores de clave generarán diferentes secuencias de números. Normalmente, el valor de la clave se genera mediante un valor de *inicialización* proporcionado por el usuario.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene los valores pseudoaleatorios resultantes. Este tensores puede tener cualquier tamaño.

`OutputStateTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores de salida opcional que contiene el estado de generador interno actualizado. Si se proporciona, este operador usa *InputStateTensor* para calcular un estado de generador actualizado adecuado y escribe el resultado en el *OutputStateTensor*. Normalmente, los autores de la llamada guardan este resultado y lo suministran como estado de entrada en una ejecución subsiguiente de este operador.

`Type`

Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Uno de los valores de la enumeración [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) , que indica el tipo de generador que se va a usar. Actualmente, el único valor válido es **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, que genera números pseudoaleatorios según el [algoritmo PHILOX 4X32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Observaciones
En cada ejecución de este operador, se debe incrementar el contador de 128 bits. Si se proporciona *OutputStateTensor* , este operador incrementa el contador con el valor correcto en su nombre y escribe el resultado en el *OutputStateTensor*. La cantidad que se debe incrementar depende del número de elementos de salida de 32 bits generados y del tipo del generador.

Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, el contador de 128 bits debe incrementarse `ceil(outputSize / 4)` en cada ejecución, donde `outputSize` es el número de elementos de *OutputTensor*.

Considere un ejemplo en el que el valor del contador de 128 bits es actualmente `0x48656c6c'6f46726f'6d536561'74746c65` y el tamaño de OutputTensor es `{3,3,20,7219}` . Después de ejecutar este operador una vez, el contador debería incrementarse en 324.855 (el número de elementos de salida generado dividido por 4, redondeado hacia arriba), lo que da como resultado un valor de contador de `0x48656c6c'6f46726f'6d536561'746f776e` . Este valor actualizado se debe proporcionar como entrada para la siguiente ejecución de este operador.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
`InputStateTensor` y `OutputStateTensor` deben tener el mismo *tamaño*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Entrada | {1, 1, 1, 6} | 4 | UINT32 |
| OutputTensor | Output | {D0, D1, D2, D3} | 4 | UINT32 |
| OutputStateTensor | Salida opcional | {1, 1, 1, 6} | 4 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |