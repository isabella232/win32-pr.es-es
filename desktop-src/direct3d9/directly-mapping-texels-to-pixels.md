---
description: Al representar la salida 2D mediante vértices transformados previamente, se debe tener cuidado para asegurarse de que cada área de textura se corresponda correctamente con un área de un solo píxel; de lo contrario, puede producirse una distorsión de textura.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Asignación directa de elementos de textura a píxeles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7294b88fb8b672aea980dbb23cb4e7c5bbd2bfdbf4d33a5078a09dbfa3084d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988289"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Asignación directa de elementos de textura a píxeles (Direct3D 9)

Al representar la salida 2D mediante vértices transformados previamente, se debe tener cuidado para asegurarse de que cada área de textura se corresponda correctamente con un área de un solo píxel; de lo contrario, puede producirse una distorsión de textura. Al comprender los conceptos básicos del proceso que sigue Direct3D al rasterizar y texturizar triángulos, puede asegurarse de que la aplicación Direct3D representa correctamente la salida 2D.

![ilustración de una pantalla de resolución 6x6](images/maptex-fig1.png)

En el diagrama anterior se muestran píxeles modelados como cuadrados. En realidad, sin embargo, los píxeles son puntos, no cuadrados. Cada cuadrado del diagrama anterior indica el área que el píxel enciende, pero un píxel siempre es solo un punto en el centro de un cuadrado. Esta distinción, aunque parece pequeña, es importante. En el diagrama siguiente se muestra una ilustración mejor de la misma pantalla.

![ilustración de una pantalla que consta de píxeles](images/maptex-fig2.png)

El diagrama anterior muestra correctamente cada píxel físico como un punto en el centro de cada celda. La coordenada del espacio de pantalla (0, 0) se encuentra directamente en el píxel superior izquierdo y, por tanto, en el centro de la celda superior izquierda. Por lo tanto, la esquina superior izquierda de la pantalla se encuentra en (-0,5, -0,5) porque se trata de 0,5 celdas a la izquierda y 0,5 celdas hacia arriba desde el píxel superior izquierdo. Direct3D representará un quad con esquinas en (0, 0) y (4, 4), como se muestra en la ilustración siguiente.

![ilustración de un esquema de un cuadrándster no assterizado entre (0, 0) y (4, 4)](images/maptex-fig3.png)

En la ilustración anterior se muestra dónde está el cuadrándculo matemático en relación con la presentación, pero no muestra el aspecto del cuadrándular una vez que Direct3D lo rasteriza y lo envía a la pantalla. De hecho, es imposible que una presentación de trama rellene el cuadrándido exactamente como se muestra porque los bordes del cuadrándular no coinciden con los límites entre las celdas de píxeles. En otras palabras, dado que cada píxel solo puede mostrar un solo color, cada celda de píxel se rellena con un solo color; Si la presentación representara el cuadránd cuadrado exactamente como se muestra, las celdas de píxeles a lo largo del borde del cuadránguido tendrían que mostrar dos colores distintos: azul, donde está cubierto por el cuadrándular y blanco, donde solo está visible el fondo.

En su lugar, el hardware gráfico tiene la tarea de determinar qué píxeles se deben rellenar para aproximarse al cuadránxel. Este proceso se denomina rasterización y se detalla en Reglas de [rasterización (Direct3D 9).](rasterization-rules.md) En este caso concreto, el cuadrándular rasterizado se muestra en la ilustración siguiente.

![ilustración de un cuadrándido sin texto dibujado de (0,0) a (4,4)](images/maptex-fig4.png)

Tenga en cuenta que el quad pasado a Direct3D tiene esquinas en (0, 0) y (4, 4), pero la salida rasterizada (la ilustración anterior) tiene esquinas en (-0,5,-0,5) y (3,5,3,5). Compare las dos ilustraciones anteriores para ver las diferencias de representación. Puede ver que lo que representa realmente la pantalla es el tamaño correcto, pero se ha desplazado por las celdas -0,5 en las direcciones x e y. Sin embargo, a excepción de las técnicas de muestreo múltiple, esta es la mejor aproximación posible al cuadrángulo. (Consulte el [ejemplo antialias para](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) obtener una cobertura exhaustiva del muestreo múltiple). Tenga en cuenta que si el rasterizador rellena todas las celdas que ha cruzado el cuadrándulco, el área resultante sería de dimensión 5 x 5 en lugar de las 4 x 4 deseadas.

Si supone que las coordenadas de pantalla se originan en la esquina superior izquierda de la cuadrícula de visualización en lugar del píxel superior izquierdo, el cuadrándular aparece exactamente como se esperaba. Sin embargo, la diferencia queda clara cuando se le da una textura al cuadrándular. En la ilustración siguiente se muestra la textura de 4 x 4 que se asignará directamente al cuadrándculo.

![ilustración de una textura 4x4](images/maptex-fig5.png)

Dado que la textura es de 4 x 4 elementos de textura y el cuadrándido es de 4 x 4 píxeles, puede esperar que el cuadrándido con textura aparezca exactamente igual que la textura, independientemente de la ubicación en la pantalla donde se dibuja el cuadrándido. Sin embargo, este no es el caso; incluso los pequeños cambios de posición influyen en cómo se muestra la textura. En la ilustración siguiente se muestra cómo se muestra un cuadrándculo entre (0, 0) y (4, 4) después de que se rasterice y se textura.

