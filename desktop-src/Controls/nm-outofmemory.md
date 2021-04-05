---
title: Código de notificación de NM_OUTOFMEMORY (commctrl. h)
description: Notifica a la ventana primaria de un control que el control no pudo completar una operación porque no hay suficiente memoria disponible. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078932"
---
# <a name="nm_outofmemory-notification-code"></a><span data-ttu-id="967ec-105">Código de notificación de NM \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="967ec-105">NM\_OUTOFMEMORY notification code</span></span>

<span data-ttu-id="967ec-106">Notifica a la ventana primaria de un control que el control no pudo completar una operación porque no hay suficiente memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="967ec-106">Notifies a control's parent window that the control could not complete an operation because there was not enough memory available.</span></span> <span data-ttu-id="967ec-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="967ec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="967ec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="967ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="967ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="967ec-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="967ec-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967ec-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="967ec-111">Return value</span></span>

<span data-ttu-id="967ec-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="967ec-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="967ec-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="967ec-113">Requirements</span></span>



| <span data-ttu-id="967ec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="967ec-114">Requirement</span></span> | <span data-ttu-id="967ec-115">Value</span><span class="sxs-lookup"><span data-stu-id="967ec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="967ec-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="967ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="967ec-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="967ec-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="967ec-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="967ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="967ec-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="967ec-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="967ec-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="967ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="967ec-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="967ec-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





