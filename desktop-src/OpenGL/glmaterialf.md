---
title: función glMaterialf (GL. h)
description: La función glMaterialf especifica los parámetros de material para el modelo de iluminación.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- glMaterialf (función) OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686216"
---
# <a name="glmaterialf-function"></a><span data-ttu-id="6c05d-104">glMaterialf función)</span><span class="sxs-lookup"><span data-stu-id="6c05d-104">glMaterialf function</span></span>

<span data-ttu-id="6c05d-105">La función **glMaterialf** especifica los parámetros de material para el modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="6c05d-105">The **glMaterialf** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c05d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c05d-106">Syntax</span></span>


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="6c05d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c05d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c05d-108">*Portada*</span><span class="sxs-lookup"><span data-stu-id="6c05d-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="6c05d-109">La cara o caras que se están actualizando.</span><span class="sxs-lookup"><span data-stu-id="6c05d-109">The face or faces that are being updated.</span></span> <span data-ttu-id="6c05d-110">Debe ser uno de los siguientes: GL \_ Front, GL \_ back o GL \_ Front y GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="6c05d-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="6c05d-111">*PName*</span><span class="sxs-lookup"><span data-stu-id="6c05d-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="6c05d-112">Parámetro de material de valor único de la cara o caras que se están actualizando.</span><span class="sxs-lookup"><span data-stu-id="6c05d-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="6c05d-113">Debe ser brillo de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="6c05d-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="6c05d-114">Value</span><span class="sxs-lookup"><span data-stu-id="6c05d-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="6c05d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="6c05d-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="6c05d-116"><dt>**brillo de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="6c05d-117">El parámetro *param* es un valor de punto flotante único que especifica el exponente especular RGBA del material.</span><span class="sxs-lookup"><span data-stu-id="6c05d-117">The *param* parameter is a single floating-point value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="6c05d-118">Los valores enteros se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="6c05d-118">Integer values are mapped directly.</span></span> <span data-ttu-id="6c05d-119">Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] .</span><span class="sxs-lookup"><span data-stu-id="6c05d-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="6c05d-120">El exponente especular predeterminado para el material orientado hacia delante y hacia atrás es 0.</span><span class="sxs-lookup"><span data-stu-id="6c05d-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6c05d-121">*param*</span><span class="sxs-lookup"><span data-stu-id="6c05d-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="6c05d-122">Valor al que se establecerá el parámetro de brillo de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="6c05d-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c05d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c05d-123">Return value</span></span>

<span data-ttu-id="6c05d-124">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6c05d-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c05d-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6c05d-125">Error codes</span></span>

<span data-ttu-id="6c05d-126">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6c05d-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6c05d-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c05d-127">Name</span></span>                                                                                              | <span data-ttu-id="6c05d-128">Significado</span><span class="sxs-lookup"><span data-stu-id="6c05d-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c05d-129"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="6c05d-130">Cualquiera de las *caras* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="6c05d-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="6c05d-131"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="6c05d-132">Se especificó un exponente especular fuera del intervalo de \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="6c05d-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c05d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c05d-133">Remarks</span></span>

<span data-ttu-id="6c05d-134">La función **glMaterialf** asigna valores a los parámetros de material.</span><span class="sxs-lookup"><span data-stu-id="6c05d-134">The **glMaterialf** function assigns values to material parameters.</span></span> <span data-ttu-id="6c05d-135">Hay dos conjuntos de parámetros de material coincidentes.</span><span class="sxs-lookup"><span data-stu-id="6c05d-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="6c05d-136">Uno, el conjunto *frontal* , se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando está deshabilitada la iluminación dos caras) o simplemente polígonos frontales (cuando está habilitada la iluminación de dos caras).</span><span class="sxs-lookup"><span data-stu-id="6c05d-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="6c05d-137">El otro conjunto, *orientado hacia atrás*, se usa para sombrear polígonos de cara a la inversa solo cuando está habilitada la iluminación de dos caras.</span><span class="sxs-lookup"><span data-stu-id="6c05d-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="6c05d-138">Consulte [**glLightModel**](gllightmodel-functions.md) para obtener más información sobre los cálculos de iluminación de una cara y dos caras.</span><span class="sxs-lookup"><span data-stu-id="6c05d-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="6c05d-139">La función **glMaterialf** toma tres argumentos.</span><span class="sxs-lookup"><span data-stu-id="6c05d-139">The **glMaterialf** function takes three arguments.</span></span> <span data-ttu-id="6c05d-140">La primera, *cara*, especifica si se modificarán los materiales de la contabilidad general \_ , los materiales traseros de la contabilidad general o los materiales de la \_ \_ parte delantera y trasera del libro de contabilidad \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6c05d-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="6c05d-141">La segunda, *PName*, especifica cuál de los diversos parámetros de uno o ambos conjuntos se modificarán.</span><span class="sxs-lookup"><span data-stu-id="6c05d-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="6c05d-142">El *tercer parámetro especifica* el valor que se asignará al parámetro especificado.</span><span class="sxs-lookup"><span data-stu-id="6c05d-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="6c05d-143">Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="6c05d-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="6c05d-144">La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="6c05d-145">Los parámetros de material se pueden actualizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6c05d-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="6c05d-146">En concreto, se puede llamar a **glMaterialf** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6c05d-146">In particular, **glMaterialf** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6c05d-147">Sin embargo, si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) a **glMaterialf**.</span><span class="sxs-lookup"><span data-stu-id="6c05d-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialf**.</span></span>

<span data-ttu-id="6c05d-148">La siguiente función recupera información relacionada con **glMaterialf**:</span><span class="sxs-lookup"><span data-stu-id="6c05d-148">The following function retrieves information related to **glMaterialf**:</span></span>

[<span data-ttu-id="6c05d-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="6c05d-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="6c05d-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c05d-150">Requirements</span></span>



| <span data-ttu-id="6c05d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c05d-151">Requirement</span></span> | <span data-ttu-id="6c05d-152">Value</span><span class="sxs-lookup"><span data-stu-id="6c05d-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c05d-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c05d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6c05d-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c05d-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c05d-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c05d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6c05d-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c05d-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c05d-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c05d-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c05d-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6c05d-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c05d-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c05d-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c05d-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c05d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c05d-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c05d-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c05d-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c05d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c05d-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="6c05d-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="6c05d-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="6c05d-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="6c05d-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="6c05d-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





