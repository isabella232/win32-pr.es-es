---
description: La iluminación emisiva se describe mediante un solo término.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Iluminación emisiva (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3200486118e6b44efc3be31f01b3a10e62c876d673c687619a4e6c8445f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802944"
---
# <a name="emissive-lighting-direct3d-9"></a>Iluminación emisiva (Direct3D 9)

La iluminación emisiva se describe mediante un solo término.

Iluminación emisiva = Cₑ

Donde:



| Parámetro | Valor predeterminado | Tipo          | Descripción     |
|-----------|---------------|---------------|-----------------|
| Cₑ        | (0,0,0,0)     | D3DCOLORVALUE | Color emisivo. |



 

El valor de Cₑ es:

-   vertex color1, si EMISSIVEMATERIALSOURCE = D3DMCS COLOR1 y el primer color de vértice se proporciona \_ en la declaración de vértice.
-   vertex color2, si EMISSIVEMATERIALSOURCE = D3DMCS COLOR2, y el segundo color de vértice se proporciona \_ en la declaración de vértice.
-   color emisivo material

> [!Note]  
> Si se usa cualquiera de las opciones EMISSIVEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color emisivo del material.

 

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colore con la luz ambiental de la escena y un color ambiental material. El código se muestra a continuación.


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

En la ilustración siguiente se muestra el color del material, que es verde. La luz emisiva enciende todos los vértices de objeto con el mismo color. No depende del vértice normal ni de la dirección de la luz. Como resultado, la esfera parece un círculo 2D porque no hay ninguna diferencia en el sombreado alrededor de la superficie del objeto.

![ilustración de una esfera verde](images/lighte.jpg)

En la ilustración siguiente se muestra cómo se combina la luz emisiva con los otros tres tipos de luces, de los ejemplos anteriores. En el lado derecho de la esfera, hay una combinación de la luz ambiental verde emisiva y roja. En el lado izquierdo de la esfera, la luz verde emisiva se combina con ambiente rojo y luz difusa que produce un degradado rojo. El resaltado especular es blanco en el centro y crea un anillo amarillo a medida que el valor de la luz especular se descuente claramente dejando los valores de luz ambiental, difuso y emisivo que se combinan para hacer amarillo.

![ilustración de una esfera verde con luz emisiva](images/lightadse.jpg)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



