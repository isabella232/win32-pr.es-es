---
title: función glDrawBuffer (GL. h)
description: La función glDrawBuffer especifica en qué búferes de color se van a dibujar.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- glDrawBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665949"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="4e737-104">glDrawBuffer función)</span><span class="sxs-lookup"><span data-stu-id="4e737-104">glDrawBuffer function</span></span>

<span data-ttu-id="4e737-105">La función **glDrawBuffer** especifica en qué búferes de color se van a dibujar.</span><span class="sxs-lookup"><span data-stu-id="4e737-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e737-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e737-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="4e737-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e737-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e737-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="4e737-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="4e737-109">Especifica hasta cuatro búferes de color en los que se van a dibujar con las siguientes constantes simbólicas aceptables.</span><span class="sxs-lookup"><span data-stu-id="4e737-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="4e737-110">Value</span><span class="sxs-lookup"><span data-stu-id="4e737-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="4e737-111">Significado</span><span class="sxs-lookup"><span data-stu-id="4e737-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="4e737-112"><dt>**GL \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="4e737-113">No se escriben búferes de color.</span><span class="sxs-lookup"><span data-stu-id="4e737-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="4e737-114"><dt>**en la \_ parte frontal \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="4e737-115">Solo se escribe el búfer de color Front-Left.</span><span class="sxs-lookup"><span data-stu-id="4e737-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="4e737-116"><dt>**lado \_ derecho de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="4e737-117">Solo se escribe el búfer de color Front-Right.</span><span class="sxs-lookup"><span data-stu-id="4e737-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="4e737-118"><dt>**LIBRO de \_ fondo hacia la \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="4e737-119">Solo se escribe el búfer de color de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="4e737-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="4e737-120"><dt>**\_derecha atrás \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="4e737-121">Solo se escribe el búfer de color de la derecha.</span><span class="sxs-lookup"><span data-stu-id="4e737-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="4e737-122"><dt>**frontal de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="4e737-123">Solo se escriben los búferes de color Front-Left y front-Right.</span><span class="sxs-lookup"><span data-stu-id="4e737-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="4e737-124">Si no hay ningún búfer de colores delante de la derecha, solo se escribe el búfer de color izquierdo frontal.</span><span class="sxs-lookup"><span data-stu-id="4e737-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="4e737-125"><dt>**libro \_ de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="4e737-126">Solo se escriben los búferes de color de la izquierda y la derecha.</span><span class="sxs-lookup"><span data-stu-id="4e737-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="4e737-127">Si no hay ningún búfer de color de fondo derecho, solo se escribe el búfer de color de fondo izquierdo.</span><span class="sxs-lookup"><span data-stu-id="4e737-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="4e737-128"><dt>**libro de contabilidad \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="4e737-129">Solo se escriben los búferes de color Front-Left y back-Left.</span><span class="sxs-lookup"><span data-stu-id="4e737-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="4e737-130">Si no hay ningún búfer de color de fondo izquierdo, solo se escribe el búfer de color Front-Left.</span><span class="sxs-lookup"><span data-stu-id="4e737-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="4e737-131"><dt>**libro de contabilidad \_ derecha**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="4e737-132">Solo se escriben los búferes de color de la derecha y la derecha.</span><span class="sxs-lookup"><span data-stu-id="4e737-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="4e737-133">Si no hay ningún búfer de color de fondo derecho, solo se escribe el búfer de color de la derecha.</span><span class="sxs-lookup"><span data-stu-id="4e737-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="4e737-134"><dt>**\_anverso \_ y \_ atrás de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="4e737-135">Se escriben todos los búferes de color delantero y de fondo (Front-Left, Front-Right, Back-izquierda, hacia la derecha).</span><span class="sxs-lookup"><span data-stu-id="4e737-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="4e737-136">Si no hay ningún búfer de color de fondo, solo se escriben los búferes de color Front-Left y front-Right.</span><span class="sxs-lookup"><span data-stu-id="4e737-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="4e737-137">Si no hay ningún búfer de color a la derecha, solo se escriben los búferes de color Front-Left y back-izquierda.</span><span class="sxs-lookup"><span data-stu-id="4e737-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="4e737-138">Si no hay ningún búfer de color derecho o de fondo, solo se escribe el búfer de color Front-Left.</span><span class="sxs-lookup"><span data-stu-id="4e737-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="4e737-139"><dt>**GL \_ AUXi**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="4e737-140">Solo se escribe el búfer de color auxiliar *i* . *i* está entre 0 y \_ \_ búferes auxiliares de GL-1.</span><span class="sxs-lookup"><span data-stu-id="4e737-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="4e737-141">(GL \_ ) \_Los búferes de AUX no son el límite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar el número de búferes auxiliares disponibles).</span><span class="sxs-lookup"><span data-stu-id="4e737-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="4e737-142">El valor predeterminado es el \_ front-end para los contextos de un solo búfer y el libro \_ de reserva para los contextos de doble búfer.</span><span class="sxs-lookup"><span data-stu-id="4e737-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e737-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e737-143">Return value</span></span>

