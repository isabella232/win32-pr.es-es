---
title: función glFeedbackBuffer (GL. h)
description: La función glFeedbackBuffer controla el modo de comentarios.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666033"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="3b129-104">glFeedbackBuffer función)</span><span class="sxs-lookup"><span data-stu-id="3b129-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="3b129-105">La función **glFeedbackBuffer** controla el modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b129-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b129-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="3b129-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b129-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b129-108">*size*</span><span class="sxs-lookup"><span data-stu-id="3b129-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="3b129-109">Número máximo de valores que se pueden escribir en el *búfer*.</span><span class="sxs-lookup"><span data-stu-id="3b129-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="3b129-110">*type*</span><span class="sxs-lookup"><span data-stu-id="3b129-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="3b129-111">Una constante simbólica que describe la información que se devolverá para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="3b129-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="3b129-112">Se aceptan las siguientes constantes simbólicas: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ color, GL \_ 3D \_ color \_ Texture y GL \_ 4D \_ color \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="3b129-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="3b129-113">*búfer*</span><span class="sxs-lookup"><span data-stu-id="3b129-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3b129-114">Devuelve los datos de los comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b129-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b129-115">Return value</span></span>

<span data-ttu-id="3b129-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3b129-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b129-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3b129-117">Error codes</span></span>

<span data-ttu-id="3b129-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="3b129-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3b129-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b129-119">Name</span></span>                                                                                                  | <span data-ttu-id="3b129-120">Significado</span><span class="sxs-lookup"><span data-stu-id="3b129-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b129-121"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3b129-122">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="3b129-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="3b129-123"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3b129-124">*el tamaño* era negativo.</span><span class="sxs-lookup"><span data-stu-id="3b129-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="3b129-125"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3b129-126">se llamó a **glFeedbackBuffer** mientras el modo de representación era comentarios de contabilidad \_ , o bien se llamó a [**glRenderMode**](glrendermode.md) con los comentarios de contabilidad de argumentos \_ antes de que se llamara a **glFeedbackBuffer** al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="3b129-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="3b129-127"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3b129-128">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3b129-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="3b129-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b129-129">Remarks</span></span>

