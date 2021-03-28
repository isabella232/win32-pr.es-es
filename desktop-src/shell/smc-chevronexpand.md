---
description: El usuario hizo clic en un botón de contenido adicional para expandir el elemento especificado por la estructura SMDATA correspondiente.
title: Mensaje de SMC_CHEVRONEXPAND (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277636"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="9282e-103">Mensaje de CHEVRONEXPAND de SMC \_</span><span class="sxs-lookup"><span data-stu-id="9282e-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="9282e-104">El usuario hizo clic en un botón de contenido adicional para expandir el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9282e-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="9282e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9282e-105">Parameters</span></span>

<span data-ttu-id="9282e-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9282e-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9282e-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9282e-107">Return value</span></span>

<span data-ttu-id="9282e-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="9282e-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9282e-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9282e-109">Remarks</span></span>

<span data-ttu-id="9282e-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="9282e-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9282e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9282e-111">Requirements</span></span>



| <span data-ttu-id="9282e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9282e-112">Requirement</span></span> | <span data-ttu-id="9282e-113">Value</span><span class="sxs-lookup"><span data-stu-id="9282e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9282e-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9282e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9282e-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9282e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9282e-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9282e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9282e-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9282e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9282e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9282e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9282e-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9282e-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="9282e-120">IDL</span><span class="sxs-lookup"><span data-stu-id="9282e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9282e-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9282e-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




