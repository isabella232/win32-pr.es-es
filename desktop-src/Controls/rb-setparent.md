---
title: Mensaje de RB_SETPARENT (commctrl. h)
description: Establece la ventana primaria de un control rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- RB_SETPARENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905417"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="4cef9-104">Mensaje de el SETPARENT de RB \_</span><span class="sxs-lookup"><span data-stu-id="4cef9-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="4cef9-105">Establece la ventana primaria de un control rebar.</span><span class="sxs-lookup"><span data-stu-id="4cef9-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cef9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cef9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cef9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cef9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cef9-108">Identificador de la ventana primaria que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="4cef9-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="4cef9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cef9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4cef9-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4cef9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cef9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cef9-111">Return value</span></span>

<span data-ttu-id="4cef9-112">Devuelve el identificador de la ventana primaria anterior o **null** si no hay ningún elemento primario anterior.</span><span class="sxs-lookup"><span data-stu-id="4cef9-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cef9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cef9-113">Remarks</span></span>

<span data-ttu-id="4cef9-114">El control rebar envía mensajes de notificación a la ventana que se especifica con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4cef9-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="4cef9-115">En realidad, este mensaje no cambia el elemento primario del control rebar.</span><span class="sxs-lookup"><span data-stu-id="4cef9-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cef9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cef9-116">Requirements</span></span>



| <span data-ttu-id="4cef9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cef9-117">Requirement</span></span> | <span data-ttu-id="4cef9-118">Value</span><span class="sxs-lookup"><span data-stu-id="4cef9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cef9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cef9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cef9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4cef9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cef9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cef9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cef9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4cef9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cef9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cef9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cef9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cef9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





