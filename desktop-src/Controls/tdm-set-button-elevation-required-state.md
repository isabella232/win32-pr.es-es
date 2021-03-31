---
title: Mensaje de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Especifica si un botón de cuadro de diálogo de tarea o vínculo de comando determinado debe tener un icono de escudo de control de cuentas de usuario (UAC). es decir, si la acción invocada por el botón requiere elevación.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151050"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="6fc29-104">\_Mensaje de \_ \_ Estado de elevación \_ requerida del botón \_ de configuración de TDM</span><span class="sxs-lookup"><span data-stu-id="6fc29-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="6fc29-105">Especifica si un botón de cuadro de diálogo de tarea o vínculo de comando determinado debe tener un icono de escudo de control de cuentas de usuario (UAC). es decir, si la acción invocada por el botón requiere elevación.</span><span class="sxs-lookup"><span data-stu-id="6fc29-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fc29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fc29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc29-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6fc29-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc29-108">IDENTIFICADOR del botón de comando o vínculo de comando que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="6fc29-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6fc29-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6fc29-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc29-110">Establézcalo en 0 para indicar que la acción invocada por el botón no requiere elevación.</span><span class="sxs-lookup"><span data-stu-id="6fc29-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="6fc29-111">Se establece en un valor distinto de cero para indicar que la acción requiere elevación.</span><span class="sxs-lookup"><span data-stu-id="6fc29-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc29-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fc29-112">Return value</span></span>

<span data-ttu-id="6fc29-113">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6fc29-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc29-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc29-114">Requirements</span></span>



| <span data-ttu-id="6fc29-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc29-115">Requirement</span></span> | <span data-ttu-id="6fc29-116">Value</span><span class="sxs-lookup"><span data-stu-id="6fc29-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc29-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc29-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc29-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6fc29-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fc29-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc29-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc29-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6fc29-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fc29-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fc29-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc29-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc29-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





