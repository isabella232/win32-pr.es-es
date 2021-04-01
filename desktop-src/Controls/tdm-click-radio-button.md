---
title: Mensaje de TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simula la acción de un clic de botón de radio en un cuadro de diálogo de tarea.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997023"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="f749d-104">\_Mensaje de \_ botón de radio haga clic en TDM \_</span><span class="sxs-lookup"><span data-stu-id="f749d-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="f749d-105">Simula la acción de un clic de botón de radio en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="f749d-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="f749d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f749d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f749d-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f749d-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f749d-108">Valor **int** que especifica el identificador del botón de radio en el que se va a hacer clic.</span><span class="sxs-lookup"><span data-stu-id="f749d-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="f749d-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f749d-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f749d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f749d-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f749d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f749d-111">Return value</span></span>

<span data-ttu-id="f749d-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f749d-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f749d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f749d-113">Remarks</span></span>

<span data-ttu-id="f749d-114">El identificador de botón de radio especificado se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte del código de notificación de un [clic del \_ \_ botón \_ de radio TDN](tdn-radio-button-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="f749d-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="f749d-115">Después de que la función de devolución de llamada vuelva, se seleccionará el botón de radio.</span><span class="sxs-lookup"><span data-stu-id="f749d-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f749d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f749d-116">Requirements</span></span>



| <span data-ttu-id="f749d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f749d-117">Requirement</span></span> | <span data-ttu-id="f749d-118">Value</span><span class="sxs-lookup"><span data-stu-id="f749d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f749d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f749d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f749d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f749d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f749d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f749d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f749d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f749d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f749d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f749d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f749d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f749d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

