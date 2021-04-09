---
title: Código de notificación de BCN_HOTITEMCHANGE (commctrl. h)
description: Notifica al propietario del control de botón que el mouse está entrando o saliendo del área cliente del control de botón. El control de botón envía este código de notificación en forma de mensaje de notificación de WM \_ .
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079212"
---
# <a name="bcn_hotitemchange-notification-code"></a><span data-ttu-id="825ed-105">Código de notificación de HOTITEMCHANGE de BCN \_</span><span class="sxs-lookup"><span data-stu-id="825ed-105">BCN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="825ed-106">Notifica al propietario del control de botón que el mouse está entrando o saliendo del área cliente del control de botón.</span><span class="sxs-lookup"><span data-stu-id="825ed-106">Notifies the button control owner that the mouse is entering or leaving the client area of the button control.</span></span> <span data-ttu-id="825ed-107">El control de botón envía este código de notificación en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="825ed-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="825ed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="825ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="825ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="825ed-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="825ed-110">Puntero a una estructura [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) .</span><span class="sxs-lookup"><span data-stu-id="825ed-110">A pointer to a [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="825ed-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="825ed-111">Return value</span></span>

<span data-ttu-id="825ed-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="825ed-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="825ed-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="825ed-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="825ed-114">Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="825ed-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="825ed-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="825ed-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="825ed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="825ed-116">Requirements</span></span>



| <span data-ttu-id="825ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="825ed-117">Requirement</span></span> | <span data-ttu-id="825ed-118">Value</span><span class="sxs-lookup"><span data-stu-id="825ed-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="825ed-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="825ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="825ed-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="825ed-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="825ed-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="825ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="825ed-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="825ed-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="825ed-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="825ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="825ed-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="825ed-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





