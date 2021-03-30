---
title: función glPushAttrib (GL. h)
description: Envía la pila de atributos.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079055"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="809f7-104">glPushAttrib función)</span><span class="sxs-lookup"><span data-stu-id="809f7-104">glPushAttrib function</span></span>

<span data-ttu-id="809f7-105">Envía la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="809f7-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="809f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="809f7-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="809f7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="809f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="809f7-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="809f7-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="809f7-109">Máscara que indica los atributos que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="809f7-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="809f7-110">Las constantes de máscara simbólica y su estado de OpenGL asociado son las siguientes (la lista de párrafos con sangría que se guardan):</span><span class="sxs-lookup"><span data-stu-id="809f7-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="809f7-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit de \_ búfer de acumulación de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="809f7-112">Valor de eliminación de búfer de acumulación</span><span class="sxs-lookup"><span data-stu-id="809f7-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="809f7-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit de \_ búfer de color de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-114">\_Bit de \_ habilitación de pruebas alfa de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="809f7-115">Función de prueba alfa y valor de referencia</span><span class="sxs-lookup"><span data-stu-id="809f7-115">Alpha test function and reference value</span></span>

<span data-ttu-id="809f7-116">\_Bit de habilitación de GL Blend</span><span class="sxs-lookup"><span data-stu-id="809f7-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="809f7-117">Combinar funciones de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="809f7-117">Blending source and destination functions</span></span>

<span data-ttu-id="809f7-118">\_Bit de habilitación de trama de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="809f7-119">Configuración de búfer de \_ dibujo de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="809f7-120">\_Bit de habilitación de la lógica de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="809f7-121">Logic OP (función)</span><span class="sxs-lookup"><span data-stu-id="809f7-121">Logic op function</span></span>

<span data-ttu-id="809f7-122">Valores claros en modo de color e índice</span><span class="sxs-lookup"><span data-stu-id="809f7-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="809f7-123">Modo de color y writemasks de modo de índice</span><span class="sxs-lookup"><span data-stu-id="809f7-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="809f7-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bits actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-125">Color RGBA actual</span><span class="sxs-lookup"><span data-stu-id="809f7-125">Current RGBA color</span></span>

<span data-ttu-id="809f7-126">Índice de color actual</span><span class="sxs-lookup"><span data-stu-id="809f7-126">Current color index</span></span>

<span data-ttu-id="809f7-127">Vector normal actual</span><span class="sxs-lookup"><span data-stu-id="809f7-127">Current normal vector</span></span>

<span data-ttu-id="809f7-128">Coordenadas de textura actuales</span><span class="sxs-lookup"><span data-stu-id="809f7-128">Current texture coordinates</span></span>

<span data-ttu-id="809f7-129">Posición de la trama actual \_ de contab \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="809f7-130">Color RGBA asociado a la posición de la trama actual</span><span class="sxs-lookup"><span data-stu-id="809f7-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="809f7-131">Índice de color asociado a la posición de la trama actual</span><span class="sxs-lookup"><span data-stu-id="809f7-131">Color index associated with current raster position</span></span>

<span data-ttu-id="809f7-132">Coordenadas de textura asociadas a la posición de la trama actual</span><span class="sxs-lookup"><span data-stu-id="809f7-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="809f7-133">Marca de marca de \_ borde de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="809f7-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ búfer de profundidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-135">\_Bit de \_ habilitación de prueba de profundidad de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="809f7-136">Función de prueba de búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="809f7-136">Depth buffer test function</span></span>

<span data-ttu-id="809f7-137">Valor de borrar del búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="809f7-137">Depth buffer clear value</span></span>

<span data-ttu-id="809f7-138">\_Bit de \_ habilitación de WRITEMASK de profundidad de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="809f7-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit de habilitación de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-140">Marca de prueba de GL \_ alfa \_</span><span class="sxs-lookup"><span data-stu-id="809f7-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="809f7-141">\_Marca de \_ normalización automática de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="809f7-142">\_Marca GL Blend</span><span class="sxs-lookup"><span data-stu-id="809f7-142">GL\_BLEND flag</span></span>

