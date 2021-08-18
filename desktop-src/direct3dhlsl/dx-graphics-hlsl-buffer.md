---
title: Tipo de búfer
description: Use la sintaxis siguiente para declarar una variable de búfer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo de búfer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78d0b452a387ed1d4bf750062963996d0248fa249954a99be581118560866123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120349"
---
# <a name="buffer-type"></a>Tipo de búfer

Use la sintaxis siguiente para declarar una variable de búfer.



| Buffer<*nombre de* >  *tipo*; |
|------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Búfer**
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Uno de los [tipos escalares,](dx-graphics-hlsl-scalar.md) [vector](dx-graphics-hlsl-vector.md)y [HLSL](dx-graphics-hlsl-matrix.md) de matriz. Puede declarar una variable de búfer con una matriz siempre que quepa en 4 cantidades de 32 bits. Por lo tanto, puede escribir `Buffer<float2x2>` . Pero `Buffer<float4x4>` es demasiado grande y el compilador generará un error.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la variable.

</dd> </dl>

## <a name="example"></a>Ejemplo

Este es un ejemplo de una declaración de búfer del archivo PipesGS.fx del [ejemplo PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Los datos se leen desde un búfer mediante una versión sobrecargada de la función intrínseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL que toma un parámetro de entrada (un índice entero). Se tiene acceso a un búfer como una matriz de elementos; por lo tanto, en este ejemplo se lee el segundo elemento .


```
float4 bufferData = g_Buffer.Load( 1 );
```



Use la [fase stream-output para](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) generar datos en un búfer.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de datos (HLSL de DirectX)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 