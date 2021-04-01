---
title: Mensaje de BCM_SETSHIELD (commctrl. h)
description: Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la \_ macro Button SetElevationRequiredState.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150198"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="ae279-105">\_Mensaje SETSHIELD de BCM</span><span class="sxs-lookup"><span data-stu-id="ae279-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="ae279-106">Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="ae279-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="ae279-107">Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .</span><span class="sxs-lookup"><span data-stu-id="ae279-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae279-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae279-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae279-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae279-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae279-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ae279-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ae279-111">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae279-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae279-112">Valor **booleano** que es **true** para dibujar un icono elevado, o bien **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ae279-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae279-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae279-113">Return value</span></span>

<span data-ttu-id="ae279-114">Devuelve 1 si se realiza correctamente, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ae279-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae279-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae279-115">Remarks</span></span>

<span data-ttu-id="ae279-116">Una aplicación debe manifestarse para usar comctl32.dll versión 6 para obtener esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ae279-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae279-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae279-117">Requirements</span></span>



| <span data-ttu-id="ae279-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae279-118">Requirement</span></span> | <span data-ttu-id="ae279-119">Value</span><span class="sxs-lookup"><span data-stu-id="ae279-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae279-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae279-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae279-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ae279-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae279-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae279-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae279-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae279-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae279-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae279-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae279-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae279-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





