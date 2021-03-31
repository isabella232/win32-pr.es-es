---
title: Mensaje de TDM_CLICK_VERIFICATION (commctrl. h)
description: Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149879"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="cf911-104">TDM- \_ hacer clic en \_ mensaje de comprobación</span><span class="sxs-lookup"><span data-stu-id="cf911-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="cf911-105">Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.</span><span class="sxs-lookup"><span data-stu-id="cf911-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf911-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf911-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf911-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf911-108">**True** para establecer el estado de la casilla que se va a comprobar; **False** para establecer que esté desactivada.</span><span class="sxs-lookup"><span data-stu-id="cf911-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="cf911-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf911-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf911-110">**True** para establecer el foco de teclado en la casilla; De lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="cf911-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf911-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf911-111">Return value</span></span>

<span data-ttu-id="cf911-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cf911-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf911-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf911-113">Requirements</span></span>



| <span data-ttu-id="cf911-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf911-114">Requirement</span></span> | <span data-ttu-id="cf911-115">Value</span><span class="sxs-lookup"><span data-stu-id="cf911-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf911-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf911-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf911-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf911-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf911-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf911-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf911-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf911-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf911-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf911-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf911-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf911-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





