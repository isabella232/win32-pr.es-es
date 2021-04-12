---
title: Comandos de cueing y niebla de profundidad de portabilidad
description: Comandos de cueing y niebla de profundidad de portabilidad
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Migración de la contabilidad de IRIS, profundidad cueing
- portabilidad de IRIS GL, Depth cueing
- trasladar a OpenGL desde IRIS GL, Depth cueing
- Exportación de OpenGL desde IRIS GL, profundidad cueing
- Migración de la contabilidad de IRIS, niebla
- portabilidad de IRIS GL, niebla
- trasladar a OpenGL desde IRIS GL, niebla
- Exportación de OpenGL desde IRIS GL, niebla
- profundidad cueing
- luz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269169"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="4df36-113">Comandos de cueing y niebla de profundidad de portabilidad</span><span class="sxs-lookup"><span data-stu-id="4df36-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="4df36-114">Al migrar los comandos Depth-cueing y niebla, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4df36-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="4df36-115">La llamada de GL de IRIS, **fogvertex**, establece un modo y los parámetros que afectan a ese modo.</span><span class="sxs-lookup"><span data-stu-id="4df36-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="4df36-116">En OpenGL, se llama una vez a [**glFog**](glfog.md) para establecer el modo y, a continuación, de nuevo dos veces o más para establecer varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="4df36-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="4df36-117">En OpenGL, Depth cueing no es una característica independiente.</span><span class="sxs-lookup"><span data-stu-id="4df36-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="4df36-118">Usar niebla lineal en lugar de cueing de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4df36-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="4df36-119">(En esta sección se proporciona un ejemplo de cómo hacerlo). Las siguientes funciones de la contabilidad de IRIS no tienen un equivalente de OpenGL directo:</span><span class="sxs-lookup"><span data-stu-id="4df36-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="4df36-120">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="4df36-120">**depthcue**</span></span>

    <span data-ttu-id="4df36-121">**lRGBrange**</span><span class="sxs-lookup"><span data-stu-id="4df36-121">**lRGBrange**</span></span>

    <span data-ttu-id="4df36-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="4df36-122">**lshaderange**</span></span>

    <span data-ttu-id="4df36-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="4df36-123">**getdcm**</span></span>

