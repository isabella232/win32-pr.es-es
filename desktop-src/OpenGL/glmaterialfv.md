---
title: función glMaterialfv (GL. h)
description: La función glMaterialfv especifica los parámetros de material para el modelo de iluminación.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- glMaterialfv (función) OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421905"
---
# <a name="glmaterialfv-function"></a><span data-ttu-id="eccf0-104">glMaterialfv función)</span><span class="sxs-lookup"><span data-stu-id="eccf0-104">glMaterialfv function</span></span>

<span data-ttu-id="eccf0-105">La función **glMaterialfv** especifica los parámetros de material para el modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eccf0-105">The **glMaterialfv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccf0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eccf0-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="eccf0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eccf0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eccf0-108">*Portada*</span><span class="sxs-lookup"><span data-stu-id="eccf0-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="eccf0-109">La cara o caras que se están actualizando.</span><span class="sxs-lookup"><span data-stu-id="eccf0-109">The face or faces that are being updated.</span></span> <span data-ttu-id="eccf0-110">Debe ser uno de los siguientes: GL \_ Front, GL \_ back o GL \_ Front y GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="eccf0-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="eccf0-111">*PName*</span><span class="sxs-lookup"><span data-stu-id="eccf0-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="eccf0-112">Parámetro de material de la cara o caras que se están actualizando.</span><span class="sxs-lookup"><span data-stu-id="eccf0-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="eccf0-113">Los parámetros que se pueden especificar mediante **glMaterialfv** y sus interpretaciones por la ecuación de iluminación son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="eccf0-113">The parameters that can be specified using **glMaterialfv**, and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="eccf0-114">Value</span><span class="sxs-lookup"><span data-stu-id="eccf0-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="eccf0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="eccf0-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="eccf0-116"><dt>**ambiente de contabilidad general \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="eccf0-117">El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia RGBA ambiental del material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-117">The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="eccf0-118">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="eccf0-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="eccf0-119">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="eccf0-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="eccf0-120">Ninguno de los valores enteros ni de punto flotante está fijado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="eccf0-121">La reflexión ambiente predeterminada para los materiales de orientación frontal y hacia delante es (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="eccf0-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="eccf0-122"><dt>**difusión en contab. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="eccf0-123">El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia RGBA difusa del material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-123">The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="eccf0-124">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="eccf0-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="eccf0-125">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="eccf0-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="eccf0-126">Ninguno de los valores enteros ni de punto flotante está fijado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="eccf0-127">La reflexión difusa predeterminada para los materiales de orientación frontal y hacia delante es (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="eccf0-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="eccf0-128"><dt>**\_especular GL**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="eccf0-129">El parámetro params contiene cuatro valores de punto flotante que especifican la reflectancia de RGBA especular del material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-129">The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="eccf0-130">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="eccf0-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="eccf0-131">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="eccf0-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="eccf0-132">Ninguno de los valores enteros ni de punto flotante está fijado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="eccf0-133">La reflexión especular predeterminada para los materiales de orientación frontal y hacia delante es (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="eccf0-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="eccf0-134"><dt>**emisión de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="eccf0-135">El parámetro params contiene cuatro valores de punto flotante que especifican la intensidad clara emitida del RGBA del material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-135">The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="eccf0-136">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="eccf0-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="eccf0-137">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="eccf0-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="eccf0-138">Ninguno de los valores enteros ni de punto flotante está fijado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="eccf0-139">La intensidad de emisión predeterminada de los materiales orientados delante y hacia delante es (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="eccf0-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="eccf0-140"><dt>**brillo de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="eccf0-141">El parámetro *param* es un valor entero único que especifica el exponente especular RGBA del material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-141">The *param* parameter is a single integer value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="eccf0-142">Los valores enteros se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="eccf0-142">Integer values are mapped directly.</span></span> <span data-ttu-id="eccf0-143">Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] .</span><span class="sxs-lookup"><span data-stu-id="eccf0-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="eccf0-144">El exponente especular predeterminado para el material orientado hacia delante y hacia atrás es 0.</span><span class="sxs-lookup"><span data-stu-id="eccf0-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="eccf0-145"><dt>**\_ambiente de contabilidad general \_ y \_ difuso**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="eccf0-146">Equivalente a llamar a [**glMaterial**](glmaterial-functions.md) dos veces con los mismos valores de parámetro, una vez con el ambiente de contabilidad general \_ y otra con el difuso de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="eccf0-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="eccf0-147"><dt>**\_índices de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="eccf0-148">El parámetro params contiene tres valores de punto flotante que especifican los índices de color para ambiente, difusión y iluminación especular.</span><span class="sxs-lookup"><span data-stu-id="eccf0-148">The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="eccf0-149">Estos tres valores, y \_ el brillo de contabilidad, son los únicos valores de material usados por la ecuación de iluminación del modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="eccf0-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="eccf0-150">Consulte [**glLightModel**](gllightmodel-functions.md) para obtener una explicación de la iluminación del índice de color.</span><span class="sxs-lookup"><span data-stu-id="eccf0-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="eccf0-151">*params*</span><span class="sxs-lookup"><span data-stu-id="eccf0-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="eccf0-152">Valor al que se establecerá el parámetro de brillo de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="eccf0-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eccf0-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eccf0-153">Return value</span></span>

