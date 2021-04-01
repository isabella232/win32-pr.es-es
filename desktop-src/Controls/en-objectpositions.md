---
title: Código de notificación de EN_OBJECTPOSITIONS (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit cuando el control Lee objetos. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905297"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="ab92a-105">\_Código de notificación en OBJECTPOSITIONS</span><span class="sxs-lookup"><span data-stu-id="ab92a-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="ab92a-106">Notifica a la ventana primaria de un control Rich Edit cuando el control Lee objetos.</span><span class="sxs-lookup"><span data-stu-id="ab92a-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="ab92a-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ab92a-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ab92a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab92a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab92a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab92a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab92a-110">Estructura [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .</span><span class="sxs-lookup"><span data-stu-id="ab92a-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab92a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab92a-111">Return value</span></span>

<span data-ttu-id="ab92a-112">Devuelve cero para continuar con la operación de **lectura** .</span><span class="sxs-lookup"><span data-stu-id="ab92a-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="ab92a-113">Devuelve un valor distinto de cero para detener la operación de **lectura** .</span><span class="sxs-lookup"><span data-stu-id="ab92a-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab92a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab92a-114">Remarks</span></span>

<span data-ttu-id="ab92a-115">Para recibir un \_ código de notificación en OBJECTPOSITIONS, especifique la marca [**\_ OBJECTPOSITIONS de ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ab92a-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab92a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab92a-116">Requirements</span></span>



| <span data-ttu-id="ab92a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab92a-117">Requirement</span></span> | <span data-ttu-id="ab92a-118">Value</span><span class="sxs-lookup"><span data-stu-id="ab92a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab92a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab92a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab92a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ab92a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab92a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab92a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab92a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab92a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab92a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab92a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab92a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab92a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab92a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab92a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab92a-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ab92a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab92a-127">**una \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="ab92a-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="ab92a-128">**OBJECTPOSITIONS**</span><span class="sxs-lookup"><span data-stu-id="ab92a-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="ab92a-129">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="ab92a-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="ab92a-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ab92a-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ab92a-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab92a-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ab92a-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab92a-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

