---
description: Después de ajustar la intensidad de la luz para cualquier efecto de atenuación, el motor de iluminación calcula la parte de la luz restante que se refleja de un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Luz difusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151954"
---
# <a name="diffuse-lighting-direct3d-9"></a>Luz difusa (Direct3D 9)

Después de ajustar la intensidad de la luz para cualquier efecto de atenuación, el motor de iluminación calcula la parte de la luz restante que se refleja de un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente. El motor de iluminación salta a este paso para las luces direccionales porque no se atenúan a lo largo de la distancia. El sistema considera dos tipos de reflexión, difuso y especular, y utiliza una fórmula diferente para determinar cuánta luz se refleja para cada una. Después de calcular los importes de la luz reflejada, Direct3D aplica estos nuevos valores a las propiedades de reflexión difusa y especular del material actual. Los valores de color resultantes son los componentes difusos y especulares que el rasterizador utiliza para generar el sombreado Gouraud y el resaltado especular.

La iluminación difusa se describe en la siguiente ecuación.

Luz difusa = suma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* ATTEN \*\]



| Parámetro       | Valor predeterminado | Tipo          | Descripción                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/D           | N/D           | Suma de cada componente difuso de la luz.                                                                  |
| C<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Color difuso.                                                                                                |
| L<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Color difuso de luz.                                                                                          |
| N               | N/D           | D3DVECTOR     | Vértice normal                                                                                                 |
| <sub>Directorio</sub> L | N/D           | D3DVECTOR     | Vector de dirección desde el vértice del objeto hasta la luz.                                                             |
| Atten           | N/D           | FLOAT         | Atenuación ligera. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Zona            | N/D           | FLOAT         | Factor destacado. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).  |



 

El valor de C<sub>d</sub> es:

-   Vertex color1, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.
-   Vertex color2, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.
-   color difuso de material

> [!Note]  
> Si se usa la opción DIFFUSEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color difuso de material.

 

Para calcular la atenuación (ATTEN) o las características destacadas (spot), vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

Los componentes difusos se fijan de 0 a 255, una vez que todas las luces se procesan y se interpolan por separado. El valor de iluminación difusa resultante es una combinación de los valores de las luces ambiente, difusa y emisor.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colorea utilizando el color difuso de luz y un color difuso de material. A continuación se muestra el código.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.

En las dos ilustraciones siguientes se muestra el color del material, que está atenuado y el color claro, que es rojo brillante.

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera roja](images/lightred.jpg)

La escena resultante se muestra en la siguiente ilustración. El único objeto de la escena es una esfera. El cálculo de iluminación difusa toma el color y la luz difusa y lo modifica por el ángulo entre la dirección de la luz y el vértice normal mediante el producto de punto. Como resultado, el parte posterior de la esfera se oscurece a medida que la superficie de la esfera se curva fuera de la luz.

![Ilustración de una esfera con iluminación difusa](images/lightd.jpg)

La combinación de la iluminación difusa con la iluminación ambiente del ejemplo anterior sombrea toda la superficie del objeto. La luz ambiente sombrea toda la superficie y la luz difusa ayuda a revelar la forma 3D del objeto, tal y como se muestra en la siguiente ilustración.

![Ilustración de una esfera con iluminación ambiente y luz difusa](images/lightad.jpg)

La iluminación difusa es más intensiva para calcular que la iluminación ambiente. Dado que depende de las normales de vértices y de la dirección luminosa, puede ver la geometría de los objetos en el espacio 3D, lo que produce una iluminación más realista que la iluminación ambiente. Puede usar los reflejos especulares para lograr un aspecto más realista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



