---
title: función glGetError (GL. h)
description: La función glGetError devuelve información de error.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- glGetError (función) OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996947"
---
# <a name="glgeterror-function"></a><span data-ttu-id="2c0b7-104">glGetError función)</span><span class="sxs-lookup"><span data-stu-id="2c0b7-104">glGetError function</span></span>

<span data-ttu-id="2c0b7-105">La función **glGetError** devuelve información de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0b7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c0b7-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="2c0b7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c0b7-107">Parameters</span></span>

<span data-ttu-id="2c0b7-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c0b7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c0b7-109">Return value</span></span>

<span data-ttu-id="2c0b7-110">La función **glGetError** devuelve uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="2c0b7-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2c0b7-111">Return code</span></span>                                                                                           | <span data-ttu-id="2c0b7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c0b7-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c0b7-113"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2c0b7-114">Se ha especificado un valor inaceptable para un argumento enumerado.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="2c0b7-115">La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="2c0b7-116"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2c0b7-117">Un argumento numérico está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-117">A numeric argument is out of range.</span></span> <span data-ttu-id="2c0b7-118">La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2c0b7-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2c0b7-120">No se permite la operación especificada en el estado actual.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="2c0b7-121">La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="2c0b7-122"><dt>**GL \_ no \_ error**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="2c0b7-123">No se ha registrado ningún error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-123">No error has been recorded.</span></span> <span data-ttu-id="2c0b7-124">Se garantiza que el valor de esta constante simbólica es cero.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="2c0b7-125"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="2c0b7-126">Esta función produciría un desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="2c0b7-127">La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="2c0b7-128"><dt>**subdesbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="2c0b7-129">Esta función produciría un subdesbordamiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="2c0b7-130">La función infractora se omite y no tiene ningún efecto secundario que no sea para establecer la marca de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="2c0b7-131"><dt>**\_memoria insuficiente para GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="2c0b7-132">No queda suficiente memoria para ejecutar la función.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="2c0b7-133">El estado de OpenGL es indefinido, excepto el estado de las marcas de error, después de que se registre este error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="2c0b7-134">Tenga en cuenta que **glGetError** devuelve \_ una operación no válida GL \_ si se llama entre una llamada a [**glBegin**](glbegin.md) y su correspondiente llamada a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2c0b7-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0b7-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c0b7-135">Remarks</span></span>

<span data-ttu-id="2c0b7-136">A cada error detectable se le asigna un código numérico y un nombre simbólico.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="2c0b7-137">Cuando se produce un error, la marca de error se establece en el valor de código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="2c0b7-138">No se registra ningún otro error hasta que se llama a **glGetError** , se devuelve el código de error y la marca se restablece a GL \_ no \_ error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="2c0b7-139">Si una llamada a **glGetError** devuelve GL \_ no \_ error, no habrá ningún error detectable desde la última llamada a **glGetError** o desde que se inicializó OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="2c0b7-140">Para permitir implementaciones distribuidas, puede haber varias marcas de error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="2c0b7-141">Si una marca de error individual ha registrado un error, se devuelve el valor de esa marca y la marca se restablece en GL \_ sin \_ errores cuando se llama a **glGetError** .</span><span class="sxs-lookup"><span data-stu-id="2c0b7-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="2c0b7-142">Si se ha registrado un error en más de una marca, **glGetError** devuelve y borra un valor de marca de error arbitrario.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="2c0b7-143">Si todas las marcas de error se van a restablecer, siempre debe llamar a **glGetError** en un bucle hasta que devuelva GL \_ no \_ error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="2c0b7-144">Inicialmente, todas las marcas de error se establecen en GL \_ no \_ error.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="2c0b7-145">Cuando se establece una marca de error, los resultados de una operación de OpenGL no se definen solo si se \_ ha agotado el libro \_ de \_ memoria.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="2c0b7-146">En todos los demás casos, la función que genera el error se omite y no tiene ningún efecto en el contenido de fotogramas o estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c0b7-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0b7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c0b7-147">Requirements</span></span>



| <span data-ttu-id="2c0b7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c0b7-148">Requirement</span></span> | <span data-ttu-id="2c0b7-149">Value</span><span class="sxs-lookup"><span data-stu-id="2c0b7-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0b7-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c0b7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0b7-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c0b7-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c0b7-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c0b7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0b7-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c0b7-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c0b7-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c0b7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0b7-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c0b7-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c0b7-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c0b7-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c0b7-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c0b7-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c0b7-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b7-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0b7-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c0b7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0b7-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2c0b7-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2c0b7-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2c0b7-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





