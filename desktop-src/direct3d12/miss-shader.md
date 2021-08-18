---
description: Sombreador que se invoca cuando no se encuentra ni se acepta ninguna intersección de rayos.
ms.assetid: ''
title: Sombreador de errores
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 30f7ce32e66a19984ce43737d9fc9cae83652c851174d7db350ca34628a33033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850828"
---
# <a name="miss-shader"></a>Sombreador de errores

Sombreador que se invoca cuando no se encuentra ni se acepta ninguna intersección de rayos. Esto es útil para el sombreado de fondo o de cielo.  El sombreador de errores puede usar [**CallShader**](callshader-function.md) **y TraceRay** para programar más trabajo.

El sombreador de errores debe incluir un parámetro de carga con tipo de estructura definida por el usuario que coincida con el proporcionado a [**TraceRay**](traceray-function.md).


## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


```
[shader("miss")]
```



## <a name="example"></a>Ejemplo

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




