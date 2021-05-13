---
description: Se envía a un archivo DLL de extensión cuando el Administrador de archivos descarga el archivo DLL.
title: FMEVENT_UNLOAD mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843076"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="5f7cf-103">Mensaje UNLOAD de FMEVENT \_</span><span class="sxs-lookup"><span data-stu-id="5f7cf-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="5f7cf-104">Se envía a un archivo DLL de extensión cuando el Administrador de archivos descarga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="5f7cf-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f7cf-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f7cf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f7cf-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f7cf-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f7cf-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f7cf-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f7cf-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f7cf-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5f7cf-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f7cf-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f7cf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f7cf-110">Return value</span></span>

<span data-ttu-id="5f7cf-111">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5f7cf-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f7cf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f7cf-112">Remarks</span></span>

<span data-ttu-id="5f7cf-113">Los *valores hwnd* **y hMenu** pasados con los mensajes [**\_ FMEVENT LOAD**](fmevent-load.md) y [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) pueden no ser válidos en el momento en que se envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5f7cf-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f7cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f7cf-114">Requirements</span></span>



| <span data-ttu-id="5f7cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f7cf-115">Requirement</span></span> | <span data-ttu-id="5f7cf-116">Value</span><span class="sxs-lookup"><span data-stu-id="5f7cf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7cf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f7cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f7cf-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f7cf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5f7cf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f7cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f7cf-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f7cf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f7cf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f7cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f7cf-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="5f7cf-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f7cf-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f7cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f7cf-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="5f7cf-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




