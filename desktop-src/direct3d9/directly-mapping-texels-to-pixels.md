---
description: Al representar la salida 2D con vértices previamente transformados, se debe tener cuidado para asegurarse de que cada área de textura se corresponde correctamente con un área de un solo píxel; de lo contrario, se puede producir una distorsión de textura.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Asignación directa de textura a píxeles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274734"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Asignación directa de textura a píxeles (Direct3D 9)

Al representar la salida 2D con vértices previamente transformados, se debe tener cuidado para asegurarse de que cada área de textura se corresponde correctamente con un área de un solo píxel; de lo contrario, se puede producir una distorsión de textura. Al comprender los aspectos básicos del proceso que Direct3D sigue al rasterizar y texturizar triángulos, puede asegurarse de que la aplicación Direct3D representa correctamente la salida 2D.

![Ilustración de una pantalla de resolución de 6x6](images/maptex-fig1.png)

En el diagrama anterior se muestran los píxeles que se modelan como cuadrados. En realidad, sin embargo, los píxeles son puntos, no cuadrados. Cada cuadrado del diagrama anterior indica el área iluminada por el píxel, pero un píxel siempre es simplemente un punto en el centro de un cuadrado. Esta distinción, a pesar de parecer pequeña, es importante. En el diagrama siguiente se muestra una ilustración mejor de la misma pantalla.

![Ilustración de una presentación que consta de píxeles](images/maptex-fig2.png)

El diagrama anterior muestra correctamente cada píxel físico como un punto en el centro de cada celda. La coordenada de espacio de pantalla (0,0) se encuentra directamente en el píxel superior izquierdo y, por tanto, en el centro de la celda superior izquierda. Por lo tanto, la esquina superior izquierda de la pantalla está en (-0,5,-0,5) porque es 0,5 celdas a la izquierda y 0,5 celdas hacia arriba desde el píxel superior izquierdo. Direct3D representará un cuádruple con esquinas en (0,0) y (4, 4), tal y como se muestra en la siguiente ilustración.

![Ilustración de un contorno de una cuádruple desrasterizada entre (0,0) y (4, 4)](images/maptex-fig3.png)

En la ilustración anterior se muestra dónde se encuentra el cuádruple matemático en relación con la pantalla, pero no se muestra el aspecto que tendrá la cuádruple una vez que Direct3D lo rasteriza y lo envía a la pantalla. De hecho, es imposible que una pantalla de trama llene el cuádruple exactamente como se muestra porque los bordes de la cuádruple no coinciden con los límites entre las celdas de píxeles. En otras palabras, dado que cada píxel solo puede mostrar un único color, cada celda de píxel se rellena con un solo color. Si la pantalla fuera a representar la cuádruple exactamente como se muestra, las celdas de píxeles en el borde de la cuádruple deberán mostrar dos colores distintos: azul, donde están incluidos en el cuádruple y el blanco, donde solo está visible el fondo.

En su lugar, el hardware gráfico tiene la tarea de determinar qué píxeles deben rellenarse para aproximarse al cuádruple. Este proceso se denomina rasterización y se detalla en [reglas de rasterización (Direct3D 9)](rasterization-rules.md). En este caso concreto, el cuádruple rasterizado se muestra en la siguiente ilustración.

![Ilustración de una Quad no texturizada dibujada de (0,0) a (4, 4)](images/maptex-fig4.png)

Tenga en cuenta que el cuádruple pasado a Direct3D tiene esquinas en (0,0) y (4, 4), pero la salida rasterizada (la ilustración anterior) tiene esquinas en (-0.5,-0,5) y (3.5, 3.5). Compare las dos ilustraciones anteriores para las diferencias de representación. Puede ver que lo que la pantalla representa realmente es el tamaño correcto, pero que se ha desplazado por 0,5 celdas en las direcciones x e y. Sin embargo, a excepción de las técnicas de muestreo múltiple, esta es la mejor aproximación posible a la cuádruple. (Vea el [ejemplo antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) para obtener una cobertura exhaustiva del muestreo múltiple). Tenga en cuenta que si el rasterizador ha llenado cada celda del fotocuadrante, el área resultante sería de dimensión 5 x 5 en lugar de los 4 x 4 deseados.

Si se da por supuesto que las coordenadas de pantalla se originan en la esquina superior izquierda de la cuadrícula de pantalla en lugar de en el píxel superior izquierdo, el cuádruple aparece exactamente como se esperaba. Sin embargo, la diferencia queda clara cuando el cuádruple recibe una textura. En la ilustración siguiente se muestra la textura de 4 x 4 que asignará directamente a la cuádruple.

![Ilustración de una textura 4x4](images/maptex-fig5.png)

Dado que la textura es 4 x 4 textura y la cuádruple es 4 x 4 píxeles, podría esperar que el cuádruple con textura aparezca exactamente igual que la textura, independientemente de la ubicación de la pantalla en la que se dibuje la cuádruple. Sin embargo, este no es el caso; incluso los pequeños cambios en la posición afectan al modo en que se muestra la textura. En la ilustración siguiente se muestra cómo se muestra un cuádruple entre (0,0) y (4, 4) después de ser rasterizado y con textura.

