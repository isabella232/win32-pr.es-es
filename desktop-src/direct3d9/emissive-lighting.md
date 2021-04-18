---
description: La iluminación emisor se describe en un único término.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Iluminación emisor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714658"
---
# <a name="emissive-lighting-direct3d-9"></a>Iluminación emisor (Direct3D 9)

La iluminación emisor se describe en un único término.

Iluminación emisor = C ₑ

Donde:



| Parámetro | Valor predeterminado | Tipo          | Descripción     |
|-----------|---------------|---------------|-----------------|
| C ₑ        | (0, 0, 0, 0)     | D3DCOLORVALUE | Color de emisor. |



 

El valor de C ₑ es:

-   Vertex color1, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.
-   Vertex color2, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.
-   color de emisor de materiales

> [!Note]  
> Si se usa la opción EMISSIVEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color de emisor del material.

 

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colorea utilizando la luz ambiente de la escena y un color ambiente de material. A continuación se muestra el código.


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



Según la ecuación, el color resultante para los vértices del objeto es el color del material.

En la ilustración siguiente se muestra el color del material, que es verde. Emisor light ilumina todos los vértices de objeto con el mismo color. No depende de la dirección de la luz o del vértice normal. Como resultado, la esfera tiene el aspecto de un círculo 2D porque no hay ninguna diferencia en el sombreado en torno a la superficie del objeto.

![Ilustración de una esfera verde](images/lighte.jpg)

En la ilustración siguiente se muestra cómo la luz emisor se combina con los otros tres tipos de luces, en los ejemplos anteriores. En el lado derecho de la esfera, hay una mezcla de los emisor verdes y la luz ambiental roja. En el lado izquierdo de la esfera, la luz verde emisor se combina con ambiente rojo y luz difusa que produce un degradado rojo. El resaltado especular está en blanco en el centro y crea un anillo amarillo a medida que el valor de la luz especular cae claramente al salir de los valores de la luz ambiente, difusos y emisors que se mezclan para hacer amarillo.

![Ilustración de una esfera verde con emisor claro](images/lightadse.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



