---
title: Mensaje de TDM_CLICK_BUTTON (commctrl. h)
description: Simula la acción de un clic de botón en un cuadro de diálogo de tarea.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658195"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="d2a6d-104">Mensaje de botón de \_ clic de TDM \_</span><span class="sxs-lookup"><span data-stu-id="d2a6d-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="d2a6d-105">Simula la acción de un clic de botón en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2a6d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a6d-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2a6d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a6d-108">Valor **int** que especifica el identificador del botón en el que se va a hacer clic.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="d2a6d-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2a6d-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a6d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a6d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2a6d-111">Return value</span></span>

<span data-ttu-id="d2a6d-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a6d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2a6d-113">Remarks</span></span>

<span data-ttu-id="d2a6d-114">El identificador de botón especificado por *wParam* se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte del código de notificación en el que se [ \_ \_ hizo clic en un botón TDN](tdn-button-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a6d-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="d2a6d-115">Después de que la función de devolución de llamada se devuelva, el cuadro de diálogo de tarea se cierra si \_ se devolvió S OK desde la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="d2a6d-116">Si \_ se devolvió S false desde la función de devolución de llamada, el cuadro de diálogo de tarea permanece activo.</span><span class="sxs-lookup"><span data-stu-id="d2a6d-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a6d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a6d-117">Requirements</span></span>



| <span data-ttu-id="d2a6d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a6d-118">Requirement</span></span> | <span data-ttu-id="d2a6d-119">Value</span><span class="sxs-lookup"><span data-stu-id="d2a6d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a6d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a6d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a6d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d2a6d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2a6d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a6d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a6d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2a6d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2a6d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2a6d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a6d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a6d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

