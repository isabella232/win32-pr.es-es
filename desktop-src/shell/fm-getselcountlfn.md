---
description: Enviado por una extensión del administrador de archivos para recuperar el número de archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.
title: Mensaje de FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997745"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="89b29-104">\_Mensaje GETSELCOUNTLFN de FM</span><span class="sxs-lookup"><span data-stu-id="89b29-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="89b29-105">Enviado por una extensión del administrador de archivos para recuperar el número de archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="89b29-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="89b29-106">El recuento incluye archivos que tienen nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="89b29-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="89b29-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89b29-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b29-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89b29-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89b29-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="89b29-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89b29-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89b29-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="89b29-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="89b29-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b29-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89b29-112">Return value</span></span>

<span data-ttu-id="89b29-113">Devuelve el número de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="89b29-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="89b29-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89b29-114">Remarks</span></span>

<span data-ttu-id="89b29-115">Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones basadas en red) deben utilizar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="89b29-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b29-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89b29-116">Requirements</span></span>



| <span data-ttu-id="89b29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="89b29-117">Requirement</span></span> | <span data-ttu-id="89b29-118">Value</span><span class="sxs-lookup"><span data-stu-id="89b29-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89b29-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89b29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89b29-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="89b29-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89b29-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89b29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89b29-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89b29-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89b29-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89b29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89b29-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="89b29-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b29-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="89b29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b29-126">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="89b29-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="89b29-127">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="89b29-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="89b29-128">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="89b29-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