<span data-ttu-id="eccf0-154">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eccf0-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eccf0-155">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="eccf0-155">Error codes</span></span>

<span data-ttu-id="eccf0-156">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="eccf0-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="eccf0-157">Nombre</span><span class="sxs-lookup"><span data-stu-id="eccf0-157">Name</span></span>                                                                                              | <span data-ttu-id="eccf0-158">Significado</span><span class="sxs-lookup"><span data-stu-id="eccf0-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eccf0-159"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="eccf0-160">Cualquiera de las *caras* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="eccf0-161"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="eccf0-162">Se especificó un exponente especular fuera del intervalo de \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="eccf0-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eccf0-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eccf0-163">Remarks</span></span>

<span data-ttu-id="eccf0-164">La función [**glMaterialfv**](glmaterialf.md) asigna valores a los parámetros de material.</span><span class="sxs-lookup"><span data-stu-id="eccf0-164">The [**glMaterialfv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="eccf0-165">Hay dos conjuntos de parámetros de material coincidentes.</span><span class="sxs-lookup"><span data-stu-id="eccf0-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="eccf0-166">Uno, el conjunto *frontal* , se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando está deshabilitada la iluminación dos caras) o simplemente polígonos frontales (cuando está habilitada la iluminación de dos caras).</span><span class="sxs-lookup"><span data-stu-id="eccf0-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="eccf0-167">El otro conjunto, *orientado hacia atrás*, se usa para sombrear polígonos de cara a la inversa solo cuando está habilitada la iluminación de dos caras.</span><span class="sxs-lookup"><span data-stu-id="eccf0-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="eccf0-168">Consulte [**glLightModel**](gllightmodel-functions.md) para obtener más información sobre los cálculos de iluminación de una cara y dos caras.</span><span class="sxs-lookup"><span data-stu-id="eccf0-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="eccf0-169">La función [**glMaterialfv**](glmaterialf.md) toma tres argumentos.</span><span class="sxs-lookup"><span data-stu-id="eccf0-169">The [**glMaterialfv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="eccf0-170">La primera, *cara*, especifica si se modificarán los materiales de la contabilidad general \_ , los materiales traseros de la contabilidad general o los materiales de la \_ \_ parte delantera y trasera del libro de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="eccf0-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="eccf0-171">La segunda, *PName*, especifica cuál de los diversos parámetros de uno o ambos conjuntos se modificarán.</span><span class="sxs-lookup"><span data-stu-id="eccf0-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="eccf0-172">El *tercer parámetro especifica* el valor que se asignará al parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="eccf0-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="eccf0-173">Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="eccf0-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="eccf0-174">La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="eccf0-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="eccf0-175">Los parámetros de material se pueden actualizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="eccf0-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="eccf0-176">En concreto, se puede llamar a [**glMaterialfv**](glmaterialf.md) entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="eccf0-176">In particular, [**glMaterialfv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="eccf0-177">Sin embargo, si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) a **glMaterialfv**.</span><span class="sxs-lookup"><span data-stu-id="eccf0-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialfv**.</span></span>

<span data-ttu-id="eccf0-178">La siguiente función recupera información relacionada con [**glMaterialfv**](glmaterialf.md):</span><span class="sxs-lookup"><span data-stu-id="eccf0-178">The following function retrieves information related to [**glMaterialfv**](glmaterialf.md):</span></span>

[<span data-ttu-id="eccf0-179">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="eccf0-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="eccf0-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eccf0-180">Requirements</span></span>



| <span data-ttu-id="eccf0-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="eccf0-181">Requirement</span></span> | <span data-ttu-id="eccf0-182">Value</span><span class="sxs-lookup"><span data-stu-id="eccf0-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eccf0-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccf0-183">Minimum supported client</span></span><br/> | <span data-ttu-id="eccf0-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eccf0-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eccf0-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccf0-185">Minimum supported server</span></span><br/> | <span data-ttu-id="eccf0-186">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eccf0-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eccf0-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eccf0-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="eccf0-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="eccf0-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eccf0-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="eccf0-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eccf0-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eccf0-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eccf0-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eccf0-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eccf0-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="eccf0-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccf0-194">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="eccf0-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="eccf0-195">**glLight**</span><span class="sxs-lookup"><span data-stu-id="eccf0-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="eccf0-196">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="eccf0-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





