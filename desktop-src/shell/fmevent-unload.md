---
description: Se envía a un archivo DLL de extensión cuando el administrador de archivos está descargando el archivo DLL.
title: Mensaje de FMEVENT_UNLOAD (Wfext. h)
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
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153619"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="2f7ab-103">FMEVENT \_ mensaje de descarga</span><span class="sxs-lookup"><span data-stu-id="2f7ab-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="2f7ab-104">Se envía a un archivo DLL de extensión cuando el administrador de archivos está descargando el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f7ab-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f7ab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7ab-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f7ab-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f7ab-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f7ab-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f7ab-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f7ab-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7ab-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f7ab-110">Return value</span></span>

<span data-ttu-id="2f7ab-111">Un archivo DLL de extensión debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7ab-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f7ab-112">Remarks</span></span>

<span data-ttu-id="2f7ab-113">Es posible que los valores *hWnd* y **hMenu** pasados con los mensajes [**FMEVENT \_ Load**](fmevent-load.md) y [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) no sean válidos en el momento en que se envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7ab-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7ab-114">Requirements</span></span>



| <span data-ttu-id="2f7ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7ab-115">Requirement</span></span> | <span data-ttu-id="2f7ab-116">Value</span><span class="sxs-lookup"><span data-stu-id="2f7ab-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7ab-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7ab-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f7ab-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2f7ab-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7ab-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f7ab-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f7ab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f7ab-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7ab-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7ab-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f7ab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7ab-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="2f7ab-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




