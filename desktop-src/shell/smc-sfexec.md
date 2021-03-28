---
description: Ejecute el elemento de carpeta de Shell especificado en la estructura SMDATA correspondiente.
title: Mensaje de SMC_SFEXEC (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985731"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="f212c-103">Mensaje de SFEXEC de SMC \_</span><span class="sxs-lookup"><span data-stu-id="f212c-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="f212c-104">Ejecute el elemento de carpeta de Shell especificado en la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f212c-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="f212c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f212c-105">Parameters</span></span>

<span data-ttu-id="f212c-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f212c-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f212c-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f212c-107">Return value</span></span>

<span data-ttu-id="f212c-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="f212c-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f212c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f212c-109">Remarks</span></span>

<span data-ttu-id="f212c-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="f212c-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f212c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f212c-111">Requirements</span></span>



| <span data-ttu-id="f212c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f212c-112">Requirement</span></span> | <span data-ttu-id="f212c-113">Value</span><span class="sxs-lookup"><span data-stu-id="f212c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f212c-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f212c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f212c-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f212c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f212c-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f212c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f212c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f212c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f212c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f212c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f212c-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f212c-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f212c-120">IDL</span><span class="sxs-lookup"><span data-stu-id="f212c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f212c-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f212c-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




