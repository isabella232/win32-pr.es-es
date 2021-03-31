---
title: Código de notificación de NM_TVSTATEIMAGECHANGING (commctrl. h)
description: Enviado por un control de vista de árbol a su ventana primaria que cambia la imagen de estado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150125"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="42ab7-105">Código de notificación de NM \_ TVSTATEIMAGECHANGING</span><span class="sxs-lookup"><span data-stu-id="42ab7-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="42ab7-106">Enviado por un control de vista de árbol a su ventana primaria que cambia la imagen de estado.</span><span class="sxs-lookup"><span data-stu-id="42ab7-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="42ab7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42ab7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="42ab7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42ab7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ab7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42ab7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42ab7-110">Puntero a una estructura [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="42ab7-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42ab7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42ab7-111">Return value</span></span>

<span data-ttu-id="42ab7-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="42ab7-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ab7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ab7-113">Requirements</span></span>



| <span data-ttu-id="42ab7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ab7-114">Requirement</span></span> | <span data-ttu-id="42ab7-115">Value</span><span class="sxs-lookup"><span data-stu-id="42ab7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42ab7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42ab7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42ab7-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42ab7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42ab7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42ab7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42ab7-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42ab7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42ab7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42ab7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42ab7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ab7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





