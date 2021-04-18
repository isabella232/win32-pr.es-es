---
title: función glArrayElement (GL. h)
description: La función glArrayElement especifica los elementos de la matriz que se usan para representar un vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement (función) OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686008"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="684d0-104">glArrayElement función)</span><span class="sxs-lookup"><span data-stu-id="684d0-104">glArrayElement function</span></span>

<span data-ttu-id="684d0-105">La función **glArrayElement** especifica los elementos de la matriz que se usan para representar un vértice.</span><span class="sxs-lookup"><span data-stu-id="684d0-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="684d0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="684d0-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="684d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="684d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="684d0-108">*índice*</span><span class="sxs-lookup"><span data-stu-id="684d0-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="684d0-109">Índice de las matrices habilitadas.</span><span class="sxs-lookup"><span data-stu-id="684d0-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="684d0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="684d0-110">Return value</span></span>

<span data-ttu-id="684d0-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="684d0-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="684d0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="684d0-112">Remarks</span></span>

<span data-ttu-id="684d0-113">Use la función **glArrayElement** dentro de pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) para especificar datos de vértices y atributos para los primitivos de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="684d0-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="684d0-114">La función **glArrayElement** especifica los datos para un solo vértice con datos de vértice y de atributo ubicados en el *Índice* de las matrices de vértices habilitadas.</span><span class="sxs-lookup"><span data-stu-id="684d0-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="684d0-115">Puede usar **glArrayElement** para construir primitivos mediante la indexación de datos de vértices, en lugar de hacerlo mediante el streaming de matrices de datos en orden de primero a último.</span><span class="sxs-lookup"><span data-stu-id="684d0-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="684d0-116">Dado que **glArrayElement** especifica solo un solo vértice, puede especificar explícitamente atributos para primitivos individuales.</span><span class="sxs-lookup"><span data-stu-id="684d0-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="684d0-117">Por ejemplo, puede establecer un solo normal para cada triángulo individual.</span><span class="sxs-lookup"><span data-stu-id="684d0-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="684d0-118">Al incluir llamadas a **glArrayElement** en las listas de visualización, los datos de la matriz necesarios, determinados por los punteros de matriz y los valores de habilitación, también se especifican en la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="684d0-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="684d0-119">Los valores de puntero de matriz y habilitar se determinan cuando se crean listas de visualización, no cuando se ejecutan listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="684d0-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="684d0-120">Puede leer y almacenar en caché los datos estáticos de la matriz en cualquier momento con **glArrayElement**.</span><span class="sxs-lookup"><span data-stu-id="684d0-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="684d0-121">Cuando se modifican los elementos de una matriz estática sin especificar la matriz de nuevo, los resultados de las llamadas subsiguientes a **glArrayElement** son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="684d0-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="684d0-122">Cuando se llama a **glArrayElement** sin llamar primero a **glEnableClientState**( \_ \_ matriz de vértices de GL), no se produce ningún dibujo, pero se modifican los atributos correspondientes a las matrices habilitadas.</span><span class="sxs-lookup"><span data-stu-id="684d0-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="684d0-123">Aunque no se genera ningún error al especificar una matriz dentro de los pares **glBegin** y **glEnd** , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="684d0-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="684d0-124">La función **glArrayElement** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="684d0-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="684d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="684d0-125">Requirements</span></span>



| <span data-ttu-id="684d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="684d0-126">Requirement</span></span> | <span data-ttu-id="684d0-127">Value</span><span class="sxs-lookup"><span data-stu-id="684d0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="684d0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="684d0-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="684d0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="684d0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="684d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="684d0-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="684d0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="684d0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="684d0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="684d0-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="684d0-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="684d0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="684d0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="684d0-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="684d0-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="684d0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="684d0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="684d0-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="684d0-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684d0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="684d0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684d0-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="684d0-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="684d0-140">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="684d0-141">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="684d0-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="684d0-142">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="684d0-143">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="684d0-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="684d0-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="684d0-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="684d0-145">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="684d0-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="684d0-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="684d0-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="684d0-147">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="684d0-148">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="684d0-149">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="684d0-150">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="684d0-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