![Ilustración de una cuádruple con textura dibujada desde (0,0) y (4, 4)](images/maptex-fig6.png)

La línea cuádruple dibujada en la ilustración anterior muestra la salida con textura (con un modo de filtrado lineal y un modo de direccionamiento de abrazadera) con el contorno rasterizado superpuesto. En el resto de este artículo se explica exactamente por qué el resultado tiene el aspecto que tiene en lugar de mirar la textura, pero para aquellos que quieren la solución, aquí es: los bordes de la entrada cuádruple deben estar en las líneas de límite entre las celdas de píxeles. Con solo desplazar las coordenadas x e y en 0,5 unidades, las celdas de textura expondrán perfectamente las celdas de píxeles y la cuádruple se puede volver a crear perfectamente en la pantalla. (La última ilustración de este tema muestra la cuádruple en las coordenadas corregidas).

Los detalles de por qué la salida rasterizada solo tiene una ligera similitud con la textura de entrada se relacionan directamente con la forma en que Direct3D dirige y muestra las texturas. Lo siguiente supone que tiene un buen conocimiento del [espacio de coordenadas de textura](texture-coordinates.md) y el [filtrado de textura bilineal](bilinear-texture-filtering.md).

Al volver a nuestra investigación de la salida de píxeles extrañas, tiene sentido hacer un seguimiento del color de salida hasta el sombreador de píxeles: se llama al sombreador de píxeles por cada píxel seleccionado para formar parte de la forma rasterizada. El cuádruple azul sólido representado en una ilustración anterior podría tener un sombreador especialmente sencillo:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



En el caso del cuádruple con textura, el sombreador de píxeles debe cambiarse ligeramente:


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



Ese código supone que la textura 4 x 4 se almacena en la textura. Como se muestra, la muestra de texturas de el muestreador se establece para realizar un filtrado bilineal en la textura. El sombreador de píxeles se llama una vez para cada píxel rasterizado y cada vez que el color devuelto es el color de la textura muestreada en vTexCoord. Cada vez que se llama al sombreador de píxeles, el argumento vTexCoord se establece en las coordenadas de textura en ese píxel. Esto significa que el sombreador solicita el muestrario de texturas para el color de la textura filtrada en la ubicación exacta del píxel, tal como se detalla en la siguiente ilustración.

![Ilustración de las ubicaciones de muestreo para las coordenadas de textura](images/maptex-fig7.png)

La textura (mostrada superpuesta) se muestrea directamente en ubicaciones de píxeles (se muestran como puntos negros). Las coordenadas de textura no se ven afectadas por la rasterización (permanecen en el espacio de pantalla proyectado del cuádruple original). Los puntos negros muestran dónde están los píxeles de rasterización. Las coordenadas de textura en cada píxel se determinan fácilmente mediante la interpolación de las coordenadas almacenadas en cada vértice: el píxel en (0,0) coincide con el vértice en (0,0); por lo tanto, las coordenadas de textura en ese píxel son simplemente las coordenadas de textura almacenadas en ese vértice, UV (0,0, 0,0). Para el píxel en (3, 1), las coordenadas interpoladas son UV (0,75, 0,25) porque ese píxel se encuentra en tres cuartos del ancho de la textura y un cuarto de su alto. Estas coordenadas interpoladas son las que se pasan al sombreador de píxeles.

Los textura no se alinean con los píxeles de este ejemplo; cada píxel (y, por tanto, cada punto de muestreo) se coloca en la esquina de cuatro textura. Dado que el modo de filtrado está establecido en lineal, la muestra calculará el promedio de los colores de los cuatro textura que comparten esa esquina. Esto explica por qué el píxel que se espera que sea rojo es en realidad tres cuartos de color gris más un cuarto rojo, mientras que el píxel que se espera que sea verde es una mitad de gris y un cuarto de color rojo más uno-cuarto verde, y así sucesivamente.

Para solucionar este problema, lo único que tiene que hacer es asignar correctamente el cuádruple a los píxeles en los que se rasterizará y, por tanto, asignar correctamente el textura a los píxeles. En la ilustración siguiente se muestran los resultados del dibujo de la misma Quad entre (-0,5,-0,5) y (3,5, 3,5), que es el cuádruple previsto desde el principio.

![Ilustración de una cuádruple con textura que coincide con el cuádruple rasterizado](images/maptex-fig8.png)

En la ilustración anterior se muestra que el cuádruple (mostrado de (-0,5,-0,5) a (3,5, 3,5)) coincide exactamente con el área rasterizada.

## <a name="summary"></a>Resumen

En Resumen, los píxeles y textura son realmente puntos, no bloques sólidos. El espacio de la pantalla se origina en el píxel superior izquierdo, pero las coordenadas de textura se originan en la esquina superior izquierda de la cuadrícula de la textura. Lo más importante es que no olvide restar 0,5 unidades de los componentes x e y de las posiciones de los vértices al trabajar en un espacio de pantalla transformado para alinear correctamente textura con píxeles.

El código siguiente es un ejemplo de desplazamiento de los vértices de un cuadrado 256 por 256 para mostrar correctamente una textura 256 by 256 en el espacio de pantalla transformado.


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

 

 



