---
title: Tipo de búfer
description: Use la siguiente sintaxis para declarar una variable de búfer.
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
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077952"
---
# <a name="buffer-type"></a>Tipo de búfer

Use la siguiente sintaxis para declarar una variable de búfer.



| Nombre de *tipo* de<de búfer >  ; |
|------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Búfer**
</dt> <dd>

Palabra clave required.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Automáticamente*
</dt> <dd>

Uno de los tipos de tipo HLSL [escalar](dx-graphics-hlsl-scalar.md), [Vector](dx-graphics-hlsl-vector.md)y some [Matrix](dx-graphics-hlsl-matrix.md) . Puede declarar una variable de búfer con una matriz siempre y cuando quepa en cantidades de 4 32 bits. Por lo tanto, puede escribir `Buffer<float2x2>` . Pero `Buffer<float4x4>` es demasiado grande y el compilador generará un error.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la variable.

</dd> </dl>

## <a name="example"></a>Ejemplo

Este es un ejemplo de una declaración de búfer del archivo PipesGS. FX en el [ejemplo PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Los datos se leen desde un búfer mediante una versión sobrecargada de la función de [**carga**](dx-graphics-hlsl-to-load.md) intrínseca de HLSL que toma un parámetro de entrada (un índice de entero). Se tiene acceso a un búfer como una matriz de elementos; por lo tanto, en este ejemplo se lee el segundo elemento.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Use la [fase Stream-Output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) para enviar datos a un búfer.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 