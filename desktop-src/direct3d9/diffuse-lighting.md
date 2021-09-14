---
description: Después de ajustar la intensidad de la luz para los efectos de atenuación, el motor de iluminación calcula la cantidad de luz restante reflejada desde un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Iluminación difusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888612"
---
# <a name="diffuse-lighting-direct3d-9"></a>Iluminación difusa (Direct3D 9)

Después de ajustar la intensidad de la luz para los efectos de atenuación, el motor de iluminación calcula la cantidad de luz restante reflejada desde un vértice, dado el ángulo del vértice normal y la dirección de la luz del incidente. El motor de iluminación omite este paso para las luces direccionales porque no se atenuan a lo largo de la distancia. El sistema considera dos tipos de reflexión, difuso y especular, y usa una fórmula diferente para determinar cuánta luz se refleja para cada uno. Después de calcular la cantidad de luz reflejada, Direct3D aplica estos nuevos valores a las propiedades de reflectancia difusa y especular del material actual. Los valores de color resultantes son los componentes difusos y especulares que usa el rasterizador para generar sombreado de Gouraud y resaltado especular.

La iluminación difusa se describe en la siguiente ecuación.

Iluminación difusa = suma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* Atten \* Spot\]



| Parámetro       | Valor predeterminado | Tipo          | Descripción                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/D           | N/D           | Suma del componente difuso de cada luz.                                                                  |
| C<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Color difuso.                                                                                                |
| L<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Color difuso claro.                                                                                          |
| N               | N/D           | D3DVECTOR     | Vértice normal                                                                                                 |
| L<sub>dir</sub> | N/D           | D3DVECTOR     | Vector de dirección del vértice del objeto a la luz.                                                             |
| Atten           | N/D           | FLOAT         | Atenuación de luz. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Zona            | N/D           | FLOAT         | Factor spotlight. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)  |



 

El valor de C<sub>d</sub> es:

-   vertex color1, si DIFFUSEMATERIALSOURCE = D3DMCS COLOR1 y el primer color de vértice se proporciona \_ en la declaración de vértice.
-   vertex color2, si DIFFUSEMATERIALSOURCE = D3DMCS COLOR2 y el segundo color de vértice se proporciona \_ en la declaración de vértice.
-   color difuso de material

> [!Note]  
> Si se usa cualquiera de las opciones DIFFUSEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color difuso del material.

 

Para calcular la atenuación (Atten) o las características de spotlight (Spot), consulte Atenuación y [factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)

Los componentes difusos se fijan para que sean de 0 a 255, después de que todas las luces se procesen e interpolan por separado. El valor de iluminación difusa resultante es una combinación de los valores de luz ambiente, difuso y emisivo.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colore con el color difuso claro y un color difuso de material. El código se muestra a continuación.


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

En las dos ilustraciones siguientes se muestra el color del material, que es gris, y el color claro, que es rojo brillante.

![ilustración de una esfera gris](images/amb1.jpg)![ilustración de una esfera roja](images/lightred.jpg)

La escena resultante se muestra en la ilustración siguiente. El único objeto de la escena es una esfera. El cálculo de iluminación difusa toma el material y el color difuso claro y lo modifica por el ángulo entre la dirección de la luz y el vértice normal mediante el producto de punto. Como resultado, la parte posterior de la esfera se vuelve más oscura cuando la superficie de la esfera se curva lejos de la luz.

![ilustración de una esfera con iluminación difusa](images/lightd.jpg)

La combinación de la iluminación difusa con la iluminación ambiente del ejemplo anterior sombrea toda la superficie del objeto. La luz ambiente sombrea toda la superficie y la luz difusa ayuda a revelar la forma 3D del objeto, como se muestra en la ilustración siguiente.

![ilustración de una esfera con iluminación difusa e iluminación ambiental](images/lightad.jpg)

La iluminación difusa es más intensiva para calcular que la iluminación ambiente. Dado que depende de las normales de vértice y la dirección de la luz, puede ver la geometría de los objetos en el espacio 3D, lo que genera una iluminación más realista que la iluminación ambiente. Puede usar resaltados especulares para lograr un aspecto más realista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



