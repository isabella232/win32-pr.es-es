---
title: Código de notificación de TBN_DRAGOVER (commctrl. h)
description: Determina si \_ se debe enviar un mensaje TB MARKBUTTON para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489796"
---
# <a name="tbn_dragover-notification-code"></a><span data-ttu-id="c07b7-105">\_Código de notificación TBN DRAGOVER</span><span class="sxs-lookup"><span data-stu-id="c07b7-105">TBN\_DRAGOVER notification code</span></span>

<span data-ttu-id="c07b7-106">Determina si se debe enviar un mensaje [**TB \_ MARKBUTTON**](tb-markbutton.md) para un botón que se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="c07b7-106">Ascertains whether a [**TB\_MARKBUTTON**](tb-markbutton.md) message should be sent for a button that is being dragged over.</span></span> <span data-ttu-id="c07b7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c07b7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c07b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c07b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c07b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c07b7-110">Puntero a una estructura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica el elemento sobre el que se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="c07b7-110">A pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that specifies which item is being dragged over.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07b7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c07b7-111">Return value</span></span>

<span data-ttu-id="c07b7-112">**False** si la barra de herramientas debe enviar un \_ mensaje TB MARKBUTTON; de lo contrario, **true**.</span><span class="sxs-lookup"><span data-stu-id="c07b7-112">**FALSE** if the toolbar should send a TB\_MARKBUTTON message; otherwise **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07b7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c07b7-113">Requirements</span></span>



| <span data-ttu-id="c07b7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07b7-114">Requirement</span></span> | <span data-ttu-id="c07b7-115">Value</span><span class="sxs-lookup"><span data-stu-id="c07b7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c07b7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c07b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c07b7-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c07b7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c07b7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c07b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c07b7-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c07b7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c07b7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c07b7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07b7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07b7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





