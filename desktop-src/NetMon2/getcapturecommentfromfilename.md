---
description: La función GetCaptureCommentFromFilename extrae el comentario de captura de un archivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Función GetCaptureCommentFromFilename (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677283"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="b5fd3-103">GetCaptureCommentFromFilename función)</span><span class="sxs-lookup"><span data-stu-id="b5fd3-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="b5fd3-104">La función **GetCaptureCommentFromFilename** extrae el comentario de captura de un [*archivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="b5fd3-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5fd3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5fd3-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="b5fd3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5fd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5fd3-107">*lpFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5fd3-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fd3-108">Puntero al nombre del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="b5fd3-109">*lpComment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5fd3-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fd3-110">Puntero a una cadena asignada previamente para el comentario.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="b5fd3-111">*BufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5fd3-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fd3-112">Tamaño de la cadena.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5fd3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5fd3-113">Return value</span></span>

<span data-ttu-id="b5fd3-114">Si la función es correcta (es decir, si se encuentra el comentario y se copia, o si no hay ningún comentario en el archivo de captura), el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b5fd3-115">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="b5fd3-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b5fd3-116">Return code</span></span>                                                                                                 | <span data-ttu-id="b5fd3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5fd3-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5fd3-118"><dt>**\_error de \_ lectura del archivo NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="b5fd3-119">No se puede leer el comentario de captura.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="b5fd3-120"><dt>**NMERR \_ \_ formato de archivo no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="b5fd3-121">El marco del comentario no es un formato de archivo válido.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="b5fd3-122"><dt>**\_ \_ no \_ se encontró el archivo NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="b5fd3-123">No se encuentra el archivo especificado por el parámetro *lpFilename* .</span><span class="sxs-lookup"><span data-stu-id="b5fd3-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="b5fd3-124"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="b5fd3-125">Uno de los parámetros no se ha especificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5fd3-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="b5fd3-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5fd3-126">Remarks</span></span>

<span data-ttu-id="b5fd3-127">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureCommentFromFilename** .</span><span class="sxs-lookup"><span data-stu-id="b5fd3-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="b5fd3-128">Para recuperar el comentario de una captura en tiempo real, llame a la función [GetCaptureComment](getcapturecomment.md) .</span><span class="sxs-lookup"><span data-stu-id="b5fd3-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5fd3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5fd3-129">Requirements</span></span>



| <span data-ttu-id="b5fd3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5fd3-130">Requirement</span></span> | <span data-ttu-id="b5fd3-131">Value</span><span class="sxs-lookup"><span data-stu-id="b5fd3-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fd3-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5fd3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b5fd3-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5fd3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b5fd3-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5fd3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b5fd3-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5fd3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b5fd3-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5fd3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5fd3-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b5fd3-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5fd3-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5fd3-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5fd3-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5fd3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5fd3-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5fd3-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5fd3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5fd3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5fd3-143">GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="b5fd3-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




