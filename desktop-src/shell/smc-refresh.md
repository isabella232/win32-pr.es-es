---
description: Envía una notificación de que los menús se han actualizado por completo y se puede restablecer su estado.
title: Mensaje de SMC_REFRESH (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911157"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="5066f-103">Mensaje de actualización de SMC \_</span><span class="sxs-lookup"><span data-stu-id="5066f-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="5066f-104">Envía una notificación de que los menús se han actualizado por completo y se puede restablecer su estado.</span><span class="sxs-lookup"><span data-stu-id="5066f-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="5066f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5066f-105">Parameters</span></span>

<span data-ttu-id="5066f-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5066f-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5066f-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5066f-107">Return value</span></span>

<span data-ttu-id="5066f-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5066f-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5066f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5066f-109">Remarks</span></span>

<span data-ttu-id="5066f-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="5066f-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5066f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5066f-111">Requirements</span></span>



| <span data-ttu-id="5066f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5066f-112">Requirement</span></span> | <span data-ttu-id="5066f-113">Value</span><span class="sxs-lookup"><span data-stu-id="5066f-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5066f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5066f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5066f-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5066f-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5066f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5066f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5066f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5066f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5066f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5066f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5066f-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5066f-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="5066f-120">IDL</span><span class="sxs-lookup"><span data-stu-id="5066f-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5066f-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5066f-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




