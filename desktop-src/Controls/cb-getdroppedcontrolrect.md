---
title: Mensaje de CB_GETDROPPEDCONTROLRECT (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETDROPPEDCONTROLRECT para recuperar las coordenadas de pantalla de un cuadro combinado en su estado desplegable.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491225"
---
# <a name="cb_getdroppedcontrolrect-message"></a><span data-ttu-id="79926-104">\_Mensaje GETDROPPEDCONTROLRECT CB</span><span class="sxs-lookup"><span data-stu-id="79926-104">CB\_GETDROPPEDCONTROLRECT message</span></span>

<span data-ttu-id="79926-105">Una aplicación envía un mensaje **CB \_ GETDROPPEDCONTROLRECT** para recuperar las coordenadas de pantalla de un cuadro combinado en su estado desplegable.</span><span class="sxs-lookup"><span data-stu-id="79926-105">An application sends a **CB\_GETDROPPEDCONTROLRECT** message to retrieve the screen coordinates of a combo box in its dropped-down state.</span></span>

## <a name="parameters"></a><span data-ttu-id="79926-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79926-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79926-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79926-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="79926-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79926-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79926-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79926-110">Puntero a la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas del cuadro combinado en su estado desplegable.</span><span class="sxs-lookup"><span data-stu-id="79926-110">A pointer to the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the coordinates of the combo box in its dropped-down state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79926-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79926-111">Return value</span></span>

<span data-ttu-id="79926-112">Si el mensaje se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="79926-112">If the message succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="79926-113">Si se produce un error en el mensaje, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="79926-113">If the message fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="79926-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79926-114">Requirements</span></span>



| <span data-ttu-id="79926-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79926-115">Requirement</span></span> | <span data-ttu-id="79926-116">Value</span><span class="sxs-lookup"><span data-stu-id="79926-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79926-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79926-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79926-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="79926-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79926-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79926-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79926-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="79926-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79926-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79926-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79926-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79926-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79926-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="79926-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="79926-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79926-124">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

