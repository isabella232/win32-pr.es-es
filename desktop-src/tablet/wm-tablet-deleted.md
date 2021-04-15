---
description: El mensaje de la \_ tableta \_ de WM eliminada se envía cuando se quita un dispositivo de tableta gráfica de Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Mensaje de WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696330"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="e570d-103">\_Mensaje eliminado de Tablet PC de WM \_</span><span class="sxs-lookup"><span data-stu-id="e570d-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="e570d-104">El mensaje de la **tableta de WM \_ \_ eliminada** se envía cuando se quita un dispositivo de tableta gráfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="e570d-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="e570d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e570d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e570d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e570d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e570d-107">Índice del dispositivo de tableta gráfica que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="e570d-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="e570d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e570d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e570d-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e570d-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e570d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e570d-110">Remarks</span></span>

<span data-ttu-id="e570d-111">Este mensaje se envía a todas las ventanas de nivel superior del sistema, incluidas las ventanas sin propietario deshabilitadas o invisibles, las ventanas superpuestas y las ventanas emergentes. pero el mensaje no se envía a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="e570d-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="e570d-112">Los índices pasados en *wParam* están relacionados con el índice utilizado por el método [**ITabletManager:: GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e570d-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e570d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e570d-113">Requirements</span></span>



| <span data-ttu-id="e570d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e570d-114">Requirement</span></span> | <span data-ttu-id="e570d-115">Value</span><span class="sxs-lookup"><span data-stu-id="e570d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e570d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e570d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e570d-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e570d-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="e570d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e570d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e570d-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e570d-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e570d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e570d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e570d-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="e570d-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
