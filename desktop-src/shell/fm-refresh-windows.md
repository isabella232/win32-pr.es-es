---
description: Enviado por una extensión del Administrador de archivos para hacer que el Administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.
title: FM_REFRESH_WINDOWS mensaje (Wfext.h)
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
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842356"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="9fbeb-103">Mensaje \_ DE WINDOWS DE ACTUALIZACIÓN DE \_ FM</span><span class="sxs-lookup"><span data-stu-id="9fbeb-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="9fbeb-104">Enviado por una extensión del Administrador de archivos para hacer que el Administrador de archivos vuelva a dibujar su ventana activa o todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fbeb-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fbeb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fbeb-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="9fbeb-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="9fbeb-107">Valor que indica si el Administrador de archivos vuelve a dibujar su ventana activa o todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="9fbeb-108">Si este parámetro es **TRUE,** el Administrador de archivos vuelve a dibujar todas sus ventanas.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="9fbeb-109">De lo contrario, el Administrador de archivos vuelve a dibujar solo su ventana activa.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="9fbeb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fbeb-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9fbeb-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fbeb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fbeb-112">Return value</span></span>

<span data-ttu-id="9fbeb-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fbeb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fbeb-114">Remarks</span></span>

<span data-ttu-id="9fbeb-115">El Administrador de archivos detecta automáticamente los cambios del sistema de archivos causados por una extensión.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="9fbeb-116">Una extensión debe usar este mensaje solo en situaciones en las que se realizan o cancelan conexiones de unidad.</span><span class="sxs-lookup"><span data-stu-id="9fbeb-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fbeb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fbeb-117">Requirements</span></span>



| <span data-ttu-id="9fbeb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fbeb-118">Requirement</span></span> | <span data-ttu-id="9fbeb-119">Value</span><span class="sxs-lookup"><span data-stu-id="9fbeb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbeb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbeb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fbeb-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9fbeb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9fbeb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbeb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fbeb-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9fbeb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fbeb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fbeb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fbeb-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="9fbeb-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fbeb-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9fbeb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbeb-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="9fbeb-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




