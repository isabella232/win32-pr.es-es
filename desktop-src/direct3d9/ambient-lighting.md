---
description: La iluminación ambiental proporciona iluminación constante para una escena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Iluminación ambiental (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a1d1d890d2de0a9cb617759ac3a9bb6d57f81b13440049bfb54575aee7a6546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069455"
---
# <a name="ambient-lighting-direct3d-9"></a>Iluminación ambiental (Direct3D 9)

La iluminación ambiental proporciona iluminación constante para una escena. Enciende todos los vértices de objeto de la misma manera porque no depende de ningún otro factor de iluminación, como los normales de vértice, la dirección de la luz, la posición de la luz, el intervalo o la atenuación. Es el tipo de iluminación más rápido, pero genera los resultados menos realistas. Direct3D contiene una sola propiedad de luz ambiente global que puede usar sin crear ninguna luz. Como alternativa, puede establecer cualquier objeto de luz para proporcionar iluminación ambiental. La iluminación ambiental de una escena se describe mediante la ecuación siguiente.

Ambient Lighting = Cₐ \* \[ Gₐ + sum(Atten<sub>i</sub> \* Spot<sub>i</sub> \* L<sub>ai</sub>)\]

Donde:



| Parámetro         | Valor predeterminado | Tipo          | Descripción                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| Cₐ                | (0,0,0,0)     | D3DCOLORVALUE | Color ambiente del material                                                                                                         |
| Gₐ                | (0,0,0,0)     | D3DCOLORVALUE | Color ambiente global                                                                                                           |
| Atten<sub>i</sub> | (0,0,0,0)     | D3DCOLORVALUE | Atenuación de la luz de ith. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Spot<sub>i</sub>  | (0,0,0,0)     | D3DVECTOR     | Factor destacado de la luz de ith. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)  |
| Sum               | N/D           | N/D           | Suma de la luz ambiente                                                                                                       |
| L<sub>ai</sub>    | (0,0,0,0)     | D3DVECTOR     | Color ambiente claro de la luz de ith                                                                                           |



 

El valor de Cₐ es:

-   vertex color1, si AMBIENTMATERIALSOURCE = D3DMCS COLOR1 y el primer color de vértice se proporciona \_ en la declaración de vértice.
-   vertex color2, si AMBIENTMATERIALSOURCE = D3DMCS COLOR2 y el segundo color de vértice \_ se proporciona en la declaración de vértice.
-   color ambiente del material.

> [!Note]  
> Si se usa cualquiera de las opciones AMBIENTMATERIALSOURCE y no se proporciona el color del vértice, se usa el color ambiente del material.

 

Para usar el color ambiente del material, use SetMaterial como se muestra en el código de ejemplo siguiente.

Gₐ es el color ambiente global. Se establece mediante SetRenderState(D3DRS \_ AMBIENT). Hay un color ambiental global en una escena de Direct3D. Este parámetro no está asociado a un objeto de luz de Direct3D.

L<sub>ai</sub> es el color ambiente de la luz de ith en la escena. Cada luz de Direct3D tiene un conjunto de propiedades, una de las cuales es el color ambiente. El término sum(L<sub>ai</sub>) es una suma de todos los colores ambientales de la escena.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colore con la luz ambiental de la escena y un color ambiental material.


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.

En las dos ilustraciones siguientes se muestra el color del material, que es gris, y el color claro, que es rojo claro.

![ilustración de una esfera gris](images/amb1.jpg)![ilustración de una esfera roja](images/lightred.jpg)

La escena resultante se muestra en la ilustración siguiente. El único objeto de la escena es una esfera. La luz ambiente enciende todos los vértices de objeto con el mismo color. No depende del vértice normal ni de la dirección de la luz. Como resultado, la esfera parece un círculo 2D porque no hay ninguna diferencia en el sombreado alrededor de la superficie del objeto.

![ilustración de una esfera con iluminación ambiental](images/lighta.jpg)

Para proporcionar a los objetos un aspecto más realista, aplique iluminación difusa o especular además de la iluminación ambiental.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



