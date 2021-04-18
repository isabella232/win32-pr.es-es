---
title: función glGetPointerv (GL. h)
description: La función glGetPointerv devuelve la dirección de una matriz de datos de vértice.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686117"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="1281a-104">glGetPointerv función)</span><span class="sxs-lookup"><span data-stu-id="1281a-104">glGetPointerv function</span></span>

<span data-ttu-id="1281a-105">La función **glGetPointerv** devuelve la dirección de una matriz de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="1281a-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="1281a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1281a-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="1281a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1281a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1281a-108">*PName*</span><span class="sxs-lookup"><span data-stu-id="1281a-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="1281a-109">El tipo de puntero de matriz que se va a devolver desde las siguientes constantes simbólicas: \_ puntero de matriz de color \_ de GL \_ , puntero de matriz de \_ \_ marca de borde de contabilidad \_ \_ , puntero de búfer de \_ comentarios de contabilidad \_ \_ , \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ puntero de matriz de índice de contabilidad, puntero de matriz de índice de contabilidad general, puntero de matriz de textura de GL, puntero de búfer de selección de contabilidad</span><span class="sxs-lookup"><span data-stu-id="1281a-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="1281a-110">*params*</span><span class="sxs-lookup"><span data-stu-id="1281a-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="1281a-111">Devuelve el valor del puntero de matriz especificado por *PName*.</span><span class="sxs-lookup"><span data-stu-id="1281a-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1281a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1281a-112">Return value</span></span>

<span data-ttu-id="1281a-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1281a-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1281a-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1281a-114">Error codes</span></span>

<span data-ttu-id="1281a-115">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="1281a-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1281a-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="1281a-116">Name</span></span>                                                                                             | <span data-ttu-id="1281a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="1281a-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="1281a-118"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1281a-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="1281a-119">*PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="1281a-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1281a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1281a-120">Remarks</span></span>

<span data-ttu-id="1281a-121">La función **glGetPointerv** devuelve información de puntero de matriz.</span><span class="sxs-lookup"><span data-stu-id="1281a-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="1281a-122">El parámetro *PName* es una constante simbólica que especifica el tipo de puntero de matriz que se va a devolver y *params* es un puntero a una ubicación donde se colocan los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="1281a-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1281a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1281a-123">Requirements</span></span>



| <span data-ttu-id="1281a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1281a-124">Requirement</span></span> | <span data-ttu-id="1281a-125">Value</span><span class="sxs-lookup"><span data-stu-id="1281a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1281a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1281a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1281a-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1281a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1281a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1281a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1281a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1281a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1281a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1281a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1281a-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1281a-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1281a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1281a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1281a-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1281a-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1281a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1281a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1281a-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1281a-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1281a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1281a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1281a-137">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="1281a-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="1281a-138">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="1281a-139">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1281a-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1281a-140">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1281a-141">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1281a-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1281a-142">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="1281a-143">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1281a-144">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="1281a-145">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="1281a-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





