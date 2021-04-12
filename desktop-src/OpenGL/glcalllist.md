---
title: función glCallList (GL. h)
description: La función glCallList ejecuta una lista de visualización.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList (función) OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150436"
---
# <a name="glcalllist-function"></a><span data-ttu-id="d2471-104">glCallList función)</span><span class="sxs-lookup"><span data-stu-id="d2471-104">glCallList function</span></span>

<span data-ttu-id="d2471-105">La función **glCallList** ejecuta una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="d2471-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2471-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2471-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="d2471-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2471-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2471-108">*list*</span><span class="sxs-lookup"><span data-stu-id="d2471-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="d2471-109">El nombre entero de la lista de visualización que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="d2471-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2471-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2471-110">Return value</span></span>

<span data-ttu-id="d2471-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d2471-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2471-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2471-112">Remarks</span></span>

<span data-ttu-id="d2471-113">Al invocar la función **glCallList** se inicia la ejecución de la lista de visualización con nombre.</span><span class="sxs-lookup"><span data-stu-id="d2471-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="d2471-114">Las funciones guardadas en la lista de visualización se ejecutan en orden, como si se hubieran llamado sin usar una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="d2471-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="d2471-115">Si *List* no se ha definido como una lista de visualización, se omite **glCallList** .</span><span class="sxs-lookup"><span data-stu-id="d2471-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="d2471-116">La función **glCallList** puede aparecer dentro de una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="d2471-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="d2471-117">Para evitar la posibilidad de que se produzca una recursividad infinita como resultado de la llamada a otras listas, se coloca un límite en el nivel de anidamiento de las listas de visualización durante la ejecución de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="d2471-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="d2471-118">Este límite es al menos 64, sin embargo, depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="d2471-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="d2471-119">El estado de OpenGL no se guarda y se restaura a través de una llamada a **glCallList**.</span><span class="sxs-lookup"><span data-stu-id="d2471-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="d2471-120">Por lo tanto, los cambios realizados en el estado de OpenGL durante la ejecución de una lista de visualización permanecen después de que se complete la ejecución de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="d2471-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="d2471-121">Para conservar el estado de OpenGL en todas las llamadas de **glCallList** , use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix**](glpopmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="d2471-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="d2471-122">Puede ejecutar listas de visualización entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre que la lista de visualización incluya solo las funciones que se permiten en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d2471-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="d2471-123">Las siguientes funciones recuperan información relacionada con **glCallList**:</span><span class="sxs-lookup"><span data-stu-id="d2471-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="d2471-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ anidamiento de lista Max de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="d2471-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="d2471-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="d2471-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="d2471-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2471-126">Requirements</span></span>



| <span data-ttu-id="d2471-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2471-127">Requirement</span></span> | <span data-ttu-id="d2471-128">Value</span><span class="sxs-lookup"><span data-stu-id="d2471-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2471-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2471-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d2471-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2471-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d2471-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2471-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d2471-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2471-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2471-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2471-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2471-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2471-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d2471-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2471-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2471-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2471-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2471-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2471-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2471-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2471-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2471-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2471-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2471-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d2471-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d2471-141">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="d2471-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="d2471-142">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="d2471-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="d2471-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d2471-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d2471-144">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="d2471-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="d2471-145">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d2471-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d2471-146">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="d2471-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="d2471-147">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="d2471-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="d2471-148">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="d2471-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="d2471-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="d2471-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="d2471-150">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="d2471-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="d2471-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="d2471-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





