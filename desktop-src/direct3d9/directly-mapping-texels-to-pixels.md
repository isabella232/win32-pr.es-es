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
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="7798b-103">Asignación directa de textura a píxeles (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7798b-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="7798b-104">Al representar la salida 2D con vértices previamente transformados, se debe tener cuidado para asegurarse de que cada área de textura se corresponde correctamente con un área de un solo píxel; de lo contrario, se puede producir una distorsión de textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="7798b-105">Al comprender los aspectos básicos del proceso que Direct3D sigue al rasterizar y texturizar triángulos, puede asegurarse de que la aplicación Direct3D representa correctamente la salida 2D.</span><span class="sxs-lookup"><span data-stu-id="7798b-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![Ilustración de una pantalla de resolución de 6x6](images/maptex-fig1.png)

<span data-ttu-id="7798b-107">En el diagrama anterior se muestran los píxeles que se modelan como cuadrados.</span><span class="sxs-lookup"><span data-stu-id="7798b-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="7798b-108">En realidad, sin embargo, los píxeles son puntos, no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="7798b-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="7798b-109">Cada cuadrado del diagrama anterior indica el área iluminada por el píxel, pero un píxel siempre es simplemente un punto en el centro de un cuadrado.</span><span class="sxs-lookup"><span data-stu-id="7798b-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="7798b-110">Esta distinción, a pesar de parecer pequeña, es importante.</span><span class="sxs-lookup"><span data-stu-id="7798b-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="7798b-111">En el diagrama siguiente se muestra una ilustración mejor de la misma pantalla.</span><span class="sxs-lookup"><span data-stu-id="7798b-111">A better illustration of the same display is shown in the following diagram.</span></span>

![Ilustración de una presentación que consta de píxeles](images/maptex-fig2.png)

<span data-ttu-id="7798b-113">El diagrama anterior muestra correctamente cada píxel físico como un punto en el centro de cada celda.</span><span class="sxs-lookup"><span data-stu-id="7798b-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="7798b-114">La coordenada de espacio de pantalla (0,0) se encuentra directamente en el píxel superior izquierdo y, por tanto, en el centro de la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="7798b-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="7798b-115">Por lo tanto, la esquina superior izquierda de la pantalla está en (-0,5,-0,5) porque es 0,5 celdas a la izquierda y 0,5 celdas hacia arriba desde el píxel superior izquierdo.</span><span class="sxs-lookup"><span data-stu-id="7798b-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="7798b-116">Direct3D representará un cuádruple con esquinas en (0,0) y (4, 4), tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7798b-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![Ilustración de un contorno de una cuádruple desrasterizada entre (0,0) y (4, 4)](images/maptex-fig3.png)

<span data-ttu-id="7798b-118">En la ilustración anterior se muestra dónde se encuentra el cuádruple matemático en relación con la pantalla, pero no se muestra el aspecto que tendrá la cuádruple una vez que Direct3D lo rasteriza y lo envía a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7798b-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="7798b-119">De hecho, es imposible que una pantalla de trama llene el cuádruple exactamente como se muestra porque los bordes de la cuádruple no coinciden con los límites entre las celdas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7798b-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="7798b-120">En otras palabras, dado que cada píxel solo puede mostrar un único color, cada celda de píxel se rellena con un solo color. Si la pantalla fuera a representar la cuádruple exactamente como se muestra, las celdas de píxeles en el borde de la cuádruple deberán mostrar dos colores distintos: azul, donde están incluidos en el cuádruple y el blanco, donde solo está visible el fondo.</span><span class="sxs-lookup"><span data-stu-id="7798b-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="7798b-121">En su lugar, el hardware gráfico tiene la tarea de determinar qué píxeles deben rellenarse para aproximarse al cuádruple.</span><span class="sxs-lookup"><span data-stu-id="7798b-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="7798b-122">Este proceso se denomina rasterización y se detalla en [reglas de rasterización (Direct3D 9)](rasterization-rules.md).</span><span class="sxs-lookup"><span data-stu-id="7798b-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="7798b-123">En este caso concreto, el cuádruple rasterizado se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7798b-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![Ilustración de una Quad no texturizada dibujada de (0,0) a (4, 4)](images/maptex-fig4.png)

<span data-ttu-id="7798b-125">Tenga en cuenta que el cuádruple pasado a Direct3D tiene esquinas en (0,0) y (4, 4), pero la salida rasterizada (la ilustración anterior) tiene esquinas en (-0.5,-0,5) y (3.5, 3.5).</span><span class="sxs-lookup"><span data-stu-id="7798b-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="7798b-126">Compare las dos ilustraciones anteriores para las diferencias de representación.</span><span class="sxs-lookup"><span data-stu-id="7798b-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="7798b-127">Puede ver que lo que la pantalla representa realmente es el tamaño correcto, pero que se ha desplazado por 0,5 celdas en las direcciones x e y.</span><span class="sxs-lookup"><span data-stu-id="7798b-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="7798b-128">Sin embargo, a excepción de las técnicas de muestreo múltiple, esta es la mejor aproximación posible a la cuádruple.</span><span class="sxs-lookup"><span data-stu-id="7798b-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="7798b-129">(Vea el [ejemplo antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) para obtener una cobertura exhaustiva del muestreo múltiple). Tenga en cuenta que si el rasterizador ha llenado cada celda del fotocuadrante, el área resultante sería de dimensión 5 x 5 en lugar de los 4 x 4 deseados.</span><span class="sxs-lookup"><span data-stu-id="7798b-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="7798b-130">Si se da por supuesto que las coordenadas de pantalla se originan en la esquina superior izquierda de la cuadrícula de pantalla en lugar de en el píxel superior izquierdo, el cuádruple aparece exactamente como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="7798b-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="7798b-131">Sin embargo, la diferencia queda clara cuando el cuádruple recibe una textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="7798b-132">En la ilustración siguiente se muestra la textura de 4 x 4 que asignará directamente a la cuádruple.</span><span class="sxs-lookup"><span data-stu-id="7798b-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![Ilustración de una textura 4x4](images/maptex-fig5.png)

<span data-ttu-id="7798b-134">Dado que la textura es 4 x 4 textura y la cuádruple es 4 x 4 píxeles, podría esperar que el cuádruple con textura aparezca exactamente igual que la textura, independientemente de la ubicación de la pantalla en la que se dibuje la cuádruple.</span><span class="sxs-lookup"><span data-stu-id="7798b-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="7798b-135">Sin embargo, este no es el caso; incluso los pequeños cambios en la posición afectan al modo en que se muestra la textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="7798b-136">En la ilustración siguiente se muestra cómo se muestra un cuádruple entre (0,0) y (4, 4) después de ser rasterizado y con textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![Ilustración de una cuádruple con textura dibujada desde (0,0) y (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="7798b-138">La línea cuádruple dibujada en la ilustración anterior muestra la salida con textura (con un modo de filtrado lineal y un modo de direccionamiento de abrazadera) con el contorno rasterizado superpuesto.</span><span class="sxs-lookup"><span data-stu-id="7798b-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="7798b-139">En el resto de este artículo se explica exactamente por qué el resultado tiene el aspecto que tiene en lugar de mirar la textura, pero para aquellos que quieren la solución, aquí es: los bordes de la entrada cuádruple deben estar en las líneas de límite entre las celdas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7798b-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="7798b-140">Con solo desplazar las coordenadas x e y en 0,5 unidades, las celdas de textura expondrán perfectamente las celdas de píxeles y la cuádruple se puede volver a crear perfectamente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7798b-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="7798b-141">(La última ilustración de este tema muestra la cuádruple en las coordenadas corregidas).</span><span class="sxs-lookup"><span data-stu-id="7798b-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="7798b-142">Los detalles de por qué la salida rasterizada solo tiene una ligera similitud con la textura de entrada se relacionan directamente con la forma en que Direct3D dirige y muestra las texturas.</span><span class="sxs-lookup"><span data-stu-id="7798b-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="7798b-143">Lo siguiente supone que tiene un buen conocimiento del [espacio de coordenadas de textura](texture-coordinates.md) y el [filtrado de textura bilineal](bilinear-texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="7798b-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="7798b-144">Al volver a nuestra investigación de la salida de píxeles extrañas, tiene sentido hacer un seguimiento del color de salida hasta el sombreador de píxeles: se llama al sombreador de píxeles por cada píxel seleccionado para formar parte de la forma rasterizada.</span><span class="sxs-lookup"><span data-stu-id="7798b-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="7798b-145">El cuádruple azul sólido representado en una ilustración anterior podría tener un sombreador especialmente sencillo:</span><span class="sxs-lookup"><span data-stu-id="7798b-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="7798b-146">En el caso del cuádruple con textura, el sombreador de píxeles debe cambiarse ligeramente:</span><span class="sxs-lookup"><span data-stu-id="7798b-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


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



<span data-ttu-id="7798b-147">Ese código supone que la textura 4 x 4 se almacena en la textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="7798b-148">Como se muestra, la muestra de texturas de el muestreador se establece para realizar un filtrado bilineal en la textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="7798b-149">El sombreador de píxeles se llama una vez para cada píxel rasterizado y cada vez que el color devuelto es el color de la textura muestreada en vTexCoord.</span><span class="sxs-lookup"><span data-stu-id="7798b-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="7798b-150">Cada vez que se llama al sombreador de píxeles, el argumento vTexCoord se establece en las coordenadas de textura en ese píxel.</span><span class="sxs-lookup"><span data-stu-id="7798b-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="7798b-151">Esto significa que el sombreador solicita el muestrario de texturas para el color de la textura filtrada en la ubicación exacta del píxel, tal como se detalla en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7798b-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![Ilustración de las ubicaciones de muestreo para las coordenadas de textura](images/maptex-fig7.png)

<span data-ttu-id="7798b-153">La textura (mostrada superpuesta) se muestrea directamente en ubicaciones de píxeles (se muestran como puntos negros).</span><span class="sxs-lookup"><span data-stu-id="7798b-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="7798b-154">Las coordenadas de textura no se ven afectadas por la rasterización (permanecen en el espacio de pantalla proyectado del cuádruple original).</span><span class="sxs-lookup"><span data-stu-id="7798b-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="7798b-155">Los puntos negros muestran dónde están los píxeles de rasterización.</span><span class="sxs-lookup"><span data-stu-id="7798b-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="7798b-156">Las coordenadas de textura en cada píxel se determinan fácilmente mediante la interpolación de las coordenadas almacenadas en cada vértice: el píxel en (0,0) coincide con el vértice en (0,0); por lo tanto, las coordenadas de textura en ese píxel son simplemente las coordenadas de textura almacenadas en ese vértice, UV (0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="7798b-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="7798b-157">Para el píxel en (3, 1), las coordenadas interpoladas son UV (0,75, 0,25) porque ese píxel se encuentra en tres cuartos del ancho de la textura y un cuarto de su alto.</span><span class="sxs-lookup"><span data-stu-id="7798b-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="7798b-158">Estas coordenadas interpoladas son las que se pasan al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7798b-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="7798b-159">Los textura no se alinean con los píxeles de este ejemplo; cada píxel (y, por tanto, cada punto de muestreo) se coloca en la esquina de cuatro textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="7798b-160">Dado que el modo de filtrado está establecido en lineal, la muestra calculará el promedio de los colores de los cuatro textura que comparten esa esquina.</span><span class="sxs-lookup"><span data-stu-id="7798b-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="7798b-161">Esto explica por qué el píxel que se espera que sea rojo es en realidad tres cuartos de color gris más un cuarto rojo, mientras que el píxel que se espera que sea verde es una mitad de gris y un cuarto de color rojo más uno-cuarto verde, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7798b-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="7798b-162">Para solucionar este problema, lo único que tiene que hacer es asignar correctamente el cuádruple a los píxeles en los que se rasterizará y, por tanto, asignar correctamente el textura a los píxeles.</span><span class="sxs-lookup"><span data-stu-id="7798b-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="7798b-163">En la ilustración siguiente se muestran los resultados del dibujo de la misma Quad entre (-0,5,-0,5) y (3,5, 3,5), que es el cuádruple previsto desde el principio.</span><span class="sxs-lookup"><span data-stu-id="7798b-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![Ilustración de una cuádruple con textura que coincide con el cuádruple rasterizado](images/maptex-fig8.png)

<span data-ttu-id="7798b-165">En la ilustración anterior se muestra que el cuádruple (mostrado de (-0,5,-0,5) a (3,5, 3,5)) coincide exactamente con el área rasterizada.</span><span class="sxs-lookup"><span data-stu-id="7798b-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="7798b-166">Resumen</span><span class="sxs-lookup"><span data-stu-id="7798b-166">Summary</span></span>

<span data-ttu-id="7798b-167">En Resumen, los píxeles y textura son realmente puntos, no bloques sólidos.</span><span class="sxs-lookup"><span data-stu-id="7798b-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="7798b-168">El espacio de la pantalla se origina en el píxel superior izquierdo, pero las coordenadas de textura se originan en la esquina superior izquierda de la cuadrícula de la textura.</span><span class="sxs-lookup"><span data-stu-id="7798b-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="7798b-169">Lo más importante es que no olvide restar 0,5 unidades de los componentes x e y de las posiciones de los vértices al trabajar en un espacio de pantalla transformado para alinear correctamente textura con píxeles.</span><span class="sxs-lookup"><span data-stu-id="7798b-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="7798b-170">El código siguiente es un ejemplo de desplazamiento de los vértices de un cuadrado 256 por 256 para mostrar correctamente una textura 256 by 256 en el espacio de pantalla transformado.</span><span class="sxs-lookup"><span data-stu-id="7798b-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7798b-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7798b-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7798b-172">Coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="7798b-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



