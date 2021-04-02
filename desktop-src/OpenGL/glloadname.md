---
title: función glLoadName (GL. h)
description: La función glLoadName carga un nombre en la pila de nombres.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName (función) OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151196"
---
# <a name="glloadname-function"></a><span data-ttu-id="a25fc-104">glLoadName función)</span><span class="sxs-lookup"><span data-stu-id="a25fc-104">glLoadName function</span></span>

<span data-ttu-id="a25fc-105">La función **glLoadName** carga un nombre en la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="a25fc-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="a25fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a25fc-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="a25fc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a25fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a25fc-108">*name*</span><span class="sxs-lookup"><span data-stu-id="a25fc-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="a25fc-109">Nombre que reemplazará el valor superior de la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="a25fc-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a25fc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a25fc-110">Return value</span></span>

<span data-ttu-id="a25fc-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a25fc-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a25fc-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a25fc-112">Error codes</span></span>

<span data-ttu-id="a25fc-113">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a25fc-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a25fc-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="a25fc-114">Name</span></span>                                                                                                  | <span data-ttu-id="a25fc-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a25fc-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a25fc-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a25fc-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a25fc-117">Se llamó a la función mientras la pila de nombres estaba vacía.</span><span class="sxs-lookup"><span data-stu-id="a25fc-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="a25fc-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a25fc-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a25fc-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a25fc-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a25fc-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a25fc-120">Remarks</span></span>

<span data-ttu-id="a25fc-121">La función **glLoadName** hace que *Name* Reemplace el valor de la parte superior de la pila de nombres, que inicialmente está vacío.</span><span class="sxs-lookup"><span data-stu-id="a25fc-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="a25fc-122">La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a25fc-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="a25fc-123">Consta de un conjunto ordenado de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="a25fc-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="a25fc-124">La pila de nombres está siempre vacía mientras que el modo de representación no es de selección de libro \_ .</span><span class="sxs-lookup"><span data-stu-id="a25fc-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="a25fc-125">Se omiten las llamadas a **glLoadName** mientras el modo de representación no sea Select de GL \_ .</span><span class="sxs-lookup"><span data-stu-id="a25fc-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="a25fc-126">Las siguientes funciones recuperan información relacionada con **glLoadName**:</span><span class="sxs-lookup"><span data-stu-id="a25fc-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="a25fc-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a25fc-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="a25fc-128">**glGet** con el argumento LM \_ Max \_ name \_ stack \_ Depth</span><span class="sxs-lookup"><span data-stu-id="a25fc-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="a25fc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a25fc-129">Requirements</span></span>



| <span data-ttu-id="a25fc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a25fc-130">Requirement</span></span> | <span data-ttu-id="a25fc-131">Value</span><span class="sxs-lookup"><span data-stu-id="a25fc-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a25fc-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a25fc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a25fc-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a25fc-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a25fc-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a25fc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a25fc-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a25fc-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a25fc-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a25fc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a25fc-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25fc-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a25fc-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a25fc-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a25fc-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a25fc-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a25fc-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a25fc-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a25fc-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a25fc-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25fc-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a25fc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25fc-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a25fc-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a25fc-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a25fc-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a25fc-145">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="a25fc-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="a25fc-146">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="a25fc-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="a25fc-147">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="a25fc-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="a25fc-148">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="a25fc-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





