---
description: Le notifica que el menú se contrae.
title: Mensaje de SMC_EXITMENU (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002298"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="d45aa-103">Mensaje de EXITMENU de SMC \_</span><span class="sxs-lookup"><span data-stu-id="d45aa-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="d45aa-104">Le notifica que el menú se contrae.</span><span class="sxs-lookup"><span data-stu-id="d45aa-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="d45aa-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d45aa-105">Parameters</span></span>

<span data-ttu-id="d45aa-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d45aa-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d45aa-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d45aa-107">Return value</span></span>

<span data-ttu-id="d45aa-108">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d45aa-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d45aa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d45aa-109">Remarks</span></span>

<span data-ttu-id="d45aa-110">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="d45aa-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45aa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d45aa-111">Requirements</span></span>



| <span data-ttu-id="d45aa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d45aa-112">Requirement</span></span> | <span data-ttu-id="d45aa-113">Value</span><span class="sxs-lookup"><span data-stu-id="d45aa-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d45aa-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d45aa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d45aa-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d45aa-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d45aa-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d45aa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d45aa-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d45aa-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d45aa-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d45aa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d45aa-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d45aa-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d45aa-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d45aa-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d45aa-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d45aa-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




