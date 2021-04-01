---
title: Mensaje de CCM_GETUNICODEFORMAT (commctrl. h)
description: Obtiene la marca del formato de caracteres Unicode para el control.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150564"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="92e2b-104">\_Mensaje GETUNICODEFORMAT de CCM</span><span class="sxs-lookup"><span data-stu-id="92e2b-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="92e2b-105">Obtiene la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="92e2b-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="92e2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92e2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e2b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92e2b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="92e2b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="92e2b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="92e2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92e2b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="92e2b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="92e2b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e2b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92e2b-111">Return value</span></span>

<span data-ttu-id="92e2b-112">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="92e2b-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="92e2b-113">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="92e2b-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="92e2b-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="92e2b-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e2b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e2b-115">Requirements</span></span>



| <span data-ttu-id="92e2b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e2b-116">Requirement</span></span> | <span data-ttu-id="92e2b-117">Value</span><span class="sxs-lookup"><span data-stu-id="92e2b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92e2b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92e2b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92e2b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92e2b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92e2b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92e2b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92e2b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="92e2b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92e2b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92e2b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e2b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e2b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e2b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="92e2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e2b-125">**\_SETUNICODEFORMAT CCM**</span><span class="sxs-lookup"><span data-stu-id="92e2b-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





