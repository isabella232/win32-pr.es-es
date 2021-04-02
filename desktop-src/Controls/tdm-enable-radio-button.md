---
title: Mensaje de TDM_ENABLE_RADIO_BUTTON (commctrl. h)
description: Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997022"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="fb1e3-104">\_Mensaje de \_ botón de radio habilitar TDM \_</span><span class="sxs-lookup"><span data-stu-id="fb1e3-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="fb1e3-105">Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb1e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1e3-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb1e3-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1e3-108">Valor **int** que especifica el identificador del botón de radio que se va a habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="fb1e3-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb1e3-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1e3-110">Especifica el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-110">Specifies button state.</span></span> <span data-ttu-id="fb1e3-111">Establézcalo en 0 para deshabilitar el botón; se establece en un valor distinto de cero para habilitar el botón.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1e3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb1e3-112">Return value</span></span>

<span data-ttu-id="fb1e3-113">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1e3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1e3-114">Requirements</span></span>



| <span data-ttu-id="fb1e3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1e3-115">Requirement</span></span> | <span data-ttu-id="fb1e3-116">Value</span><span class="sxs-lookup"><span data-stu-id="fb1e3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1e3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1e3-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb1e3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb1e3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1e3-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb1e3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb1e3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb1e3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb1e3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1e3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





