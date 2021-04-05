---
title: función glGetString (GL. h)
description: La función glGetString devuelve una cadena que describe la conexión de OpenGL actual.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString (función) OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997003"
---
# <a name="glgetstring-function"></a><span data-ttu-id="7d9b7-104">glGetString función)</span><span class="sxs-lookup"><span data-stu-id="7d9b7-104">glGetString function</span></span>

<span data-ttu-id="7d9b7-105">La función **glGetString** devuelve una cadena que describe la conexión de OpenGL actual.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9b7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d9b7-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="7d9b7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d9b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d9b7-108">*name*</span><span class="sxs-lookup"><span data-stu-id="7d9b7-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d9b7-109">Una de las constantes simbólicas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="7d9b7-110">Value</span><span class="sxs-lookup"><span data-stu-id="7d9b7-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7d9b7-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7d9b7-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="7d9b7-112"><dt>**proveedor de contabilidad general \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="7d9b7-113">Devuelve la empresa responsable de esta implementación de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="7d9b7-114">Este nombre no cambia de Release a Release.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="7d9b7-115"><dt>**Representador de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="7d9b7-116">Devuelve el nombre del representador.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-116">Returns the name of the renderer.</span></span> <span data-ttu-id="7d9b7-117">Este nombre suele ser específico de una configuración determinada de una plataforma de hardware.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="7d9b7-118">No cambia de Release a Release.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="7d9b7-119"><dt>**versión de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="7d9b7-120">Devuelve una versión o un número de versión.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="7d9b7-121"><dt>**extensiones de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="7d9b7-122">Devuelve una lista separada por espacios de las extensiones admitidas a OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="7d9b7-123">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7d9b7-123">Error codes</span></span>

<span data-ttu-id="7d9b7-124">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7d9b7-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d9b7-125">Name</span></span>                                                                                                  | <span data-ttu-id="7d9b7-126">Significado</span><span class="sxs-lookup"><span data-stu-id="7d9b7-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d9b7-127"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7d9b7-128">*el nombre* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="7d9b7-129"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7d9b7-130">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7d9b7-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7d9b7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d9b7-131">Remarks</span></span>

<span data-ttu-id="7d9b7-132">La función **glGetString** devuelve un puntero a una cadena estática que describe algún aspecto de la conexión de OpenGL actual.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="7d9b7-133">Dado que OpenGL no incluye consultas para las características de rendimiento de una implementación, se espera que algunas aplicaciones se escriban para reconocer plataformas conocidas y modifiquen el uso de OpenGL en función de las características de rendimiento conocidas de estas plataformas.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="7d9b7-134">Las cadenas de \_ representador de contabilidad y de libro de contabilidad de forma \_ exclusiva especifican una plataforma y no cambiarán de Release a Release.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="7d9b7-135">Los algoritmos de reconocimiento de plataforma deben usarlos como tales.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="7d9b7-136">El formato y el contenido de la cadena que devuelve **glGetString** dependen de la implementación, excepto en que:</span><span class="sxs-lookup"><span data-stu-id="7d9b7-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="7d9b7-137">Los nombres de extensión no incluirán caracteres de espacio y estarán separados por caracteres de espacio en la \_ cadena de extensiones GL.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="7d9b7-138">La cadena de versión de GL \_ comienza con un número de versión.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="7d9b7-139">El número de versión usa una de estas formas:</span><span class="sxs-lookup"><span data-stu-id="7d9b7-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="7d9b7-140">*\_ número principal*. *\_ número secundario*</span><span class="sxs-lookup"><span data-stu-id="7d9b7-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="7d9b7-141">*\_ número principal*. *\_ número secundario*. *\_ número de versión*</span><span class="sxs-lookup"><span data-stu-id="7d9b7-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="7d9b7-142">La información específica del proveedor puede seguir el número de versión.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="7d9b7-143">Su formato depende de la implementación, pero un espacio siempre separa el número de versión y la información específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="7d9b7-144">Todas las cadenas terminan en NULL.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-144">All strings are null-terminated.</span></span>

<span data-ttu-id="7d9b7-145">Si se genera un error, **glGetString** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="7d9b7-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9b7-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d9b7-146">Requirements</span></span>



| <span data-ttu-id="7d9b7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9b7-147">Requirement</span></span> | <span data-ttu-id="7d9b7-148">Value</span><span class="sxs-lookup"><span data-stu-id="7d9b7-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9b7-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d9b7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7d9b7-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7d9b7-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7d9b7-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d9b7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7d9b7-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d9b7-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d9b7-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d9b7-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d9b7-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7d9b7-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d9b7-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d9b7-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d9b7-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d9b7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d9b7-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b7-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d9b7-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d9b7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9b7-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7d9b7-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7d9b7-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7d9b7-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





