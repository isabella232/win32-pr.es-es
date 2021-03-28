---
description: Enviado por una extensión del administrador de archivos para que el administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.
title: Mensaje de FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275112"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="57301-103">\_Mensaje de \_ Windows actualizar FM</span><span class="sxs-lookup"><span data-stu-id="57301-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="57301-104">Enviado por una extensión del administrador de archivos para que el administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="57301-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="57301-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57301-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57301-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="57301-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="57301-107">Valor que indica si el administrador de archivos vuelve A dibujar su ventana activa o todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="57301-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="57301-108">Si este parámetro es **true**, el administrador de archivos vuelve a dibujar todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="57301-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="57301-109">De lo contrario, el administrador de archivos vuelve a dibujar solo la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="57301-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="57301-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57301-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="57301-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="57301-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57301-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57301-112">Return value</span></span>

<span data-ttu-id="57301-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="57301-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57301-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57301-114">Remarks</span></span>

<span data-ttu-id="57301-115">El administrador de archivos detecta automáticamente los cambios realizados en el sistema de archivos causados por una extensión.</span><span class="sxs-lookup"><span data-stu-id="57301-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="57301-116">Una extensión solo debe usar este mensaje en situaciones en las que se realizan o cancelan conexiones de unidad.</span><span class="sxs-lookup"><span data-stu-id="57301-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="57301-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57301-117">Requirements</span></span>



| <span data-ttu-id="57301-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="57301-118">Requirement</span></span> | <span data-ttu-id="57301-119">Value</span><span class="sxs-lookup"><span data-stu-id="57301-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57301-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57301-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57301-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="57301-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="57301-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57301-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57301-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57301-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="57301-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57301-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57301-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="57301-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57301-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="57301-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57301-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="57301-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




