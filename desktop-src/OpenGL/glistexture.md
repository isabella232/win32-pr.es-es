---
title: función glIsTexture (GL. h)
description: La función glIsTexture determina si un nombre corresponde a una textura.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture (función) OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492604"
---
# <a name="glistexture-function"></a><span data-ttu-id="a538d-104">glIsTexture función)</span><span class="sxs-lookup"><span data-stu-id="a538d-104">glIsTexture function</span></span>

<span data-ttu-id="a538d-105">La función **glIsTexture** determina si un nombre corresponde a una textura.</span><span class="sxs-lookup"><span data-stu-id="a538d-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a538d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a538d-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="a538d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a538d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a538d-108">*degrada*</span><span class="sxs-lookup"><span data-stu-id="a538d-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="a538d-109">Valor que es el nombre de una textura.</span><span class="sxs-lookup"><span data-stu-id="a538d-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="a538d-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a538d-110">Error codes</span></span>

<span data-ttu-id="a538d-111">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="a538d-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a538d-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="a538d-112">Name</span></span>                                                                                                  | <span data-ttu-id="a538d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a538d-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a538d-114"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a538d-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a538d-115">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a538d-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a538d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a538d-116">Remarks</span></span>

<span data-ttu-id="a538d-117">Si el parámetro *Texture* es actualmente el nombre de una textura, la función **glIsTexture** devuelve GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="a538d-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="a538d-118">La función **glIsTexture** devuelve GL \_ false si *Texture* es cero.</span><span class="sxs-lookup"><span data-stu-id="a538d-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="a538d-119">También devuelve GL \_ false si es un valor distinto de cero que actualmente no es el nombre de una textura o si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a538d-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="a538d-120">No puede incluir llamadas a **glIsTexture** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="a538d-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="a538d-121">La función **glIsTexture** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a538d-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a538d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a538d-122">Requirements</span></span>



| <span data-ttu-id="a538d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a538d-123">Requirement</span></span> | <span data-ttu-id="a538d-124">Value</span><span class="sxs-lookup"><span data-stu-id="a538d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a538d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a538d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a538d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a538d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a538d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a538d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a538d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a538d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a538d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a538d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a538d-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a538d-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a538d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a538d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a538d-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a538d-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a538d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a538d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a538d-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a538d-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a538d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a538d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a538d-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a538d-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a538d-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="a538d-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="a538d-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a538d-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a538d-139">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="a538d-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="a538d-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a538d-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a538d-141">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a538d-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="a538d-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a538d-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a538d-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a538d-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a538d-144">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a538d-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





