---
description: Sombreador que se invoca desde otro sombreador con la función intrínseca CallShader.
ms.assetid: ''
title: Sombreador al que se puede llamar
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461075"
---
# <a name="callable-shader"></a>Sombreador al que se puede llamar

Sombreador que se invoca desde otro sombreador con la [**función intrínseca CallShader.**](callshader-function.md)

Hay una estructura de parámetros proporcionada en el sitio de llamada de **CallShader** que debe coincidir con la estructura de parámetros utilizada en el sombreador al que se puede llamar al que apunta el índice solicitado en la tabla de sombreador a la que se puede llamar proporcionada a través del método [**DispatchRays.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)  El sombreador al que se puede llamar debe declarar este parámetro *como de entrada.*  Además, el sombreador al que se puede llamar puede leer entradas de índice de inicio y de dimensión. Para obtener más información, vea [**Intrínsecos de valor del sistema.**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md) 


## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


```
[shader("callable")]
```



## <a name="example"></a>Ejemplo

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




