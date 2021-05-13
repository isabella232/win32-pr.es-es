---
description: Enviado por una extensión del Administrador de archivos para recuperar un recuento de los archivos seleccionados en la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).
title: FM_GETSELCOUNT mensaje (Wfext.h)
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
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842376"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="7fe4f-103">Mensaje \_ DE FM GETSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="7fe4f-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="7fe4f-104">Enviado por una extensión del Administrador de archivos para recuperar un recuento de los archivos seleccionados en la ventana activa del Administrador de archivos (ya sea la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="7fe4f-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="7fe4f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fe4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe4f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fe4f-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fe4f-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7fe4f-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7fe4f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fe4f-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fe4f-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7fe4f-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe4f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fe4f-110">Return value</span></span>

<span data-ttu-id="7fe4f-111">Devuelve el número de archivos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="7fe4f-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe4f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fe4f-112">Requirements</span></span>



| <span data-ttu-id="7fe4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe4f-113">Requirement</span></span> | <span data-ttu-id="7fe4f-114">Value</span><span class="sxs-lookup"><span data-stu-id="7fe4f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe4f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fe4f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe4f-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7fe4f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7fe4f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fe4f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe4f-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7fe4f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7fe4f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fe4f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe4f-120"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe4f-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe4f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7fe4f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe4f-122">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="7fe4f-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="7fe4f-123">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="7fe4f-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="7fe4f-124">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="7fe4f-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




