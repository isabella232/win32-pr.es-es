---
title: Código de notificación de HDN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905032"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="d7a7e-105">Código de notificación de ITEMCHANGING de HDN \_</span><span class="sxs-lookup"><span data-stu-id="d7a7e-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="d7a7e-106">Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="d7a7e-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="d7a7e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a7e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d7a7e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7a7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7a7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a7e-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento de encabezado, incluidos los atributos que están a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="d7a7e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a7e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7a7e-111">Return value</span></span>

<span data-ttu-id="d7a7e-112">Devuelve **false** para permitir los cambios o **true** para evitarlos.</span><span class="sxs-lookup"><span data-stu-id="d7a7e-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a7e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a7e-113">Requirements</span></span>



| <span data-ttu-id="d7a7e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a7e-114">Requirement</span></span> | <span data-ttu-id="d7a7e-115">Value</span><span class="sxs-lookup"><span data-stu-id="d7a7e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a7e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a7e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a7e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a7e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7a7e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a7e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a7e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a7e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7a7e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7a7e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a7e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a7e-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d7a7e-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d7a7e-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d7a7e-123">**HDN \_ ITEMCHANGINGW** (Unicode) y **HDN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d7a7e-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 