-   <span data-ttu-id="4df36-124">Para ajustar la calidad de la niebla, use [**glHint**](glhint.md)(sugerencia de niebla de GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="4df36-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="4df36-125">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para administrar la niebla y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4df36-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4df36-126">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="4df36-126">IRIS GL function</span></span>         | <span data-ttu-id="4df36-127">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="4df36-127">OpenGL function</span></span>                                     | <span data-ttu-id="4df36-128">Significado</span><span class="sxs-lookup"><span data-stu-id="4df36-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="4df36-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="4df36-129">**fogvertex**</span></span>            | [<span data-ttu-id="4df36-130">**glFog**</span><span class="sxs-lookup"><span data-stu-id="4df36-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="4df36-131">Establece varios parámetros de niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="4df36-132">**fogvertex**(FG \_ en)</span><span class="sxs-lookup"><span data-stu-id="4df36-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="4df36-133">[**glEnable**](glenable.md) (niebla de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="4df36-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="4df36-134">Activa la niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="4df36-135">**fogvertex**(FG \_ desactivado)</span><span class="sxs-lookup"><span data-stu-id="4df36-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="4df36-136">[**glDisable**](gldisable.md) (niebla de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="4df36-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="4df36-137">Desactiva la niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="4df36-138">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="4df36-138">**depthcue**</span></span>             | <span data-ttu-id="4df36-139">[**glFog**](glfog.md) ( \_ \_ módulo de niebla de contabilidad general, GL \_ lineal)</span><span class="sxs-lookup"><span data-stu-id="4df36-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="4df36-140">Utiliza la niebla lineal para cueing de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4df36-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="4df36-141">En la tabla siguiente se enumeran los parámetros que se pueden pasar a **glFog**.</span><span class="sxs-lookup"><span data-stu-id="4df36-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="4df36-142">Parámetro de niebla</span><span class="sxs-lookup"><span data-stu-id="4df36-142">Fog parameter</span></span>    | <span data-ttu-id="4df36-143">Significado</span><span class="sxs-lookup"><span data-stu-id="4df36-143">Meaning</span></span>                       | <span data-ttu-id="4df36-144">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4df36-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="4df36-145">\_densidad de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="4df36-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="4df36-146">Densidad de niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-146">Fog density.</span></span>                  | <span data-ttu-id="4df36-147">1,0</span><span class="sxs-lookup"><span data-stu-id="4df36-147">1.0</span></span>                      |
| <span data-ttu-id="4df36-148">\_Inicio de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="4df36-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="4df36-149">Cerca de distancia para la niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="4df36-149">Near distance for linear fog.</span></span> | <span data-ttu-id="4df36-150">0,0</span><span class="sxs-lookup"><span data-stu-id="4df36-150">0.0</span></span>                      |
| <span data-ttu-id="4df36-151">finalización de la niebla de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4df36-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="4df36-152">Distancia lejana para la niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="4df36-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="4df36-153">1,0</span><span class="sxs-lookup"><span data-stu-id="4df36-153">1.0</span></span>                      |
| <span data-ttu-id="4df36-154">\_Índice de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="4df36-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="4df36-155">Índice de color de niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-155">Fog color index.</span></span>              | <span data-ttu-id="4df36-156">0,0</span><span class="sxs-lookup"><span data-stu-id="4df36-156">0.0</span></span>                      |
| <span data-ttu-id="4df36-157">\_color de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="4df36-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="4df36-158">Color RGBA de niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-158">Fog RGBA color.</span></span>               | <span data-ttu-id="4df36-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="4df36-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="4df36-160">\_modo de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="4df36-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="4df36-161">Modo de niebla.</span><span class="sxs-lookup"><span data-stu-id="4df36-161">Fog mode.</span></span>                     | <span data-ttu-id="4df36-162">Consulte la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4df36-162">See the following table.</span></span> |



 

<span data-ttu-id="4df36-163">El parámetro niebla-density de OpenGL difiere del de IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="4df36-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="4df36-164">Se relacionan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4df36-164">They are related as follows:</span></span>

-   <span data-ttu-id="4df36-165">Si *fogMode* = EXP2</span><span class="sxs-lookup"><span data-stu-id="4df36-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="4df36-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="4df36-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="4df36-167">Si *fogMode* = exp</span><span class="sxs-lookup"><span data-stu-id="4df36-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="4df36-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))</span><span class="sxs-lookup"><span data-stu-id="4df36-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="4df36-169">donde **sqrt** es la operación de raíz cuadrada, **log** es el logaritmo natural, *irisGLfogDensity* es la densidad de niebla de la contabilidad de iris y *OpenGLfogDensity* es la densidad de niebla de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4df36-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="4df36-170">Para cambiar entre el cálculo de la niebla en modo por píxel y el modo por vértice, use [**glHint**](glhint.md)( \_ sugerencia de niebla de GL \_ , *hintMode*).</span><span class="sxs-lookup"><span data-stu-id="4df36-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="4df36-171">Hay dos modos de sugerencia disponibles:</span><span class="sxs-lookup"><span data-stu-id="4df36-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="4df36-172">\_Cálculo de niebla por píxel más bonito</span><span class="sxs-lookup"><span data-stu-id="4df36-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="4df36-173">\_Cálculo de niebla por vértice más rápido de GL</span><span class="sxs-lookup"><span data-stu-id="4df36-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="4df36-174">En la tabla siguiente se enumeran los modos de niebla de la contabilidad de IRIS y sus equivalentes de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4df36-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="4df36-175">Modo de niebla de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="4df36-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="4df36-176">Modo de niebla de OpenGL</span><span class="sxs-lookup"><span data-stu-id="4df36-176">OpenGL fog mode</span></span> | <span data-ttu-id="4df36-177">Modo de sugerencia</span><span class="sxs-lookup"><span data-stu-id="4df36-177">Hint mode</span></span>                         | <span data-ttu-id="4df36-178">Significado</span><span class="sxs-lookup"><span data-stu-id="4df36-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="4df36-179">FG \_ VTX \_ exp, FG \_ PIX \_ exp</span><span class="sxs-lookup"><span data-stu-id="4df36-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="4df36-180">contabilidad \_ General</span><span class="sxs-lookup"><span data-stu-id="4df36-180">GL\_EXP</span></span>         | <span data-ttu-id="4df36-181">GL \_ más rápido, libro de contabilidad más \_ agradable</span><span class="sxs-lookup"><span data-stu-id="4df36-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="4df36-182">Modo de niebla pesada (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4df36-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="4df36-183">FG \_ VTX \_ EXP2, FG \_ PIX \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="4df36-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="4df36-184">GL \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="4df36-184">GL\_EXP2</span></span>        | <span data-ttu-id="4df36-185">GL \_ más rápido, libro de contabilidad más \_ agradable</span><span class="sxs-lookup"><span data-stu-id="4df36-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="4df36-186">Modo Haze.</span><span class="sxs-lookup"><span data-stu-id="4df36-186">Haze mode.</span></span>                               |
| <span data-ttu-id="4df36-187">FG \_ VTX- \_ foto, FG \_ PIX \_</span><span class="sxs-lookup"><span data-stu-id="4df36-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="4df36-188">CONTABILIDAD \_ lineal</span><span class="sxs-lookup"><span data-stu-id="4df36-188">GL\_LINEAR</span></span>      | <span data-ttu-id="4df36-189">GL \_ más rápido, libro de contabilidad más \_ agradable</span><span class="sxs-lookup"><span data-stu-id="4df36-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="4df36-190">Modo de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="4df36-190">Linear fog mode.</span></span> <span data-ttu-id="4df36-191">(Se usa para cueing de profundidad).</span><span class="sxs-lookup"><span data-stu-id="4df36-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="4df36-192">En el ejemplo de código siguiente se muestra la profundidad cueing en OpenGL:</span><span class="sxs-lookup"><span data-stu-id="4df36-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





