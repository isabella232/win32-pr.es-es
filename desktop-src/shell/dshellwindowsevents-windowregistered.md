---
description: Se llama cuando se registra una ventana como una ventana de Shell.
title: DShellWindowsEvents.WindowRegistered (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 64bf83a88584c5d97994726696d4fb3a1e971bdf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841456"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="13943-103">DShellWindowsEvents.WindowRegistered (método)</span><span class="sxs-lookup"><span data-stu-id="13943-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="13943-104">Se llama cuando se registra una ventana como una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="13943-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="13943-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13943-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="13943-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13943-107">*lCookie* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13943-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13943-108">Tipo: **Entero**</span><span class="sxs-lookup"><span data-stu-id="13943-108">Type: **Integer**</span></span>

<span data-ttu-id="13943-109">Cookie que identifica la ventana que se registró.</span><span class="sxs-lookup"><span data-stu-id="13943-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13943-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13943-110">Return value</span></span>

<span data-ttu-id="13943-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13943-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13943-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13943-112">Remarks</span></span>

<span data-ttu-id="13943-113">A una ventana se le concede una cookie cuando se registra como una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="13943-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="13943-114">Para obtener más información, vea [**Registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="13943-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="13943-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13943-115">Requirements</span></span>



| <span data-ttu-id="13943-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13943-116">Requirement</span></span> | <span data-ttu-id="13943-117">Value</span><span class="sxs-lookup"><span data-stu-id="13943-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13943-118">Producto</span><span class="sxs-lookup"><span data-stu-id="13943-118">Product</span></span><br/> | <span data-ttu-id="13943-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="13943-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="13943-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13943-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="13943-121"><dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="13943-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13943-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13943-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13943-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="13943-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="13943-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="13943-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="13943-125">**Register**</span><span class="sxs-lookup"><span data-stu-id="13943-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="13943-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="13943-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