<span data-ttu-id="3b129-130">La función **glFeedbackBuffer** controla los comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="3b129-131">Los comentarios, como la selección, son un modo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3b129-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="3b129-132">El modo se selecciona llamando a [**glRenderMode**](glrendermode.md) con comentarios de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="3b129-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="3b129-133">Cuando OpenGL está en modo de comentarios, no se genera ningún píxel mediante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="3b129-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="3b129-134">En su lugar, la información acerca de los primitivos que se habrían rasterizado se devolverá a la aplicación mediante OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3b129-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="3b129-135">La función **glFeedbackBuffer** tiene tres argumentos:</span><span class="sxs-lookup"><span data-stu-id="3b129-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="3b129-136">*buffer* es un puntero a una matriz de valores de punto flotante en el que se coloca información de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="3b129-137">*tamaño* indica el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3b129-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="3b129-138">*Type* es una constante simbólica que describe la información que se devuelve para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="3b129-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="3b129-139">Debe emitir **glFeedbackBuffer** antes de que se habilite el modo de comentarios (llamando a **glRenderMode** con los comentarios de contabilidad de argumentos \_ ).</span><span class="sxs-lookup"><span data-stu-id="3b129-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="3b129-140">La configuración \_ de comentarios de contabilidad sin establecer el búfer de comentarios, o la llamada a **GlFeedbackBuffer** mientras OpenGL está en modo de comentarios, es un error.</span><span class="sxs-lookup"><span data-stu-id="3b129-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="3b129-141">Saque el modo de comentarios de OpenGL mediante una llamada a [**glRenderMode**](glrendermode.md) con un valor de parámetro distinto de comentarios de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="3b129-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="3b129-142">Al hacerlo mientras OpenGL está en modo de comentarios, **glRenderMode** devuelve el número de entradas colocadas en la matriz de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="3b129-143">El valor devuelto nunca supera el *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="3b129-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="3b129-144">Si los datos de comentarios requirieron más espacio que el disponible en el *búfer*, **glRenderMode** devuelve un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="3b129-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="3b129-145">En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="3b129-146">Si esto haría que el número de entradas superara el máximo, **glFeedbackBuffer** escribe parcialmente el bloque para rellenar la matriz (si hay alguna habitación) y establece una marca de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="3b129-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="3b129-147">Cada bloque comienza con un código que indica el tipo primitivo, seguido de los valores que describen los vértices del primitivo y los datos asociados.</span><span class="sxs-lookup"><span data-stu-id="3b129-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="3b129-148">La función **glFeedbackBuffer** también escribe entradas para los mapas de bits y los rectángulos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="3b129-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="3b129-149">Los comentarios se producen después de la selección de polígono y la interpretación [**glPolygonMode**](glpolygonmode.md) de los polígonos ha tenido lugar, por lo que los polígonos que se seleccionan no se devuelven en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="3b129-150">También se puede producir después de que los polígonos con más de tres bordes se dividan en triángulos, si la implementación de OpenGL representa polígonos realizando esta descomposición.</span><span class="sxs-lookup"><span data-stu-id="3b129-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="3b129-151">Puede insertar un marcador en el búfer de comentarios con [**glPassThrough**](glpassthrough.md).</span><span class="sxs-lookup"><span data-stu-id="3b129-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="3b129-152">A continuación se encuentra la gramática de los bloques de valores escritos en el búfer de comentarios.</span><span class="sxs-lookup"><span data-stu-id="3b129-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="3b129-153">Cada primitiva se indica con un valor de identificación único seguido de un número de vértices.</span><span class="sxs-lookup"><span data-stu-id="3b129-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="3b129-154">Las entradas de polígono incluyen un valor entero que indica el número de vértices que siguen.</span><span class="sxs-lookup"><span data-stu-id="3b129-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="3b129-155">Un vértice se devolverá como cierto número de valores de punto flotante, según lo determinado por el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="3b129-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="3b129-156">Los colores se devuelven como cuatro valores en el modo RGBA y un valor en modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="3b129-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="3b129-157">feedbackList < feedbackItem feedbackList \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="3b129-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="3b129-158">mapa de bits de < feedbackItem punto de \| segmento de segmento \| \| \| pixelRectangle \| passThru</span><span class="sxs-lookup"><span data-stu-id="3b129-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="3b129-159">punto < vértice del token del \_ punto de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="3b129-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="3b129-160">lineSegment < token de línea de libro de la línea de \_ \_ \| libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b129-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="3b129-161">Polygon < token de polígono de GL \_ \_ n polispec</span><span class="sxs-lookup"><span data-stu-id="3b129-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="3b129-162">vértice de vértice de vértice del vértice de polispec < polispec \|</span><span class="sxs-lookup"><span data-stu-id="3b129-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="3b129-163">mapa de bits < vértice del token de mapa de bits de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b129-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="3b129-164">pixelRectangle < libro de píxeles del token de píxel de la \_ \_ \_ \| \_ copia GL \_ \_ del vértice del token de píxel</span><span class="sxs-lookup"><span data-stu-id="3b129-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="3b129-165">passThru < el valor del token de la contabilidad de \_ paso \_ a través \_</span><span class="sxs-lookup"><span data-stu-id="3b129-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="3b129-166">Vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="3b129-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="3b129-167">valor de < 2D</span><span class="sxs-lookup"><span data-stu-id="3b129-167">2d <  value value</span></span>

<span data-ttu-id="3b129-168">valor de valor de valor de < 3D</span><span class="sxs-lookup"><span data-stu-id="3b129-168">3d <  value value value</span></span>

<span data-ttu-id="3b129-169">color del valor de 3dColor < valor de valor</span><span class="sxs-lookup"><span data-stu-id="3b129-169">3dColor <  value value value color</span></span>

<span data-ttu-id="3b129-170">3dColorTexture < valor color valor Tex</span><span class="sxs-lookup"><span data-stu-id="3b129-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="3b129-171">4dColorTexture < valor Value valor color Tex</span><span class="sxs-lookup"><span data-stu-id="3b129-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="3b129-172">color < \| Índice RGBA</span><span class="sxs-lookup"><span data-stu-id="3b129-172">color <  rgba \| index</span></span>

<span data-ttu-id="3b129-173">RGBA < valor del valor del valor de valor</span><span class="sxs-lookup"><span data-stu-id="3b129-173">rgba <  value value value value</span></span>

<span data-ttu-id="3b129-174">valor de < de índice</span><span class="sxs-lookup"><span data-stu-id="3b129-174">index <  value</span></span>

<span data-ttu-id="3b129-175">Tex < valor del valor del valor del valor</span><span class="sxs-lookup"><span data-stu-id="3b129-175">tex <  value value value value</span></span>

