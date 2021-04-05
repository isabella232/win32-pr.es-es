---
title: Código de notificación de HDN_ITEMKEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079757"
---
# <a name="hdn_itemkeydown-notification-code"></a><span data-ttu-id="6c82c-105">Código de notificación de ITEMKEYDOWN de HDN \_</span><span class="sxs-lookup"><span data-stu-id="6c82c-105">HDN\_ITEMKEYDOWN notification code</span></span>

<span data-ttu-id="6c82c-106">Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6c82c-106">Notifies a header control's parent window that a key has been pressed with an item selected.</span></span> <span data-ttu-id="6c82c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6c82c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c82c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c82c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c82c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c82c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c82c-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="6c82c-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c82c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c82c-111">Return value</span></span>

<span data-ttu-id="6c82c-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6c82c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c82c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c82c-113">Requirements</span></span>



| <span data-ttu-id="6c82c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c82c-114">Requirement</span></span> | <span data-ttu-id="6c82c-115">Value</span><span class="sxs-lookup"><span data-stu-id="6c82c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c82c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c82c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c82c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6c82c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c82c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c82c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c82c-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c82c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c82c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c82c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c82c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c82c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





