---
description: Enviado por una extensión del administrador de archivos para recuperar un recuento de los archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda).
title: Mensaje de FM_GETSELCOUNT (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: aac7d08de3785bb02c31dabc1ef7a25fea0d5b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997217"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="7b332-103">\_Mensaje GETSELCOUNT de FM</span><span class="sxs-lookup"><span data-stu-id="7b332-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="7b332-104">Enviado por una extensión del administrador de archivos para recuperar un recuento de los archivos seleccionados en la ventana del administrador de archivos activo (la ventana de directorio o la ventana de resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="7b332-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="7b332-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b332-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b332-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b332-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7b332-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7b332-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7b332-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b332-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7b332-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7b332-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b332-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b332-110">Return value</span></span>

<span data-ttu-id="7b332-111">Devuelve el número de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="7b332-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b332-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b332-112">Requirements</span></span>



| <span data-ttu-id="7b332-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b332-113">Requirement</span></span> | <span data-ttu-id="7b332-114">Value</span><span class="sxs-lookup"><span data-stu-id="7b332-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b332-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b332-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7b332-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7b332-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7b332-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b332-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7b332-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b332-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7b332-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b332-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b332-120"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b332-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b332-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b332-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b332-122">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="7b332-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="7b332-123">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="7b332-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="7b332-124">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="7b332-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




