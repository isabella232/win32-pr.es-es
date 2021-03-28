---
description: Promocionar el elemento especificado por la estructura SMDATA adjunta.
title: Mensaje de SMC_PROMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985735"
---
# <a name="smc_promote-message"></a><span data-ttu-id="aa3aa-103">Mensaje de promoción de SMC \_</span><span class="sxs-lookup"><span data-stu-id="aa3aa-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="aa3aa-104">Promocionar el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.</span><span class="sxs-lookup"><span data-stu-id="aa3aa-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="aa3aa-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa3aa-105">Parameters</span></span>

<span data-ttu-id="aa3aa-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="aa3aa-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa3aa-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa3aa-107">Return value</span></span>

<span data-ttu-id="aa3aa-108">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="aa3aa-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa3aa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa3aa-109">Remarks</span></span>

<span data-ttu-id="aa3aa-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="aa3aa-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3aa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa3aa-111">Requirements</span></span>



| <span data-ttu-id="aa3aa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa3aa-112">Requirement</span></span> | <span data-ttu-id="aa3aa-113">Value</span><span class="sxs-lookup"><span data-stu-id="aa3aa-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3aa-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3aa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aa3aa-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa3aa-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aa3aa-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3aa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aa3aa-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa3aa-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa3aa-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa3aa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa3aa-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa3aa-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa3aa-120">IDL</span><span class="sxs-lookup"><span data-stu-id="aa3aa-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa3aa-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa3aa-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




