---
description: Se llama cuando se revoca el registro de una ventana de Shell.
title: DShellWindowsEvents. WindowRevoked, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987601"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="a8c41-103">DShellWindowsEvents. WindowRevoked, método</span><span class="sxs-lookup"><span data-stu-id="a8c41-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="a8c41-104">Se llama cuando se revoca el registro de una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="a8c41-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8c41-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="a8c41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8c41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c41-107">*lCookie* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8c41-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c41-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="a8c41-108">Type: **Integer**</span></span>

<span data-ttu-id="a8c41-109">Cookie que identifica la ventana que se revocó.</span><span class="sxs-lookup"><span data-stu-id="a8c41-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c41-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8c41-110">Return value</span></span>

<span data-ttu-id="a8c41-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a8c41-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c41-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8c41-112">Remarks</span></span>

<span data-ttu-id="a8c41-113">Se concede una cookie a una ventana cuando se registra como una ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="a8c41-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="a8c41-114">Para obtener más información, consulte [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="a8c41-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c41-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c41-115">Requirements</span></span>



| <span data-ttu-id="a8c41-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c41-116">Requirement</span></span> | <span data-ttu-id="a8c41-117">Value</span><span class="sxs-lookup"><span data-stu-id="a8c41-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c41-118">Producto</span><span class="sxs-lookup"><span data-stu-id="a8c41-118">Product</span></span><br/> | <span data-ttu-id="a8c41-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="a8c41-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="a8c41-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8c41-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8c41-121"><dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a8c41-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c41-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8c41-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c41-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="a8c41-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="a8c41-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="a8c41-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="a8c41-125">**Revocación**</span><span class="sxs-lookup"><span data-stu-id="a8c41-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