<span data-ttu-id="809f7-143">Habilitar bits para los planos de recorte definibles por el usuario</span><span class="sxs-lookup"><span data-stu-id="809f7-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="809f7-144">\_material de color GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="809f7-145">Marca de cara de \_ selección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="809f7-146">Marca de prueba de \_ profundidad de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="809f7-147">\_Marca de interpolación de contabilidad</span><span class="sxs-lookup"><span data-stu-id="809f7-147">GL\_DITHER flag</span></span>

<span data-ttu-id="809f7-148">Marca de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-148">GL\_FOG flag</span></span>

<span data-ttu-id="809f7-149">GL \_ Light *i* , donde 0 <= *i* < \_ \_ Lights Max GL</span><span class="sxs-lookup"><span data-stu-id="809f7-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="809f7-150">Marca de iluminación de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="809f7-151">\_Marca de suavizado de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-152">\_Marca punteada de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="809f7-153">\_Marca de \_ operación de lógica de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="809f7-154">\_Marca de \_ OP de lógica de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="809f7-155">GL \_ MAP1 \_ x, donde x es un tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="809f7-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="809f7-156">GL \_ MAP2 ( \_ x, donde x es un tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="809f7-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="809f7-157">\_Marca de normalización de contabilidad</span><span class="sxs-lookup"><span data-stu-id="809f7-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="809f7-158">\_Marca de suavizado de punto de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-159">\_Marca de \_ línea de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="809f7-160">\_Marca de \_ relleno de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="809f7-161">\_Marca de \_ punto de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="809f7-162">\_Marca de Polígono suave de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-163">\_ \_ Marca punteada de GL poligonal</span><span class="sxs-lookup"><span data-stu-id="809f7-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="809f7-164">Marca de prueba de \_ tijera de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="809f7-165">Marca de prueba de \_ estarcido de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="809f7-166">\_Marca de textura 1D de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="809f7-167">\_Marca 2D de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="809f7-168">Marcas GL \_ Texture \_ \_ x, donde x es S, T, R o Q</span><span class="sxs-lookup"><span data-stu-id="809f7-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="809f7-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit de evaluación de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-170">GL \_ MAP1 \_ x habilitar bits, donde x es un tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="809f7-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="809f7-171">GL \_ MAP2 ( \_ x habilitar bits, donde x es un tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="809f7-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="809f7-172">puntos de conexión y divisiones de la cuadrícula 1D</span><span class="sxs-lookup"><span data-stu-id="809f7-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="809f7-173">puntos de conexión y divisiones de la cuadrícula 2D</span><span class="sxs-lookup"><span data-stu-id="809f7-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="809f7-174">\_Bit de \_ habilitación de normalización automática de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="809f7-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-176">\_Marca de habilitación de niebla de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="809f7-177">Color de niebla</span><span class="sxs-lookup"><span data-stu-id="809f7-177">Fog color</span></span>

<span data-ttu-id="809f7-178">Densidad de niebla</span><span class="sxs-lookup"><span data-stu-id="809f7-178">Fog density</span></span>

<span data-ttu-id="809f7-179">Inicio de niebla lineal</span><span class="sxs-lookup"><span data-stu-id="809f7-179">Linear fog start</span></span>

<span data-ttu-id="809f7-180">Finalización de la niebla lineal</span><span class="sxs-lookup"><span data-stu-id="809f7-180">Linear fog end</span></span>

<span data-ttu-id="809f7-181">Índice de niebla</span><span class="sxs-lookup"><span data-stu-id="809f7-181">Fog index</span></span>

<span data-ttu-id="809f7-182">Valor del modo de \_ niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="809f7-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit de sugerencia de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-184">\_Configuración de \_ sugerencia de corrección de perspectiva de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="809f7-185">\_Valor de \_ sugerencia de suavizado de punto de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="809f7-186">\_Valor de \_ sugerencia de suavizado de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="809f7-187">\_Valor de \_ sugerencia de suavizado de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="809f7-188">Configuración de la sugerencia de niebla de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="809f7-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit de iluminación de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-190">\_Bit de \_ habilitación del material de color GL</span><span class="sxs-lookup"><span data-stu-id="809f7-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="809f7-191">\_Valor de \_ superficie de material de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="809f7-192">Parámetros de material de color que están realizando el seguimiento del color actual</span><span class="sxs-lookup"><span data-stu-id="809f7-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="809f7-193">Color de la escena ambiente</span><span class="sxs-lookup"><span data-stu-id="809f7-193">Ambient scene color</span></span>

<span data-ttu-id="809f7-194">\_Valor del \_ \_ visor local del modelo de contabilidad solar \_</span><span class="sxs-lookup"><span data-stu-id="809f7-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="809f7-195">\_Configuración de \_ \_ dos \_ lados del modelo de contabilidad solar</span><span class="sxs-lookup"><span data-stu-id="809f7-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="809f7-196">\_Bit de habilitación de iluminación de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="809f7-197">Habilitar bit para cada luz</span><span class="sxs-lookup"><span data-stu-id="809f7-197">Enable bit for each light</span></span>

<span data-ttu-id="809f7-198">Intensidad de ambiente, difuso y especular para cada luz</span><span class="sxs-lookup"><span data-stu-id="809f7-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="809f7-199">Dirección, posición, exponente y ángulo límite para cada luz</span><span class="sxs-lookup"><span data-stu-id="809f7-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="809f7-200">Factores de atenuación constante, lineal y cuadrático para cada luz</span><span class="sxs-lookup"><span data-stu-id="809f7-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="809f7-201">Color ambiente, difuso, especular y emisor para cada material</span><span class="sxs-lookup"><span data-stu-id="809f7-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="809f7-202">Índices de color ambiente, difuso y especular para cada material</span><span class="sxs-lookup"><span data-stu-id="809f7-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="809f7-203">Exponente especular para cada \_ configuración de modelo de sombreado de contabilidad de materiales \_</span><span class="sxs-lookup"><span data-stu-id="809f7-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="809f7-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="809f7-205">\_Marca de suavizado de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-206">\_Bit de habilitación de línea de contabilidad \_ punteada</span><span class="sxs-lookup"><span data-stu-id="809f7-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="809f7-207">Patrón punteado de línea y contador de repetición</span><span class="sxs-lookup"><span data-stu-id="809f7-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="809f7-208">Ancho de línea</span><span class="sxs-lookup"><span data-stu-id="809f7-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="809f7-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit de lista de contab. \_</span><span class="sxs-lookup"><span data-stu-id="809f7-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-210">Configuración de base de \_ lista de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="809f7-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit de \_ modo de píxel de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-212">\_ \_ Configuración de sesgo rojo de GL y escala de rojo de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="809f7-213">\_ \_ Valores de escala verde de GL y escala de verde de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="809f7-214">\_Tendencia azul \_ de GL y \_ escala azul de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="809f7-215">\_Tendencia alfa \_ de contabilidad general \_ y \_ escala de alfa</span><span class="sxs-lookup"><span data-stu-id="809f7-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="809f7-216">\_ \_ Tendencia de profundidad de GL y \_ escala de profundidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="809f7-217">\_ \_ Valores de desplazamiento de índice de GL y cambio de índice de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="809f7-218">\_ \_ \_ Marcas de estarcido de mapa de contabilidad y contab. \_</span><span class="sxs-lookup"><span data-stu-id="809f7-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="809f7-219">\_Zoom \_ de GL X y contabilidad \_ \_ y factores de zoom de GL</span><span class="sxs-lookup"><span data-stu-id="809f7-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="809f7-220">Configuración de búfer de \_ lectura de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="809f7-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de punta de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-222">\_Marca de suavizado de punto de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-223">Tamaño del punto</span><span class="sxs-lookup"><span data-stu-id="809f7-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="809f7-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-225">\_Bit de \_ habilitación de la cara de selección de contabilidad</span><span class="sxs-lookup"><span data-stu-id="809f7-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="809f7-226">\_Valor del \_ modo de cara de selección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="809f7-227">\_Indicador de cara frontal de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="809f7-228">\_Configuración de modo polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="809f7-229">\_Marca de Polígono suave de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="809f7-230">\_Bit de habilitación de los polígonos de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="809f7-231">\_Marca de \_ relleno de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="809f7-232">\_Marca de \_ línea de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="809f7-233">\_Marca de \_ punto de desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="809f7-234">\_factor de \_ desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="809f7-235">\_unidades de \_ desplazamiento de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="809f7-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_bit de \_ punteado de los polígonos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-237">Imagen de punteado de polígono</span><span class="sxs-lookup"><span data-stu-id="809f7-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="809f7-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit de tijera de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-239">Marca de prueba de \_ tijera de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="809f7-240">Cuadro de tijeras</span><span class="sxs-lookup"><span data-stu-id="809f7-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="809f7-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ búfer de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-242">\_Habilitar bits de la prueba de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="809f7-243">Función de estarcido y valor de referencia</span><span class="sxs-lookup"><span data-stu-id="809f7-243">Stencil function and reference value</span></span>

<span data-ttu-id="809f7-244">Máscara de valor de estarcido</span><span class="sxs-lookup"><span data-stu-id="809f7-244">Stencil value mask</span></span>

<span data-ttu-id="809f7-245">Acciones de paso de búfer de error, de paso y de profundidad de la galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="809f7-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="809f7-246">Valor sin formato del búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="809f7-246">Stencil buffer clear value</span></span>

<span data-ttu-id="809f7-247">Búfer de estarcido writemask</span><span class="sxs-lookup"><span data-stu-id="809f7-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="809f7-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-249">Habilitar bits para las cuatro coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="809f7-250">Color de borde de cada imagen de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-250">Border color for each texture image</span></span>

<span data-ttu-id="809f7-251">Función minificación para cada imagen de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-251">Minification function for each texture image</span></span>

<span data-ttu-id="809f7-252">Función de ampliación para cada imagen de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-252">Magnification function for each texture image</span></span>

<span data-ttu-id="809f7-253">Coordenadas de textura y el modo de ajuste para cada imagen de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="809f7-254">Color y modo para cada entorno de textura</span><span class="sxs-lookup"><span data-stu-id="809f7-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="809f7-255">Habilitar la textura GL de bits \_ \_ gen \_ *x*; *x* es S, T, R y Q</span><span class="sxs-lookup"><span data-stu-id="809f7-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="809f7-256">\_ \_ \_ Configuración del modo de generación de texturas GL para S, T, R y Q</span><span class="sxs-lookup"><span data-stu-id="809f7-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="809f7-257">ecuaciones de plano glTexGen para S, T, R y Q</span><span class="sxs-lookup"><span data-stu-id="809f7-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="809f7-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformación de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-259">Coeficientes de los seis planos de recorte</span><span class="sxs-lookup"><span data-stu-id="809f7-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="809f7-260">Habilitar bits para los planos de recorte definibles por el usuario</span><span class="sxs-lookup"><span data-stu-id="809f7-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="809f7-261">Valor del modo de \_ matriz de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="809f7-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="809f7-262">\_Marca de normalización de contabilidad</span><span class="sxs-lookup"><span data-stu-id="809f7-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="809f7-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit de ventanilla de GL \_</span><span class="sxs-lookup"><span data-stu-id="809f7-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="809f7-264">Rango de profundidad (Near y Far)</span><span class="sxs-lookup"><span data-stu-id="809f7-264">Depth range (near and far)</span></span>

<span data-ttu-id="809f7-265">Origen y extensión de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="809f7-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="809f7-266">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="809f7-266">Return value</span></span>

<span data-ttu-id="809f7-267">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="809f7-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="809f7-268">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="809f7-268">Error codes</span></span>

<span data-ttu-id="809f7-269">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="809f7-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="809f7-270">Nombre</span><span class="sxs-lookup"><span data-stu-id="809f7-270">Name</span></span>                                                                                                  | <span data-ttu-id="809f7-271">Significado</span><span class="sxs-lookup"><span data-stu-id="809f7-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="809f7-272"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="809f7-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="809f7-273">Se llamó a la función mientras la pila de atributos estaba llena.</span><span class="sxs-lookup"><span data-stu-id="809f7-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="809f7-274"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="809f7-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="809f7-275">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="809f7-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="809f7-276">Observaciones</span><span class="sxs-lookup"><span data-stu-id="809f7-276">Remarks</span></span>

<span data-ttu-id="809f7-277">La función **glPushAttrib** toma un argumento, una máscara que indica los grupos de variables de estado que se van a guardar en la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="809f7-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="809f7-278">Las constantes simbólicas se utilizan para establecer bits en la máscara.</span><span class="sxs-lookup"><span data-stu-id="809f7-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="809f7-279">El parámetro Mask se construye normalmente aplicando la operación **or** lógica a varias de estas constantes.</span><span class="sxs-lookup"><span data-stu-id="809f7-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="809f7-280">Puede usar la máscara especial GL \_ All \_ attrib \_ bits para guardar todos los Estados apilables.</span><span class="sxs-lookup"><span data-stu-id="809f7-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="809f7-281">La función [**glPopAttrib**](glpopattrib.md) restaura los valores de las variables de estado guardadas con el último comando **glPushAttrib** .</span><span class="sxs-lookup"><span data-stu-id="809f7-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="809f7-282">Los que no se han guardado permanecen inalterados.</span><span class="sxs-lookup"><span data-stu-id="809f7-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="809f7-283">Es un error insertar atributos en una pila completa o desactivar los atributos de una pila vacía.</span><span class="sxs-lookup"><span data-stu-id="809f7-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="809f7-284">En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="809f7-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="809f7-285">Inicialmente, la pila de atributos está vacía.</span><span class="sxs-lookup"><span data-stu-id="809f7-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="809f7-286">No todos los valores del estado de OpenGL se pueden guardar en la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="809f7-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="809f7-287">Por ejemplo, no puede guardar el paquete de píxeles y desempaquetar, el estado del modo de representación y el estado de selección y de comentarios.</span><span class="sxs-lookup"><span data-stu-id="809f7-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="809f7-288">La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.</span><span class="sxs-lookup"><span data-stu-id="809f7-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="809f7-289">Las siguientes funciones recuperan información relacionada con **glPushAttrib** y [**glPopAttrib**](glpopattrib.md):</span><span class="sxs-lookup"><span data-stu-id="809f7-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="809f7-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ pila de atrib \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="809f7-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ profundidad máxima de la pila de Max \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="809f7-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="809f7-292">Requisitos</span><span class="sxs-lookup"><span data-stu-id="809f7-292">Requirements</span></span>



| <span data-ttu-id="809f7-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="809f7-293">Requirement</span></span> | <span data-ttu-id="809f7-294">Value</span><span class="sxs-lookup"><span data-stu-id="809f7-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="809f7-295">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="809f7-295">Minimum supported client</span></span><br/> | <span data-ttu-id="809f7-296">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="809f7-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="809f7-297">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="809f7-297">Minimum supported server</span></span><br/> | <span data-ttu-id="809f7-298">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="809f7-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="809f7-299">Encabezado</span><span class="sxs-lookup"><span data-stu-id="809f7-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="809f7-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="809f7-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="809f7-301">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="809f7-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="809f7-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="809f7-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="809f7-303">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="809f7-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="809f7-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="809f7-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809f7-305">Vea también</span><span class="sxs-lookup"><span data-stu-id="809f7-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809f7-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="809f7-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="809f7-307">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="809f7-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="809f7-308">**glGet**</span><span class="sxs-lookup"><span data-stu-id="809f7-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="809f7-309">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="809f7-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="809f7-310">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="809f7-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="809f7-311">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="809f7-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="809f7-312">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="809f7-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="809f7-313">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="809f7-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="809f7-314">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="809f7-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="809f7-315">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="809f7-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="809f7-316">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="809f7-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="809f7-317">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="809f7-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="809f7-318">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="809f7-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="809f7-319">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="809f7-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="809f7-320">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="809f7-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="809f7-321">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="809f7-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="809f7-322">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="809f7-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





