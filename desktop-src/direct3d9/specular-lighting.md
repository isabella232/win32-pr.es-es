---
description: La reflexión especular de modelado requiere que el sistema no solo sepa en qué dirección viaja la luz, sino también la dirección hacia el ojo del espectador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminación especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84597b63ebd064fbe27ae90b673e9c91166be96f6f45b039ba29a16de9011054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520176"
---
# <a name="specular-lighting-direct3d-9"></a>Iluminación especular (Direct3D 9)

La reflexión especular de modelado requiere que el sistema no solo sepa en qué dirección viaja la luz, sino también la dirección hacia el ojo del espectador. El sistema usa una versión simplificada del modelo de reflexión especular de Phong, que emplea un vector a medio camino para aproximar la intensidad de la reflexión especular.

El estado de iluminación predeterminado no calcula los resaltados especulares. Para habilitar la iluminación especular, asegúrese de establecer D3DRS \_ SPECULARENABLE en **TRUE.**

## <a name="specular-lighting-equation"></a>Ecuación de iluminación especular

La iluminación especular se describe mediante la ecuación siguiente:

**Iluminación especular = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**



 

En la tabla siguiente se identifican las variables, sus tipos y sus intervalos.



| Parámetro    | Valor predeterminado | Tipo          | Descripción                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Cs           | (0,0,0,0)     | D3DCOLORVALUE | Color especular.                                                                                                     |
| Sum          | N/D           | N/D           | Suma del componente especular de cada luz.                                                                       |
| N            | N/D           | D3DVECTOR     | Vértice normal.                                                                                                      |
| H            | N/D           | D3DVECTOR     | Vector a medio camino. Consulte la sección sobre el vector medio.                                                             |
| <sup>P</sup> | 0,0           | FLOAT         | Potencia de reflexión especular. El intervalo es de 0 a +infinito                                                                  |
| Ls           | (0,0,0,0)     | D3DCOLORVALUE | Color especular claro.                                                                                               |
| Atten        | N/D           | FLOAT         | Valor de atenuación ligera. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Zona         | N/D           | FLOAT         | Factor spotlight. Consulte [Atenuación y factor spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)        |



 

El valor de Cs es:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   color de vértice1, si el origen del material especular es D3DMCS COLOR1 y el primer color de vértice se proporciona \_ en la declaración de vértice.
-   vertex color2, si el origen del material especular es D3DMCS COLOR2 y el segundo color del vértice se proporciona \_ en la declaración del vértice.
-   color especular de material

> [!Note]  
> Si se usa cualquiera de las opciones de origen de material especular y no se proporciona el color del vértice, se usa el color especular del material.

 

Los componentes especulares se fijan para que estén entre 0 y 255, una vez que todas las luces se procesan e interpolan por separado.

## <a name="the-halfway-vector"></a>Vector a mitad de camino

El vector medio (H) existe a medio camino entre dos vectores: el vector de un vértice de objeto a la fuente de luz y el vector de un vértice de objeto a la posición de la cámara. Direct3D proporciona dos maneras de calcular el vector medio. Cuando LOCALVIEWER de D3DRS se establece en TRUE, el sistema calcula el vector a medio camino usando la posición de la cámara y la posición del vértice, junto con el vector de dirección \_ de la luz.  En la fórmula siguiente se muestra esto.

**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**



 



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Cp              | N/D           | D3DVECTOR | Posición de la cámara.                                             |
| Vp              | N/D           | D3DVECTOR | Posición del vértice.                                             |
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice a la posición de la luz. |



 

Determinar el vector medio de esta manera puede ser un proceso intensivo. Como alternativa, al establecer D3DRS \_ LOCALVIEWER = **FALSE,** se indica al sistema que actúe como si el punto de vista se encontrara infinitamente alejado en el eje Z. Esto se refleja en la fórmula siguiente.

**H = norm((0,0,1) + L <sub>dir</sub>)**



 

Esta configuración consume menos cálculos, pero es mucho menos precisa, por lo que es más usada por las aplicaciones que usan proyección ortogonal.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colore con el color claro especular de la escena y un color especular de material. El código se muestra a continuación.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



Según la ecuación, el color resultante para los vértices del objeto es una combinación del color del material y el color claro.

En las dos ilustraciones siguientes se muestra el color del material especular, que es gris, y el color claro especular, que es blanco.

![ilustración de una esfera gris](images/amb1.jpg)![ilustración de una esfera blanca](images/lightwhite.jpg)

El resaltado especular resultante se muestra en la ilustración siguiente.

![ilustración del resaltado especular](images/lights.jpg)

La combinación del resaltado especular con la iluminación ambiental y difusa genera la siguiente ilustración. Con los tres tipos de iluminación aplicados, esto se parece más claramente a un objeto realista.

![ilustración de la combinación del resaltado especular, la iluminación ambiental y la iluminación difusa](images/lightads.jpg)

La iluminación especular es más intensiva de calcular que la iluminación difusa. Normalmente se usa para proporcionar pistas visuales sobre el material de superficie. El resaltado especular varía en tamaño y color con el material de la superficie.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