![ilustración de un cuadrándido con textura extraído de (0, 0) y (4, 4)](images/maptex-fig6.png)

El cuadrándculo dibujado en la ilustración anterior muestra la salida con textura (con un modo de filtrado lineal y un modo de direccionamiento de fijación) con el contorno rasterizado superpuesto. En el resto de este artículo se explica exactamente por qué la salida tiene el aspecto que tiene en lugar de parecerse a la textura, pero para los que quieren la solución, aquí está: Los bordes del cuadrándculo de entrada deben encontrarse sobre las líneas de límite entre las celdas de píxeles. Con solo desplazar las coordenadas de cuadránxel x e y por -0,5 unidades, las celdas de texel cubrirán perfectamente las celdas de píxel y el cuadrándular se puede volver a crear perfectamente en la pantalla. (En la última ilustración de este tema se muestra el cuadrándculo en las coordenadas corregidas).

Los detalles de por qué la salida rasterizada solo tiene un ligero parecido a la textura de entrada están directamente relacionados con la forma en que Direct3D direcciona y muestrea texturas. A continuación se da por supuesto que tiene una buena comprensión del espacio de [coordenadas](texture-coordinates.md) de textura y el filtrado [de textura bilineal.](bilinear-texture-filtering.md)

Volviendo a la investigación de la salida de píxeles extraños, tiene sentido hacer un seguimiento del color de salida hasta el sombreador de píxeles: se llama al sombreador de píxeles para que cada píxel seleccionado forme parte de la forma rasterizada. El cuadrándido azul sólido representado en una ilustración anterior podría tener un sombreador particularmente sencillo:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Para el cuadrándido con textura, el sombreador de píxeles debe cambiarse ligeramente:


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



Ese código supone que la textura 4 x 4 se almacena en MyTexture. Como se muestra, el muestreador de textura MySampler está establecido para realizar el filtrado bilineal en MyTexture. Se llama al sombreador de píxeles una vez para cada píxel rasterizado y cada vez que el color devuelto es el color de textura muestreado en vTexCoord. Cada vez que se llama al sombreador de píxeles, el argumento vTexCoord se establece en las coordenadas de textura de ese píxel. Esto significa que el sombreador pide al muestreador de textura el color de textura filtrado en la ubicación exacta del píxel, como se detalla en la ilustración siguiente.

![ilustración de ubicaciones de muestreo para coordenadas de textura](images/maptex-fig7.png)

La textura (que se muestra superpuesta) se muestrea directamente en ubicaciones de píxeles (se muestra como puntos negros). Las coordenadas de textura no se ven afectadas por la rasterización (permanecen en el espacio de pantalla proyectado del cuadrándular original). Los puntos negros muestran dónde están los píxeles de rasterización. Las coordenadas de textura de cada píxel se determinan fácilmente mediante la interpolación de las coordenadas almacenadas en cada vértice: el píxel en (0,0) coincide con el vértice en (0, 0); Por lo tanto, las coordenadas de textura en ese píxel son simplemente las coordenadas de textura almacenadas en ese vértice, UV (0,0, 0,0). Para el píxel en (3, 1), las coordenadas interpoladas son UV (0,75, 0,25) porque ese píxel se encuentra en tres cuartos del ancho de la textura y un cuarto de su altura. Estas coordenadas interpoladas son las que se pasan al sombreador de píxeles.

Los elementos de textura no se alinean con los píxeles de este ejemplo; cada píxel (y, por tanto, cada punto de muestreo) se coloca en la esquina de cuatro elementos de textura. Dado que el modo de filtrado se establece en Lineal, el muestreador promediará los colores de los cuatro elementos de textura que comparten esa esquina. Esto explica por qué el píxel que se espera que sea rojo es realmente gris de tres cuartos más uno cuarto rojo, el píxel que se espera que sea verde es una mitad gris más un cuarto rojo más un cuarto verde, y así sucesivamente.

Para corregir este problema, todo lo que necesita hacer es asignar correctamente el cuadránxel a los píxeles a los que se va a rasterizar y, por tanto, asignar correctamente los elementos de textura a píxeles. En la ilustración siguiente se muestran los resultados de dibujar el mismo cuadrándculo entre (-0,5, -0,5) y (3,5, 3,5), que es el cuadrándculo previsto desde el principio.

![ilustración de un cuadrándido con textura que coincide con el cuadrándido rasterizado](images/maptex-fig8.png)

En la ilustración anterior se muestra que el cuadrándido (que se muestra de (-0,5, -0,5) a (3,5, 3,5)) coincide exactamente con el área rasterizada.

## <a name="summary"></a>Resumen

En resumen, los píxeles y los elementos de textura son realmente puntos, no bloques sólidos. El espacio de pantalla se origina en el píxel superior izquierdo, pero las coordenadas de textura se originan en la esquina superior izquierda de la cuadrícula de la textura. Lo más importante es que recuerde restar 0,5 unidades de los componentes x e y de las posiciones de los vértices al trabajar en un espacio de pantalla transformado para alinear correctamente los elementos de textura con píxeles.

El código siguiente es un ejemplo de desplazamiento de los vértices de un cuadrado de 256 por 256 para mostrar correctamente una textura de 256 por 256 en el espacio de pantalla transformado.


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 



