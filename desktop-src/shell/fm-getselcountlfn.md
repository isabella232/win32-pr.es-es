---
description: Enviado por una extensión del Administrador de archivos para recuperar el número de archivos seleccionados en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda). El recuento incluye archivos que tienen nombres de archivo largos.
title: FM_GETSELCOUNTLFN mensaje (Wfext.h)
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
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841346"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="ff141-104">Mensaje \_ FM GETSELCOUNTLFN</span><span class="sxs-lookup"><span data-stu-id="ff141-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="ff141-105">Enviado por una extensión del Administrador de archivos para recuperar el número de archivos seleccionados en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="ff141-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="ff141-106">El recuento incluye archivos que tienen nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="ff141-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff141-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff141-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff141-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff141-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ff141-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff141-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ff141-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff141-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ff141-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ff141-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff141-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff141-112">Return value</span></span>

<span data-ttu-id="ff141-113">Devuelve el número de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="ff141-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff141-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff141-114">Remarks</span></span>

<span data-ttu-id="ff141-115">Solo las extensiones que admiten nombres de archivo largos (por ejemplo, extensiones compatibles con la red) deben usar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ff141-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff141-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff141-116">Requirements</span></span>



| <span data-ttu-id="ff141-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff141-117">Requirement</span></span> | <span data-ttu-id="ff141-118">Value</span><span class="sxs-lookup"><span data-stu-id="ff141-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff141-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff141-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff141-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ff141-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ff141-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff141-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff141-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff141-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff141-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff141-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff141-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="ff141-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff141-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff141-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff141-126">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="ff141-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="ff141-127">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="ff141-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="ff141-128">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="ff141-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




