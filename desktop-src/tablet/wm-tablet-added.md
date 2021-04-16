---
description: El mensaje de la tableta de WM \_ \_ agregada se envía cuando se agrega un dispositivo de tableta a Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Mensaje de WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696331"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="8653f-103">\_Mensaje agregado a Tablet PC de WM \_</span><span class="sxs-lookup"><span data-stu-id="8653f-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="8653f-104">El mensaje de la **tableta de WM \_ \_ agregada** se envía cuando se agrega un dispositivo de tableta a Windows.</span><span class="sxs-lookup"><span data-stu-id="8653f-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="8653f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8653f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8653f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8653f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8653f-107">Índice del dispositivo de tableta gráfica que se va a agregar</span><span class="sxs-lookup"><span data-stu-id="8653f-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="8653f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8653f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8653f-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="8653f-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8653f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8653f-110">Remarks</span></span>

<span data-ttu-id="8653f-111">Este mensaje se envía a todas las ventanas de nivel superior del sistema, incluidas las ventanas sin propietario deshabilitadas o invisibles, las ventanas superpuestas y las ventanas emergentes. pero el mensaje no se envía a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="8653f-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="8653f-112">Los índices pasados en *wParam* están relacionados con el índice utilizado por el método [**ITabletManager:: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8653f-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8653f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8653f-113">Requirements</span></span>



| <span data-ttu-id="8653f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8653f-114">Requirement</span></span> | <span data-ttu-id="8653f-115">Value</span><span class="sxs-lookup"><span data-stu-id="8653f-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8653f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8653f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8653f-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8653f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8653f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8653f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8653f-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8653f-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="8653f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8653f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8653f-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="8653f-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
