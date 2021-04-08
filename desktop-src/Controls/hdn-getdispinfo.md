---
title: Código de notificación de HDN_GETDISPINFO (commctrl. h)
description: Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada. Este código de notificación se envía como un mensaje de notificación de WM \_ .
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078945"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="10b4e-105">Código de notificación de GETDISPINFO de HDN \_</span><span class="sxs-lookup"><span data-stu-id="10b4e-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="10b4e-106">Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="10b4e-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="10b4e-107">Este código de notificación se envía como un mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10b4e-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="10b4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10b4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b4e-110">Puntero a una estructura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="10b4e-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="10b4e-111">En la entrada, los campos de la estructura especifican qué información se requiere y el elemento de interés.</span><span class="sxs-lookup"><span data-stu-id="10b4e-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b4e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10b4e-112">Return value</span></span>

<span data-ttu-id="10b4e-113">Devuelve un LRESULT.</span><span class="sxs-lookup"><span data-stu-id="10b4e-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b4e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10b4e-114">Remarks</span></span>

<span data-ttu-id="10b4e-115">Rellene los miembros adecuados de la estructura para devolver la información solicitada al control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="10b4e-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="10b4e-116">Si el controlador de mensajes establece el miembro de **máscara** de la estructura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) en HDI \_ di \_ SETITEM, el control de encabezado almacena la información y no la volverá a solicitar.</span><span class="sxs-lookup"><span data-stu-id="10b4e-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b4e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b4e-117">Requirements</span></span>



| <span data-ttu-id="10b4e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b4e-118">Requirement</span></span> | <span data-ttu-id="10b4e-119">Value</span><span class="sxs-lookup"><span data-stu-id="10b4e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b4e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b4e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10b4e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10b4e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b4e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b4e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10b4e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="10b4e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b4e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10b4e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b4e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b4e-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="10b4e-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="10b4e-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="10b4e-127">**HDN \_ GETDISPINFOW** (Unicode) y **HDN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="10b4e-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





