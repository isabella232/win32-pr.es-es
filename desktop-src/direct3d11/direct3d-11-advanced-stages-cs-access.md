---
title: Acceso a recursos
description: Hay varias maneras de tener acceso a los recursos.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997116"
---
# <a name="accessing-resources"></a>Acceso a recursos

Hay varias maneras de tener acceso a [los recursos](overviews-direct3d-11-resources-types.md). Independientemente de, Direct3D garantiza que se devuelva cero para cualquier recurso al que se tenga acceso fuera de los límites.

-   [Acceso por desplazamiento de bytes](#access-by-byte-offset)
-   [Acceso por índice](#access-by-index)
-   [Acceso mediante el método MIPS](#access-by-mips-method)
-   [Temas relacionados](#related-topics)

## <a name="access-by-byte-offset"></a>Acceso por desplazamiento de bytes

Se puede tener acceso a dos nuevos tipos de búfer con un desplazamiento de bytes:

-   [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) es un búfer de solo lectura.
-   [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) es un búfer de lectura o escritura.

## <a name="access-by-index"></a>Acceso por índice

Los tipos de recursos pueden utilizar un índice para hacer referencia a una ubicación específica en el recurso. Considere este ejemplo:


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



En este ejemplo se asignan los 4 valores float que se almacenan en el textura situado en la posición del *PDV* en el recurso de textura 2D de *textura* a la variable *myVar* .

> [!Note]  
> El valor predeterminado para tener acceso a una textura de esta manera es el nivel cero de mipmap (el nivel más detallado).

 

> [!Note]  
> La línea "FLOAT4 myVar = nontexture \[ pos \] ;" es equivalente a "FLOAT4 myVar = cartexture. Load (UInt3 (pos, 0));". El acceso por índice es una nueva mejora de la sintaxis de HLSL.

 

> [!Note]  
> El compilador en la versión de junio de 2010 del SDK de DirectX y versiones posteriores permite indexar todos los tipos de recursos excepto los [búferes de direcciones de bytes](direct3d-11-advanced-stages-cs-resources.md).

 

> [!Note]  
> El compilador 2010 de junio y versiones posteriores permiten declarar variables de recursos locales. Puede asignar recursos definidos globalmente (como mi *textura*) a estas variables y usarlas de la misma manera que sus homólogos globales.

 

## <a name="access-by-mips-method"></a>Acceso mediante el método MIPS

Los objetos de textura tienen un método **MIPS** (por ejemplo, [**Texture2D. MIPS**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que puede usar para especificar el nivel de mipmap. En este ejemplo se lee el color almacenado en (7, 16) en el nivel 2 de mipmap en una textura 2D:


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



Se trata de una mejora del compilador 2010 de junio y posterior. La \[ \] \[ expresión "uint2 (x, y) \] " es equivalente a "texturiza. Load (UInt3 (x, y, 2))".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general del sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 