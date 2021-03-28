---
description: Disminuir de nivel el elemento especificado por la estructura SMDATA adjunta.
title: Mensaje de SMC_DEMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997796"
---
# <a name="smc_demote-message"></a><span data-ttu-id="fca86-103">Desdegradar el mensaje de SMC \_</span><span class="sxs-lookup"><span data-stu-id="fca86-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="fca86-104">Disminuir de nivel el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.</span><span class="sxs-lookup"><span data-stu-id="fca86-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="fca86-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fca86-105">Parameters</span></span>

<span data-ttu-id="fca86-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fca86-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fca86-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fca86-107">Return value</span></span>

<span data-ttu-id="fca86-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="fca86-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fca86-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fca86-109">Remarks</span></span>

<span data-ttu-id="fca86-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="fca86-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca86-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fca86-111">Requirements</span></span>



| <span data-ttu-id="fca86-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca86-112">Requirement</span></span> | <span data-ttu-id="fca86-113">Value</span><span class="sxs-lookup"><span data-stu-id="fca86-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fca86-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fca86-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fca86-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fca86-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fca86-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fca86-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fca86-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fca86-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fca86-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fca86-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fca86-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca86-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="fca86-120">IDL</span><span class="sxs-lookup"><span data-stu-id="fca86-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fca86-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fca86-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




