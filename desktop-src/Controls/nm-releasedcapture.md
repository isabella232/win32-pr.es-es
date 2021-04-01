---
title: Código de notificación de NM_RELEASEDCAPTURE (commctrl. h)
description: Notifica a la ventana primaria de un control que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 222a3be1-20f1-43c6-b982-852512209a45
keywords:
- NM_RELEASEDCAPTURE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1510fd3bbdd6877dba279cbfb9c69c14146a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996817"
---
# <a name="nm_releasedcapture-notification-code"></a><span data-ttu-id="70e40-105">Código de notificación de NM \_ RELEASEDCAPTURE</span><span class="sxs-lookup"><span data-stu-id="70e40-105">NM\_RELEASEDCAPTURE notification code</span></span>

<span data-ttu-id="70e40-106">Notifica a la ventana primaria de un control que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="70e40-106">Notifies a control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="70e40-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="70e40-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="70e40-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70e40-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70e40-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="70e40-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e40-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70e40-111">Return value</span></span>

<span data-ttu-id="70e40-112">A menos que se especifique lo contrario, el control omite el valor devuelto de este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="70e40-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e40-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70e40-113">Requirements</span></span>



| <span data-ttu-id="70e40-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e40-114">Requirement</span></span> | <span data-ttu-id="70e40-115">Value</span><span class="sxs-lookup"><span data-stu-id="70e40-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70e40-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70e40-116">Minimum supported client</span></span><br/> | <span data-ttu-id="70e40-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70e40-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70e40-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70e40-118">Minimum supported server</span></span><br/> | <span data-ttu-id="70e40-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70e40-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70e40-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70e40-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e40-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e40-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





