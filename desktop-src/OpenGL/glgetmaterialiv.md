---
title: función glGetMaterialiv (GL. h)
description: Las funciones glGetMaterialfv y glGetMaterialiv devuelven parámetros de material. | función glGetMaterialiv (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glGetMaterialiv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689748"
---
# <a name="glgetmaterialiv-function"></a><span data-ttu-id="b0fbe-105">glGetMaterialiv función)</span><span class="sxs-lookup"><span data-stu-id="b0fbe-105">glGetMaterialiv function</span></span>

<span data-ttu-id="b0fbe-106">Las funciones [**glGetMaterialfv**](glgetmaterialfv.md) y **glGetMaterialiv** devuelven parámetros de material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-106">The [**glGetMaterialfv**](glgetmaterialfv.md) and **glGetMaterialiv** functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0fbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0fbe-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="b0fbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0fbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fbe-109">*Portada*</span><span class="sxs-lookup"><span data-stu-id="b0fbe-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="b0fbe-110">Especifica cuál de los dos materiales se está consultando.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="b0fbe-111">\_Se aceptan el anverso o el libro de contabilidad \_ , que representan el material delantero y el trasero, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b0fbe-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="b0fbe-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b0fbe-113">Parámetro de material que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-113">The material parameter to return.</span></span> <span data-ttu-id="b0fbe-114">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-114">The following values are accepted.</span></span>



| <span data-ttu-id="b0fbe-115">Value</span><span class="sxs-lookup"><span data-stu-id="b0fbe-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="b0fbe-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b0fbe-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="b0fbe-117"><dt>**ambiente de contabilidad general \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="b0fbe-118">El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia ambiente del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="b0fbe-119">Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b0fbe-120">Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="b0fbe-121"><dt>**difusión en contab. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="b0fbe-122">El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia difusa del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="b0fbe-123">Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b0fbe-124">Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="b0fbe-125"><dt>**\_especular GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="b0fbe-126">El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la reflectancia especular del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="b0fbe-127">Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b0fbe-128">Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="b0fbe-129"><dt>**emisión de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="b0fbe-130">El parámetro *params* devuelve cuatro valores enteros o de punto flotante que representan la intensidad de luz emitida del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="b0fbe-131">Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al valor entero representable más positivo y-1,0 se asigna al valor entero representable más negativo.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b0fbe-132">Si el valor interno está fuera del intervalo \[ -1, 1 \] , el valor devuelto de tipo entero correspondiente es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="b0fbe-133"><dt>**brillo de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="b0fbe-134">El parámetro *params* devuelve un entero o un valor de punto flotante que representa el exponente especular del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="b0fbe-135">Los valores enteros, cuando se solicitan, se calculan redondeando el valor de punto flotante interno al valor entero más cercano.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="b0fbe-136"><dt>**\_índices de color de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="b0fbe-137">El parámetro *params* devuelve tres valores enteros o de punto flotante que representan los índices de ambiente, difusos e especulares del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="b0fbe-138">Utilice estos índices solo para la iluminación de índice de color.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="b0fbe-139">(Los demás parámetros se usan solo para la iluminación RGBA). Los valores enteros, cuando se solicitan, se calculan Redondeando los valores de punto flotante internos a los valores enteros más cercanos.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b0fbe-140">*params*</span><span class="sxs-lookup"><span data-stu-id="b0fbe-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b0fbe-141">Devuelve los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fbe-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0fbe-142">Return value</span></span>

<span data-ttu-id="b0fbe-143">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0fbe-144">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b0fbe-144">Error codes</span></span>

<span data-ttu-id="b0fbe-145">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0fbe-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="b0fbe-146">Name</span></span>                                                                                                  | <span data-ttu-id="b0fbe-147">Significado</span><span class="sxs-lookup"><span data-stu-id="b0fbe-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0fbe-148"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0fbe-149">el *destino* o la *consulta* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="b0fbe-150"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0fbe-151">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b0fbe-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0fbe-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0fbe-152">Remarks</span></span>

<span data-ttu-id="b0fbe-153">La función **glGetMaterial** devuelve en *params* el valor o los valores del parámetro *PName* de la *superficie* del material.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="b0fbe-154">Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="b0fbe-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fbe-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0fbe-155">Requirements</span></span>



| <span data-ttu-id="b0fbe-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0fbe-156">Requirement</span></span> | <span data-ttu-id="b0fbe-157">Value</span><span class="sxs-lookup"><span data-stu-id="b0fbe-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fbe-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0fbe-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fbe-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0fbe-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0fbe-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0fbe-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fbe-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0fbe-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0fbe-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0fbe-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fbe-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0fbe-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0fbe-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0fbe-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0fbe-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0fbe-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0fbe-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0fbe-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fbe-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0fbe-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fbe-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b0fbe-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b0fbe-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0fbe-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b0fbe-171">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b0fbe-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





