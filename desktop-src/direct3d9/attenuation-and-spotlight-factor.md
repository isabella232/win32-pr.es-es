---
description: Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de luz y el cono de foco. Estos términos se describen a continuación.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Atenuación y factor de Spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552825"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Atenuación y factor de Spotlight (Direct3D 9)

Los componentes de iluminación difusa y especular de la ecuación de iluminación global contienen términos que describen la atenuación de luz y el cono de foco. Estos términos se describen a continuación.

## <a name="attenuation"></a>Atenuación

La atenuación de una luz depende del tipo de luz y de la distancia entre la luz y la posición del vértice. Para calcular la atenuación, use una de las siguientes ecuaciones.

ATTEN = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + Att2<sub>i</sub> \* d ²)

Donde:



| Parámetro        | Valor predeterminado | Tipo  | Descripción                                     | Intervalo          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación constante                     | de 0 a + infinito |
| Att1<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación lineal                       | de 0 a + infinito |
| Att2<sub>i</sub> | 0,0           | FLOAT | Factor de atenuación cuadrático                    | de 0 a + infinito |
| d                | N/D           | FLOAT | Distancia desde la posición del vértice hasta la posición de la luz | N/D            |



 

-   ATTEN = 1, si la luz es una luz direccional.
-   ATTEN = 0, si la distancia entre la luz y el vértice supera el intervalo de la luz.

Los valores att0, Att1, Att2 se especifican mediante los miembros Attenuation0, Attenuation1 y Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).

La distancia entre la luz y la posición del vértice siempre es positiva.

d = \| <sub>directorio</sub> L \|

Donde:



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>Directorio</sub> L | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice hasta la posición de la luz |



 

Si d es mayor que el intervalo de la luz, es decir, el miembro del intervalo de una estructura [**D3DLIGHT9**](d3dlight9.md) , Direct3D no realiza más cálculos de atenuación y no aplica ningún efecto de la luz al vértice.

Las constantes de atenuación actúan como coeficientes en la fórmula; puede generar diversas curvas de atenuación realizando ajustes sencillos en ellas. Puede establecer Attenuation1 en 1,0 para crear una luz que no se atenuará pero que siga limitada por el intervalo, o puede experimentar con valores diferentes para lograr distintos efectos de atenuación.

La atenuación en el intervalo máximo de la luz no es 0,0. Para evitar que las luces aparezcan repentinamente cuando están en el intervalo de luz, una aplicación puede aumentar el intervalo de luz. O bien, la aplicación puede configurar constantes de atenuación para que el factor de atenuación esté cerca de 0,0 en el intervalo de luz. El valor de atenuación se multiplica por los componentes rojo, verde y azul del color de la luz para escalar la intensidad de la luz como un factor de la luz de distancia que se desplaza a un vértice.

## <a name="spotlight-factor"></a>Factor destacado

La siguiente ecuación especifica el factor destacado.

![ecuación del factor de Spotlight](images/dx8light9.png)



| Parámetro         | Valor predeterminado | Tipo  | Descripción                              | Intervalo                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| Rho<sub>i</sub>   | N/D           | FLOAT | coseno (ángulo) para los focos            | N/D                      |
| Phi<sub>i</sub>   | 0,0           | FLOAT | Penumbra ángulo de foco i en radianes | \[Theta<sub>i</sub>, PI) |
| Theta<sub>i</sub> | 0,0           | FLOAT | Umbra ángulo de foco i en radianes    | \[0, PI)                 |
| disminución           | 0,0           | FLOAT | Factor de difuminación                           | (-Infinity, + infinito)   |



 

Donde:

Rho = norma (L<sub>DC</sub>)<sup>.</sup> norma (L<sub>dir</sub>)

y:



| Parámetro       | Valor predeterminado | Tipo      | Descripción                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>DC</sub> de L | N/D           | D3DVECTOR | El negativo de la dirección de la luz en el espacio de la cámara         |
| <sub>Directorio</sub> L | N/D           | D3DVECTOR | Vector de dirección desde la posición del vértice hasta la posición de la luz |



 

Después de calcular la atenuación de luz, Direct3D también tiene en cuenta los efectos destacados, si procede, el ángulo que la luz refleja de una superficie y la reflectancia del material actual para calcular los componentes difusos y especulares para ese vértice. Para obtener más información, consulte [Spotlight](light-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Matemáticas de iluminación](mathematics-of-lighting.md)
</dt> </dl>

 

 