<span data-ttu-id="3b129-176">El parámetro de *valor* es un número de punto flotante y *n* es un entero de punto flotante que indica el número de vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="3b129-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="3b129-177">Las siguientes son constantes de punto flotante simbólicas: token de punto de contabilidad general \_ \_ , token de línea de contabilidad \_ \_ , token de \_ restablecimiento de línea de libro de contabilidad \_ \_ , \_ \_ token de polígono de GL, token de mapa de bits de contabilidad, token de píxel de dibujo de GL, token de píxel de copia de contabilidad y token de \_ \_ \_ \_ \_ \_ \_ \_ paso de contab \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3b129-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="3b129-178">\_ \_ \_ El token de restablecimiento de línea de contabilidad se devuelve cuando se restablece el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="3b129-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="3b129-179">Los datos devueltos como vértice dependen del *tipo* de comentario.</span><span class="sxs-lookup"><span data-stu-id="3b129-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="3b129-180">En la tabla siguiente se proporciona la correspondencia entre el *tipo* y el número de valores por vértice; *k* es 1 en modo de índice de color y 4 en modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="3b129-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="3b129-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b129-181">Type</span></span>                   | <span data-ttu-id="3b129-182">Coordenadas</span><span class="sxs-lookup"><span data-stu-id="3b129-182">Coordinates</span></span>        | <span data-ttu-id="3b129-183">Color</span><span class="sxs-lookup"><span data-stu-id="3b129-183">Color</span></span> | <span data-ttu-id="3b129-184">Textura</span><span class="sxs-lookup"><span data-stu-id="3b129-184">Texture</span></span> | <span data-ttu-id="3b129-185">Número total de valores</span><span class="sxs-lookup"><span data-stu-id="3b129-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="3b129-186">GL en \_ 2D</span><span class="sxs-lookup"><span data-stu-id="3b129-186">GL\_2D</span></span>                 | <span data-ttu-id="3b129-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="3b129-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="3b129-188">2</span><span class="sxs-lookup"><span data-stu-id="3b129-188">2</span></span>                      |
| <span data-ttu-id="3b129-189">GL \_ 3D</span><span class="sxs-lookup"><span data-stu-id="3b129-189">GL\_3D</span></span>                 | <span data-ttu-id="3b129-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="3b129-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="3b129-191">3</span><span class="sxs-lookup"><span data-stu-id="3b129-191">3</span></span>                      |
| <span data-ttu-id="3b129-192">\_Color 3D de GL \_</span><span class="sxs-lookup"><span data-stu-id="3b129-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="3b129-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="3b129-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="3b129-194">*k*</span><span class="sxs-lookup"><span data-stu-id="3b129-194">*k*</span></span>   |         | <span data-ttu-id="3b129-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="3b129-195">3 + *k*</span></span>                |
| <span data-ttu-id="3b129-196">\_Textura de \_ color \_ 3D de GL</span><span class="sxs-lookup"><span data-stu-id="3b129-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="3b129-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="3b129-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="3b129-198">*k*</span><span class="sxs-lookup"><span data-stu-id="3b129-198">*k*</span></span>   | <span data-ttu-id="3b129-199">4</span><span class="sxs-lookup"><span data-stu-id="3b129-199">4</span></span>       | <span data-ttu-id="3b129-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="3b129-200">7 + *k*</span></span>                |
| <span data-ttu-id="3b129-201">\_Textura de \_ color \_ 4D de GL</span><span class="sxs-lookup"><span data-stu-id="3b129-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="3b129-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="3b129-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="3b129-203">*k*</span><span class="sxs-lookup"><span data-stu-id="3b129-203">*k*</span></span>   | <span data-ttu-id="3b129-204">4</span><span class="sxs-lookup"><span data-stu-id="3b129-204">4</span></span>       | <span data-ttu-id="3b129-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="3b129-205">8 + *k*</span></span>                |



 

<span data-ttu-id="3b129-206">Las coordenadas de los vértices de comentarios se encuentran en coordenadas de ventana, excepto *w*, que está en coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="3b129-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="3b129-207">Los colores de los comentarios se iluminan si la iluminación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="3b129-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="3b129-208">Se generan coordenadas de textura de comentarios si está habilitada la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3b129-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="3b129-209">Siempre se transforman mediante la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="3b129-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="3b129-210">La función **glFeedbackBuffer** , cuando se usa en una lista de visualización, no se compila en la lista de visualización, sino que se ejecuta inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3b129-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="3b129-211">La siguiente función recupera información relacionada con **glFeedbackBuffer**:</span><span class="sxs-lookup"><span data-stu-id="3b129-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="3b129-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="3b129-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="3b129-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b129-213">Requirements</span></span>



| <span data-ttu-id="3b129-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b129-214">Requirement</span></span> | <span data-ttu-id="3b129-215">Value</span><span class="sxs-lookup"><span data-stu-id="3b129-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b129-216">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b129-216">Minimum supported client</span></span><br/> | <span data-ttu-id="3b129-217">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b129-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3b129-218">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b129-218">Minimum supported server</span></span><br/> | <span data-ttu-id="3b129-219">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b129-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b129-220">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b129-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b129-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3b129-222">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b129-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b129-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b129-224">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b129-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b129-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b129-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b129-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b129-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b129-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3b129-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3b129-228">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3b129-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3b129-229">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3b129-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3b129-230">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="3b129-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="3b129-231">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="3b129-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="3b129-232">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="3b129-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="3b129-233">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="3b129-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="3b129-234">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="3b129-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





