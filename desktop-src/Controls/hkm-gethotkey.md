---
title: Mensaje de HKM_GETHOTKEY (commctrl. h)
description: Obtiene el código de tecla virtual y los marcadores modificadores de una tecla de acceso rápido de un control de tecla de acceso rápido.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490211"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="9d9d1-104">HKM \_ GETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="9d9d1-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="9d9d1-105">Obtiene el código de tecla virtual y los marcadores modificadores de una tecla de acceso rápido de un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d9d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d9d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d9d1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9d9d1-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9d9d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d9d1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9d9d1-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9d1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d9d1-111">Return value</span></span>

<span data-ttu-id="9d9d1-112">Devuelve el código de tecla virtual y los marcadores de modificador.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="9d9d1-113">El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de tecla virtual de la tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="9d9d1-114">El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que especifica las teclas que definen una combinación de teclas de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="9d9d1-115">Las marcas modificadoras pueden ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="9d9d1-116">Value</span><span class="sxs-lookup"><span data-stu-id="9d9d1-116">Value</span></span>            | <span data-ttu-id="9d9d1-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9d9d1-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="9d9d1-118">HOTKEYF \_ Alt</span><span class="sxs-lookup"><span data-stu-id="9d9d1-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="9d9d1-119">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="9d9d1-119">ALT key</span></span>      |
| <span data-ttu-id="9d9d1-120">\_control HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="9d9d1-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="9d9d1-121">Tecla CONTROL</span><span class="sxs-lookup"><span data-stu-id="9d9d1-121">CONTROL key</span></span>  |
| <span data-ttu-id="9d9d1-122">\_ext HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="9d9d1-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="9d9d1-123">Clave extendida</span><span class="sxs-lookup"><span data-stu-id="9d9d1-123">Extended key</span></span> |
| <span data-ttu-id="9d9d1-124">HOTKEYF \_ Shift</span><span class="sxs-lookup"><span data-stu-id="9d9d1-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="9d9d1-125">Tecla Mayús</span><span class="sxs-lookup"><span data-stu-id="9d9d1-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="9d9d1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d9d1-126">Remarks</span></span>

<span data-ttu-id="9d9d1-127">El valor de 16 bits devuelto por este mensaje se puede usar como parámetro *wParam* en el mensaje de [**\_ SETHOTKEY de WM**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="9d9d1-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9d1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d9d1-128">Requirements</span></span>



| <span data-ttu-id="9d9d1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d9d1-129">Requirement</span></span> | <span data-ttu-id="9d9d1-130">Value</span><span class="sxs-lookup"><span data-stu-id="9d9d1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9d1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d9d1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9d1-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9d9d1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d9d1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d9d1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9d1-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d9d1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d9d1-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d9d1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9d1-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9d1-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

