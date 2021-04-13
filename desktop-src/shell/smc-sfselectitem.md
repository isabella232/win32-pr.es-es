---
description: El usuario ha seleccionado el elemento especificado por la estructura SMDATA correspondiente.
title: Mensaje de SMC_SFSELECTITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985563"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="17dfa-103">Mensaje de SFSELECTITEM de SMC \_</span><span class="sxs-lookup"><span data-stu-id="17dfa-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="17dfa-104">El usuario ha seleccionado el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17dfa-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="17dfa-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17dfa-105">Parameters</span></span>

<span data-ttu-id="17dfa-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="17dfa-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17dfa-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dfa-107">Return value</span></span>

<span data-ttu-id="17dfa-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="17dfa-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="17dfa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17dfa-109">Remarks</span></span>

<span data-ttu-id="17dfa-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="17dfa-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17dfa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dfa-111">Requirements</span></span>



| <span data-ttu-id="17dfa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="17dfa-112">Requirement</span></span> | <span data-ttu-id="17dfa-113">Value</span><span class="sxs-lookup"><span data-stu-id="17dfa-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17dfa-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dfa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="17dfa-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="17dfa-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="17dfa-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17dfa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="17dfa-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17dfa-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17dfa-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17dfa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="17dfa-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17dfa-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="17dfa-120">IDL</span><span class="sxs-lookup"><span data-stu-id="17dfa-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17dfa-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17dfa-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




