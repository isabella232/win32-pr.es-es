---
description: Solicita si es aceptable quitar un objeto de datos en el elemento especificado por la estructura SMDATA adjunta.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Mensaje de SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985734"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="2f7ad-103">Mensaje de SFDDRESTRICTED de SMC \_</span><span class="sxs-lookup"><span data-stu-id="2f7ad-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="2f7ad-104">Solicita si es aceptable quitar un objeto de datos en el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.</span><span class="sxs-lookup"><span data-stu-id="2f7ad-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="2f7ad-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f7ad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7ad-106">*pDropTarget*</span><span class="sxs-lookup"><span data-stu-id="2f7ad-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="2f7ad-107">Dirección de un puntero void que recibe un puntero a la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="2f7ad-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="2f7ad-108">Establezca este valor en **null** si no desea aceptar el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="2f7ad-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7ad-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f7ad-109">Return value</span></span>

<span data-ttu-id="2f7ad-110">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2f7ad-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7ad-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f7ad-111">Remarks</span></span>

<span data-ttu-id="2f7ad-112">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="2f7ad-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7ad-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7ad-113">Requirements</span></span>



| <span data-ttu-id="2f7ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7ad-114">Requirement</span></span> | <span data-ttu-id="2f7ad-115">Value</span><span class="sxs-lookup"><span data-stu-id="2f7ad-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7ad-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7ad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7ad-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f7ad-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f7ad-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7ad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7ad-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f7ad-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f7ad-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f7ad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7ad-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ad-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f7ad-122">IDL</span><span class="sxs-lookup"><span data-stu-id="2f7ad-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f7ad-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ad-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
