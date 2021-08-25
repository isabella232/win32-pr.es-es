---
title: Acceso a recursos
description: Hay varias maneras de acceder a los recursos.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b66ae5ad0f3a49f51281d12ba5e3c2c52cd822aadd5097485b571533ae1a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677175"
---
# <a name="accessing-resources"></a>Acceso a recursos

Hay varias maneras de acceder a [los recursos.](overviews-direct3d-11-resources-types.md) Independientemente, Direct3D garantiza que se devuelva cero para cualquier recurso al que se acceda fuera de los límites.

-   [Acceso por desplazamiento de bytes](#access-by-byte-offset)
-   [Acceso por índice](#access-by-index)
-   [Método Access By Mips](#access-by-mips-method)
-   [Temas relacionados](#related-topics)

## <a name="access-by-byte-offset"></a>Acceso por desplazamiento de bytes

Se puede acceder a dos nuevos tipos de búfer mediante un desplazamiento de bytes:

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) es un búfer de solo lectura.
-   [**RWByteAddressBuffer es**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) un búfer de lectura o escritura.

## <a name="access-by-index"></a>Acceso por índice

Los tipos de recursos pueden usar un índice para hacer referencia a una ubicación específica del recurso. Considere este ejemplo:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



En este ejemplo se asignan los 4 valores float que se almacenan en el texel ubicado en la posición *pos* del recurso de textura *2D myTexture* a la variable *myVar.*

> [!Note]  
> El valor predeterminado para acceder a una textura de esta manera es mipmap level zero (el nivel más detallado).

 

> [!Note]  
> La línea "float4 myVar = myTexture pos ;" equivale a \[ \] "float4 myVar = myTexture.Load(uint3(pos,0));". El acceso por índice es una nueva mejora de la sintaxis HLSL.

 

> [!Note]  
> El compilador de la versión de junio de 2010 del SDK de DirectX y versiones posteriores permite indexar todos los tipos de recursos, excepto los búferes [de direcciones de bytes.](direct3d-11-advanced-stages-cs-resources.md)

 

> [!Note]  
> El compilador de junio de 2010 y versiones posteriores le permite declarar variables de recursos locales. Puede asignar recursos definidos globalmente (como *myTexture)* a estas variables y usarlos de la misma manera que sus homólogos globales.

 

## <a name="access-by-mips-method"></a>Método Access By Mips

Los objetos de textura tienen **un método mips** (por ejemplo, [**Texture2D.mips),**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))que puede usar para especificar el nivel de mapa mip. En este ejemplo se lee el color almacenado en (7,16) en el nivel de mapa mipmap 2 en una textura 2D:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Se trata de una mejora del compilador de junio de 2010 y versiones posteriores. La expresión "myTexture.mips \[ 2 \] \[ uint2(x,y) " equivale \] a "myTexture.Load(uint3(x,y,2))".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el sombreador de proceso](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 