---
title: Código de notificación de RBN_HEIGHTCHANGE (commctrl. h)
description: Se envía por un control Rebar cuando su alto ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996330"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="92fb0-105">Código de notificación de HEIGHTCHANGE de RBN \_</span><span class="sxs-lookup"><span data-stu-id="92fb0-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="92fb0-106">Se envía por un control Rebar cuando su alto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="92fb0-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="92fb0-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="92fb0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="92fb0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92fb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fb0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92fb0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92fb0-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="92fb0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fb0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92fb0-111">Return value</span></span>

<span data-ttu-id="92fb0-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="92fb0-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="92fb0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92fb0-113">Remarks</span></span>

<span data-ttu-id="92fb0-114">Los controles Rebar que usan el estilo [**CCS \_ Vert**](common-control-styles.md) envían este código de notificación cuando cambia el ancho.</span><span class="sxs-lookup"><span data-stu-id="92fb0-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="92fb0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92fb0-115">Requirements</span></span>



| <span data-ttu-id="92fb0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92fb0-116">Requirement</span></span> | <span data-ttu-id="92fb0-117">Value</span><span class="sxs-lookup"><span data-stu-id="92fb0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92fb0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92fb0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92fb0-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92fb0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92fb0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92fb0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92fb0-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="92fb0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92fb0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92fb0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="92fb0-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92fb0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