<span data-ttu-id="4e737-144">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4e737-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e737-145">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4e737-145">Error codes</span></span>

<span data-ttu-id="4e737-146">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="4e737-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4e737-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e737-147">Name</span></span>                                                                                                  | <span data-ttu-id="4e737-148">Significado</span><span class="sxs-lookup"><span data-stu-id="4e737-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e737-149"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4e737-150">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="4e737-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4e737-151"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4e737-152">Ninguno de los búferes indicados por el *modo* existía.</span><span class="sxs-lookup"><span data-stu-id="4e737-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="4e737-153"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4e737-154">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4e737-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="4e737-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e737-155">Remarks</span></span>

<span data-ttu-id="4e737-156">Cuando los colores se escriben en fotogramas, se escriben en los búferes de color especificados por **glDrawBuffer**.</span><span class="sxs-lookup"><span data-stu-id="4e737-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="4e737-157">Si se selecciona más de un búfer de color para dibujar, las operaciones lógicas o de mezcla se calculan y se aplican de forma independiente para cada búfer de color y pueden generar resultados diferentes en cada búfer.</span><span class="sxs-lookup"><span data-stu-id="4e737-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="4e737-158">Los contextos de Monoscopic incluyen solo los búferes izquierdos y los contextos de Stereoscopic incluyen los búferes izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="4e737-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="4e737-159">Del mismo modo, los contextos de un solo búfer incluyen solo los búferes frontales y los contextos de búfer doble incluyen los búferes frontal y posterior.</span><span class="sxs-lookup"><span data-stu-id="4e737-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="4e737-160">El contexto se selecciona en la inicialización de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4e737-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="4e737-161">Siempre es el caso de GL \_ AUX *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="4e737-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="4e737-162">Las siguientes funciones recuperan información relacionada con la función **glDrawBuffer** :</span><span class="sxs-lookup"><span data-stu-id="4e737-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="4e737-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de \_ búfer de dibujo de GL \_</span><span class="sxs-lookup"><span data-stu-id="4e737-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="4e737-164">**glGet** con \_ búferes auxiliares de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="4e737-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="4e737-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e737-165">Requirements</span></span>



| <span data-ttu-id="4e737-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e737-166">Requirement</span></span> | <span data-ttu-id="4e737-167">Value</span><span class="sxs-lookup"><span data-stu-id="4e737-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e737-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e737-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4e737-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4e737-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e737-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e737-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4e737-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e737-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e737-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e737-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e737-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4e737-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e737-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e737-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e737-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e737-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e737-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e737-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e737-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e737-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e737-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4e737-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4e737-180">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="4e737-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="4e737-181">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="4e737-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="4e737-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4e737-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4e737-183">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4e737-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4e737-184">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="4e737-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="4e737-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="4e737-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="4e737-186">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="4e737-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





