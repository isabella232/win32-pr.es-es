---
description: La iluminación ambiente proporciona iluminación constante para una escena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Iluminación ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539033"
---
# <a name="ambient-lighting-direct3d-9"></a>Iluminación ambiente (Direct3D 9)

La iluminación ambiente proporciona iluminación constante para una escena. Ilumina todos los vértices de objeto de la misma forma porque no depende de ningún otro factor de iluminación, como las normales de vértice, la dirección clara, la posición de la luz, el intervalo o la atenuación. Es el tipo de iluminación más rápido, pero genera los resultados menos realistas. Direct3D contiene una única propiedad de luz ambiente global que puede usar sin crear ninguna luz. Como alternativa, puede establecer cualquier objeto de luz para proporcionar iluminación ambiente. La iluminación ambiente para una escena se describe en la siguiente ecuación.

Iluminación ambiente = C ₐ \* \[ g ₐ + SUM (ATTEN<sub>i</sub>i i i e \* <sub></sub> \* <sub>IA</sub>)\]

Donde:



| Parámetro         | Valor predeterminado | Tipo          | Descripción                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| C ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Color ambiental de material                                                                                                         |
| G ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Color ambiente global                                                                                                           |
| ATTEN<sub>i</sub> | (0, 0, 0, 0)     | D3DCOLORVALUE | Atenuación de la luz i. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Puntual<sub></sub>  | (0, 0, 0, 0)     | D3DVECTOR     | Factor destacado de la luz i. Vea [atenuación y factor de Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).  |
| Sum               | N/D           | N/D           | Suma de la luz ambiente                                                                                                       |
| L<sub>AI</sub>    | (0, 0, 0, 0)     | D3DVECTOR     | Color ambiente claro de la luz iésimo                                                                                           |



 

El valor de C ₐ es:

-   Vertex color1, si AMBIENTMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.
-   Vertex color2, si AMBIENTMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.
-   color ambiente de material.

> [!Note]  
> Si se usa la opción AMBIENTMATERIALSOURCE y no se proporciona el color del vértice, se usa el color ambiente del material.

 

Para usar el color ambiente de material, use SetMaterial como se muestra en el código de ejemplo siguiente.

G ₐ es el color ambiente global. Se establece mediante SetRenderState (D3DRS \_ ambiente). Hay un color ambiente global en una escena de Direct3D. Este parámetro no está asociado a un objeto de Direct3D Light.

L<sub>AI</sub> es el color ambiente de la luz iésimo de la escena. Cada luz de Direct3D tiene un conjunto de propiedades, uno de los cuales es el color ambiente. El término SUM (L<sub>AI</sub>) es una suma de todos los colores de ambiente de la escena.

## <a name="example"></a>Ejemplo

En este ejemplo, el objeto se colorea utilizando la luz ambiente de la escena y un color ambiente de material.


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

En las dos ilustraciones siguientes se muestra el color del material, que está atenuado y el color claro, que es rojo brillante.

![Ilustración de una esfera gris](images/amb1.jpg)![Ilustración de una esfera roja](images/lightred.jpg)

La escena resultante se muestra en la siguiente ilustración. El único objeto de la escena es una esfera. Luz ambiente ilumina todos los vértices de objetos con el mismo color. No depende de la dirección de la luz o del vértice normal. Como resultado, la esfera tiene el aspecto de un círculo 2D porque no hay ninguna diferencia en el sombreado en torno a la superficie del objeto.

![Ilustración de una esfera con iluminación ambiente](images/lighta.jpg)

Para dar una apariencia más realista a los objetos, aplique la iluminación difusa o especular además de la iluminación ambiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



