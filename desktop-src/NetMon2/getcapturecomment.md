---
description: Devuelve un puntero al comentario de una captura.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Función GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666285"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="9c961-103">GetCaptureComment función)</span><span class="sxs-lookup"><span data-stu-id="9c961-103">GetCaptureComment function</span></span>

<span data-ttu-id="9c961-104">La función **GetCaptureComment** devuelve un puntero al comentario de una captura.</span><span class="sxs-lookup"><span data-stu-id="9c961-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c961-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c961-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="9c961-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c961-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c961-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c961-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="9c961-108">A handle to the capture.</span></span> <span data-ttu-id="9c961-109">Para obtener más información sobre cómo obtener el identificador de captura, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c961-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c961-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c961-110">Return value</span></span>

<span data-ttu-id="9c961-111">Si la función es correcta (es decir, si la captura contiene un comentario), el valor devuelto es un puntero a la cadena de comentario.</span><span class="sxs-lookup"><span data-stu-id="9c961-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="9c961-112">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="9c961-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c961-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c961-113">Remarks</span></span>

<span data-ttu-id="9c961-114">No modifique la cadena de comentario devuelta, que es la cadena de comentario real que se encuentra en la captura cargada.</span><span class="sxs-lookup"><span data-stu-id="9c961-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="9c961-115">Cualquier cambio puede dañar la captura.</span><span class="sxs-lookup"><span data-stu-id="9c961-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="9c961-116">Los intentos de modificar la cadena producen una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c961-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="9c961-117">El identificador de la captura se puede obtener de varias maneras, dependiendo de si el experto o el analizador realizan la llamada.</span><span class="sxs-lookup"><span data-stu-id="9c961-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="9c961-118">En el caso de los expertos, el identificador se especifica en el miembro **hCapture** de la estructura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9c961-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="9c961-119">En el caso de los analizadores, el identificador de captura se puede obtener llamando a la función [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="9c961-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="9c961-120">Para recuperar el comentario de una captura de su archivo de captura, llame a la función [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .</span><span class="sxs-lookup"><span data-stu-id="9c961-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="9c961-121">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureComment** .</span><span class="sxs-lookup"><span data-stu-id="9c961-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c961-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c961-122">Requirements</span></span>



| <span data-ttu-id="9c961-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c961-123">Requirement</span></span> | <span data-ttu-id="9c961-124">Value</span><span class="sxs-lookup"><span data-stu-id="9c961-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c961-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c961-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9c961-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9c961-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9c961-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c961-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9c961-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9c961-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c961-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c961-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c961-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c961-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9c961-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c961-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c961-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c961-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c961-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c961-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c961-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c961-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c961-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c961-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c961-136">EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="9c961-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="9c961-137">GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="9c961-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="9c961-138">GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="9c961-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




