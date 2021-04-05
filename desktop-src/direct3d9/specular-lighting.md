---
description: El modelado de reflexión especular requiere que el sistema no solo sepa en qué dirección se desplaza la luz, sino también la dirección del ojo del espectador.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Iluminación especular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559524"
---
# <a name="specular-lighting-direct3d-9"></a>Iluminación especular (Direct3D 9)

El modelado de reflexión especular requiere que el sistema no solo sepa en qué dirección se desplaza la luz, sino también la dirección del ojo del espectador. El sistema utiliza una versión simplificada del modelo de reflexión especular de Phong, que emplea un vector a la mitad para aproximar la intensidad de reflexión especular.

El estado de iluminación predeterminado no calcula los reflejos especulares. Para habilitar la iluminación especular, asegúrese de establecer D3DRS \_ SPECULARENABLE en **true**.

## <a name="specular-lighting-equation"></a>Ecuación de iluminación especular

La iluminación especular se describe mediante la siguiente ecuación.



|                                                                             |
|-----------------------------------------------------------------------------|
| Iluminación especular = CS \* SUM \[ LS \* (N · H)<sup>P</sup> \* ATTEN \*\] |



 

En la tabla siguiente se identifican las variables, sus tipos y sus intervalos.



| Parámetro    | Valor predeterminado | Tipo          | Descripción                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Estrategia           | (0, 0, 0, 0)     | D3DCOLORVALUE | Color especular.                                                                                                     |
| Sum          | N/D           | N/D           | Suma del componente especular de cada luz.                                                                       |
| N            | N/D           | D3DVECTOR     | El vértice es normal.                                                                                                      |
| H            | N/D           | D3DVECTOR     | Vector medio. Vea la sección sobre el vector a la mitad.                                                             |
| <sup>P</sup> | 0,0           | FLOAT         | Potencia de reflexión especular. El intervalo es de 0 a + infinito                                                                  |
| LS           | (0, 0, 0, 0)     | D3DCOLORVALUE | Color especular claro.                                                                                               |
| Atten        | N/D           | FLOAT         | Valor de atenuación de luz. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Zona         | N/D           | FLOAT         | Factor destacado. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).        |



 

El valor de CS es:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   vértice color1, si el origen del material especular es D3DMCS \_ color1 y el primer color de vértice se proporciona en la declaración de vértices.
-   Vertex color2, si el origen del material especular es D3DMCS \_ color2 y el segundo color de vértice se proporciona en la declaración de vértices.
-   color especular de material

> [!Note]  
> Si se usa la opción de origen de material especular y no se proporciona el color de vértice, se usa el color especular de material.

 

Los componentes especulares están fijados de 0 a 255, después de que todas las luces se procesan y se interpolan por separado.

## <a name="the-halfway-vector"></a>Vector en la mitad

El vector medio (H) existe entre dos vectores: el vector de un vértice de objeto a la fuente de luz y el vector de un vértice de objeto a la posición de la cámara. Direct3D proporciona dos maneras de calcular el vector a la mitad. Cuando D3DRS \_ LOCALVIEWER se establece en **true**, el sistema calcula el vector en la mitad con la posición de la cámara y la posición del vértice, junto con el vector de dirección de la luz. La siguiente fórmula ilustra esto.



|                                           |
|-------------------------------------------|
| H = norma (Norm (CP-VP) + L<sub>dir</sub>) |



 



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| CP              | N/D           | D3DVECTOR | Posición de la cámara.                                             |
| Expertos              | N/D           | D3DVECTOR | Posición del vértice.                                             |
| <sub>Directorio</sub> L | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice hasta la posición de la luz. |



 

Determinar el vector a la mitad de esta manera puede consumir un uso intensivo de los cálculos. Como alternativa, el establecimiento de D3DRS \_ LOCALVIEWER = **false** indica al sistema que actúe como si el punto de vista se distan infinitamente en el eje z. Esto se refleja en la siguiente fórmula.



|                                     |
|-------------------------------------|
| H = normal ((0, 0, 1) + L<sub>dir</sub>) |



 

Este valor es menos computacionalmente intensivo, pero es mucho menos preciso, por lo que es mejor para las aplicaciones que usan la proyección ortogonal.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colorea utilizando el color de luz especular de la escena y un color especular de material. A continuación se muestra el código.


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

En las dos ilustraciones siguientes se muestra el color del material especular, que está atenuado, y el color de luz especular, que es blanco.

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera blanca](images/lightwhite.jpg)

El resaltado especular resultante se muestra en la siguiente ilustración.

![Ilustración del resaltado especular](images/lights.jpg)

La combinación del resaltado especular con el ambiente y la iluminación difusa produce la siguiente ilustración. Con los tres tipos de iluminación aplicados, esto se parece más claramente a un objeto realista.

![Ilustración de la combinación del resaltado especular, la iluminación ambiente y la iluminación difusa](images/lightads.jpg)

La iluminación especular es más intensiva para calcular que la luz difusa. Normalmente se usa para proporcionar pistas visuales sobre el material de la superficie. El resaltado especular varía en tamaño y color con el material de la superficie.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



