---
title: función glReadBuffer (GL. h)
description: La función glReadBuffer selecciona un origen de búfer de color para los píxeles.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- glReadBuffer (función) OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686116"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="630d4-104">glReadBuffer función)</span><span class="sxs-lookup"><span data-stu-id="630d4-104">glReadBuffer function</span></span>

<span data-ttu-id="630d4-105">La función **glReadBuffer** selecciona un origen de búfer de color para los píxeles.</span><span class="sxs-lookup"><span data-stu-id="630d4-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="630d4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="630d4-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="630d4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="630d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="630d4-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="630d4-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="630d4-109">Un búfer de color.</span><span class="sxs-lookup"><span data-stu-id="630d4-109">A color buffer.</span></span> <span data-ttu-id="630d4-110">Los valores aceptados son GL \_ Front \_ left, GL \_ Front \_ right, GL \_ back \_ left, GL back Right, GL Front, GL up, GL \_ \_ \_ \_ \_ left, GL \_ right y GL \_ AUX *i*, donde *i* está entre 0 y \_ búferes auxiliares de GL \_ 1.</span><span class="sxs-lookup"><span data-stu-id="630d4-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="630d4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="630d4-111">Return value</span></span>

<span data-ttu-id="630d4-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="630d4-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="630d4-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="630d4-113">Error codes</span></span>

<span data-ttu-id="630d4-114">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="630d4-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="630d4-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="630d4-115">Name</span></span>                                                                                                  | <span data-ttu-id="630d4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="630d4-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="630d4-117"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="630d4-118">el *modo* no era uno de los doce (o más) valores aceptados.</span><span class="sxs-lookup"><span data-stu-id="630d4-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="630d4-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="630d4-120">el *modo* especificó un búfer que no existe.</span><span class="sxs-lookup"><span data-stu-id="630d4-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="630d4-121"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="630d4-122">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="630d4-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="630d4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="630d4-123">Remarks</span></span>

<span data-ttu-id="630d4-124">La función **glReadBuffer** especifica un búfer de color como el origen de los siguientes comandos [**glReadPixels**](glreadpixels.md) y [**glCopyPixels**](glcopypixels.md) .</span><span class="sxs-lookup"><span data-stu-id="630d4-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="630d4-125">El parámetro de *modo* acepta uno de doce valores predefinidos o más.</span><span class="sxs-lookup"><span data-stu-id="630d4-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="630d4-126">(GL \_ ) \_Siempre se definen AUX0 a GL AUX3). En un sistema completamente configurado, GL \_ Front, GL \_ left y GL \_ Front \_ left, todo el nombre del búfer de la izquierda, la \_ parte delantera derecha y el nombre de la contabilidad de la derecha el búfer de la derecha, y el nombre de contabilidad de la izquierda \_ \_ y la parte posterior \_ \_ \_ del búfer de retroceso.</span><span class="sxs-lookup"><span data-stu-id="630d4-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="630d4-127">Las configuraciones de búfer doble no estéreo tienen solo un búfer de la izquierda y la derecha.</span><span class="sxs-lookup"><span data-stu-id="630d4-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="630d4-128">Las configuraciones de un solo búfer tienen un búfer de front-end y front-Right si es estéreo, y solo un búfer de Front-Left si es no estéreo.</span><span class="sxs-lookup"><span data-stu-id="630d4-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="630d4-129">Es un error especificar un búfer inexistente para **glReadBuffer**.</span><span class="sxs-lookup"><span data-stu-id="630d4-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="630d4-130">De forma predeterminada, el *modo* está \_ en la parte frontal de la contabilidad en configuraciones de búfer único y \_ en las configuraciones de búfer doble.</span><span class="sxs-lookup"><span data-stu-id="630d4-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="630d4-131">La siguiente función recupera información relacionada con **glReadBuffer**:</span><span class="sxs-lookup"><span data-stu-id="630d4-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="630d4-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ búfer de lectura de GL \_</span><span class="sxs-lookup"><span data-stu-id="630d4-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="630d4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="630d4-133">Requirements</span></span>



| <span data-ttu-id="630d4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="630d4-134">Requirement</span></span> | <span data-ttu-id="630d4-135">Value</span><span class="sxs-lookup"><span data-stu-id="630d4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="630d4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630d4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="630d4-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="630d4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="630d4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630d4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="630d4-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="630d4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="630d4-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="630d4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="630d4-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="630d4-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="630d4-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="630d4-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="630d4-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="630d4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630d4-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630d4-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="630d4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="630d4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630d4-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="630d4-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="630d4-148">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="630d4-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="630d4-149">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="630d4-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="630d4-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="630d4-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="630d4-151">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="630d4-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





