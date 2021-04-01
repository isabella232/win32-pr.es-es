---
title: Código de notificación de HDN_ENDFILTEREDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que ha finalizado la edición de un filtro. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- HDN_ENDFILTEREDIT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804159"
---
# <a name="hdn_endfilteredit-notification-code"></a><span data-ttu-id="1e4a5-105">Código de notificación de ENDFILTEREDIT de HDN \_</span><span class="sxs-lookup"><span data-stu-id="1e4a5-105">HDN\_ENDFILTEREDIT notification code</span></span>

<span data-ttu-id="1e4a5-106">Notifica a la ventana primaria de un control de encabezado que ha finalizado la edición de un filtro.</span><span class="sxs-lookup"><span data-stu-id="1e4a5-106">Notifies a header control's parent window that a filter edit has ended.</span></span> <span data-ttu-id="1e4a5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4a5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1e4a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e4a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e4a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4a5-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre el filtro que se está editando.</span><span class="sxs-lookup"><span data-stu-id="1e4a5-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e4a5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e4a5-111">Return value</span></span>

<span data-ttu-id="1e4a5-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e4a5-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4a5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e4a5-113">Requirements</span></span>



| <span data-ttu-id="1e4a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4a5-114">Requirement</span></span> | <span data-ttu-id="1e4a5-115">Value</span><span class="sxs-lookup"><span data-stu-id="1e4a5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4a5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4a5-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1e4a5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e4a5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4a5-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e4a5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e4a5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e4a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e4a5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4a5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





