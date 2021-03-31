---
title: función glGetPolygonStipple (GL. h)
description: La función glGetPolygonStipple devuelve el patrón de los polígonos.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glGetPolygonStipple (función) OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905074"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="2c4c5-104">glGetPolygonStipple función)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="2c4c5-105">La función **glGetPolygonStipple** devuelve el patrón de los polígonos.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c4c5-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="2c4c5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c4c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4c5-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="2c4c5-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="2c4c5-109">Devuelve el patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4c5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c4c5-110">Return value</span></span>

<span data-ttu-id="2c4c5-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c4c5-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2c4c5-112">Error codes</span></span>

<span data-ttu-id="2c4c5-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2c4c5-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c4c5-114">Name</span></span>                                                                                                  | <span data-ttu-id="2c4c5-115">Significado</span><span class="sxs-lookup"><span data-stu-id="2c4c5-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c4c5-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c5-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2c4c5-117">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2c4c5-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c4c5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c4c5-118">Remarks</span></span>

<span data-ttu-id="2c4c5-119">La función **glGetPolygonStipple** devuelve un patrón punteado de 32 polígonos a través del parámetro *Mask* .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="2c4c5-120">El patrón se empaqueta en la memoria como si se llamara a [**glReadPixels**](glreadpixels.md) con el *alto* y el *ancho* de 32, el *tipo* de mapa de bits de contabilidad \_ y el *formato* del índice de color de GL \_ \_ y el patrón punteado se almacenó en un búfer interno de índice de color 32x32.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="2c4c5-121">A diferencia de **glReadPixels**, sin embargo, las operaciones de transferencia de píxeles (desplazamiento, desplazamiento y mapa de píxeles) no se aplican a la imagen de un devuelto.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="2c4c5-122">Si se genera un error, no se realiza ningún cambio en el contenido de la *máscara*.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4c5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c4c5-123">Requirements</span></span>



| <span data-ttu-id="2c4c5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c4c5-124">Requirement</span></span> | <span data-ttu-id="2c4c5-125">Value</span><span class="sxs-lookup"><span data-stu-id="2c4c5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4c5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4c5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4c5-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c4c5-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c4c5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c4c5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4c5-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c4c5-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c4c5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c4c5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4c5-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c5-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c4c5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c4c5-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c4c5-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c5-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c4c5-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c4c5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c4c5-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4c5-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c4c5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c4c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4c5-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2c4c5-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2c4c5-139">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="2c4c5-140">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="2c4c5-141">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="2c4c5-142">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="2c4c5-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





