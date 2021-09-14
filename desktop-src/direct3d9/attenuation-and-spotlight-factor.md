---
description: Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de la luz y el cono de foco. Estos términos se describen a continuación.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Atenuación y factor spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060758"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Atenuación y factor spotlight (Direct3D 9)

Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de la luz y el cono de foco. Estos términos se describen a continuación.

## <a name="attenuation"></a>Atenuación

La atenuación de una luz depende del tipo de luz y la distancia entre la luz y la posición del vértice. Para calcular la atenuación, use una de las siguientes ecuaciones.

Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d):

Donde:



| Parámetro        | Valor predeterminado | Tipo  | Descripción                                     | Intervalo          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación constante                     | De 0 a +infinito |
| att1<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación lineal                       | De 0 a +infinito |
| att2<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación cuadrática                    | De 0 a +infinito |
| d                | N/D           | FLOAT | Distancia entre la posición del vértice y la posición ligera | N/D            |



 

-   Atten = 1, si la luz es una luz direccional.
-   Atten = 0, si la distancia entre la luz y el vértice supera el intervalo de la luz.

Los valores att0, att1 y att2 se especifican mediante los miembros Atenuación0, Atenuación1 y Atenuación2 de [**D3DLIGHT9.**](d3dlight9.md)

La distancia entre la luz y la posición del vértice siempre es positiva.

d = \| L<sub>dir</sub>\|

Donde:



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice a la posición de la luz |



 

Si d es mayor que el intervalo de la luz, es decir, el miembro Range de una estructura [**D3DLIGHT9,**](d3dlight9.md) Direct3D no realiza ningún cálculo de atenuación adicional y no aplica ningún efecto de la luz al vértice.

Las constantes de atenuación actúan como coeficientes en la fórmula: puede generar una variedad de curvas de atenuación realizando ajustes sencillos en ellas. Puede establecer Atenuación1 en 1.0 para crear una luz que no se atenua, pero que sigue estando limitada por intervalo, o puede experimentar con valores diferentes para lograr varios efectos de atenuación.

La atenuación en el intervalo máximo de la luz no es 0,0. Para evitar que las luces aparezcan repentinamente cuando están en el intervalo de luz, una aplicación puede aumentar el intervalo de luz. O bien, la aplicación puede configurar constantes de atenuación para que el factor de atenuación esté cerca de 0,0 en el intervalo de luz. El valor de atenuación se multiplica por los componentes rojo, verde y azul del color de la luz para escalar la intensidad de la luz como un factor de la distancia que la luz recorre a un vértice.

## <a name="spotlight-factor"></a>Spotlight Factor

La siguiente ecuación especifica el factor destacado.

![ecuación del factor destacado](images/dx8light9.png)



| Parámetro         | Valor predeterminado | Tipo  | Descripción                              | Intervalo                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| i<sub></sub>   | N/D           | FLOAT | cosine(angle) for spotlight i            | N/D                      |
| phi<sub>i</sub>   | 0,0           | FLOAT | Ángulo de penumbra de spotlight i en radianes | \[theta<sub>i</sub>, pi) |
| theta<sub>i</sub> | 0,0           | FLOAT | Ángulo de Umbra de spotlight i en radianes    | \[0, pi)                 |
| Difuminación           | 0,0           | FLOAT | Factor de caída                           | (-infinity, +infinity)   |



 

Donde:

, = norm(L<sub>dcs</sub>)<sup>.</sup> norm(L<sub>dir</sub>)

y:



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dcs</sub> | N/D           | D3DVECTOR | Negativo de la dirección de la luz en el espacio de la cámara         |
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice a la posición de la luz |



 

Después de calcular la atenuación de luz, Direct3D también tiene en cuenta los efectos de los focos si procede, el ángulo que refleja la luz de una superficie y la reflectancia del material actual para calcular los componentes difusos y especulares para ese vértice. Para obtener más información, vea [SpotLight](light-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



