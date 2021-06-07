---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: Rellena un tensor de salida con bits generados de forma determinista, pseudo aleatorios y distribuidos uniformemente. Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.
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
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417945"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a>DML_RANDOM_GENERATOR_OPERATOR_DESC estructura (directml.h)

Rellena un tensor de salida con bits generados de forma determinista, pseudo aleatorios y distribuidos uniformemente. Opcionalmente, este operador también puede generar un estado de generador interno actualizado, que se puede usar durante las ejecuciones posteriores del operador.

Este operador es determinista y se comporta como si fuera una función pura, es decir, su ejecución no produce efectos secundarios y &mdash; no usa ningún estado global. La salida pseudolealea producida por este operador depende únicamente de los valores proporcionados en *InputStateTensor*.

Los generadores implementados por este operador no son criptográficamente seguros; Por lo tanto, este operador no debe usarse para el cifrado, la generación de claves u otras aplicaciones que requieran la generación de números aleatorios criptográficamente segura.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Tensor de entrada que contiene el estado del generador interno. El tamaño y el formato de este tensor de entrada dependen del [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).

Para **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, este tensor debe ser de tipo **UINT32** y tener tamaños `{1,1,1,6}` . Los cuatro primeros valores de 32 bits contienen un contador de 128 bits que aumenta de forma monótona. Los dos últimos valores de 32 bits contienen el valor de clave de 64 bits para el generador.

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

Al inicializar el estado de entrada del generador por primera vez, normalmente el contador de 128 bits (los cuatro primeros valores UINT32 de 32 bits) debe inicializarse en 0. La clave se puede elegir arbitrariamente; los distintos valores de clave producirán secuencias de números diferentes. El valor de la clave normalmente se genera mediante un *valor de ed. proporcionado por el usuario.*

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los valores pseudo aleatorios resultantes. Este tensor puede ser de cualquier tamaño.

`OutputStateTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida opcional que contiene el estado del generador interno actualizado. Si se proporciona, este operador usa *InputStateTensor* para calcular un estado de generador actualizado adecuado y escribe el resultado en *OutputStateTensor*. Normalmente, los autores de la llamada guardarían este resultado y lo proporcionarían como estado de entrada en una ejecución posterior de este operador.

`Type`

Tipo: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**

Uno de los valores de la [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enumeración, que indica el tipo de generador que se usará. Actualmente, el único valor válido **es DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, que genera números pseudo aleatorios según el algoritmo [de Philox 4x32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).

## <a name="remarks"></a>Comentarios
En cada ejecución de este operador, se debe incrementar el contador de 128 bits. Si se *proporciona OutputStateTensor,* THEN este operador incrementa el contador con el valor correcto en su nombre y escribe el resultado en *OutputStateTensor*. La cantidad en la que se debe incrementar depende del número de elementos de salida de 32 bits generados y del tipo del generador.

Por **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, el contador de 128 bits se debe incrementar en en cada ejecución, donde es el número de elementos `ceil(outputSize / 4)` de `outputSize` *OutputTensor*.

Considere un ejemplo en el que el valor del contador de 128 bits es actualmente y el tamaño de `0x48656c6c'6f46726f'6d536561'74746c65` OutputTensor es `{3,3,20,7219}` . Después de ejecutar este operador una vez, el contador debe incrementarse en 324 855 (el número de elementos de salida generados divididos por 4, redondeados hacia arriba) lo que da como resultado un valor de contador de `0x48656c6c'6f46726f'6d536561'746f776e` . A continuación, este valor actualizado debe proporcionarse como entrada para la siguiente ejecución de este operador.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
`InputStateTensor`y `OutputStateTensor` deben tener los mismos *tamaños.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Dimensions | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputStateTensor | Entrada | { 1, 1, 1, 6 } | 4 | UINT32 |
| OutputTensor | Resultados | { D0, D1, D2, D3 } | 4 | UINT32 |
| OutputStateTensor | Salida opcional | { 1, 1, 1, 6 } | 4 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |