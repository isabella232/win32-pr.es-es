---
description: Solicita información sobre un elemento de menú normal.
title: Mensaje de SMC_GETINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f60c1581ae7c4585de48eea943cc23b4d87fa4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997788"
---
# <a name="smc_getinfo-message"></a><span data-ttu-id="d2c39-103">\_Mensaje GetInfo de SMC</span><span class="sxs-lookup"><span data-stu-id="d2c39-103">SMC\_GETINFO message</span></span>

<span data-ttu-id="d2c39-104">Solicita información sobre un elemento de menú normal.</span><span class="sxs-lookup"><span data-stu-id="d2c39-104">Requests information about a regular menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="d2c39-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2c39-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c39-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="d2c39-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c39-107">Puntero a una estructura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="d2c39-107">A pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="d2c39-108">Rellene la estructura con la información adecuada y vuelva a \_ Aceptar.</span><span class="sxs-lookup"><span data-stu-id="d2c39-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c39-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2c39-109">Return value</span></span>

<span data-ttu-id="d2c39-110">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d2c39-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c39-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2c39-111">Remarks</span></span>

<span data-ttu-id="d2c39-112">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="d2c39-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c39-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c39-113">Requirements</span></span>



| <span data-ttu-id="d2c39-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c39-114">Requirement</span></span> | <span data-ttu-id="d2c39-115">Value</span><span class="sxs-lookup"><span data-stu-id="d2c39-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c39-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2c39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c39-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2c39-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d2c39-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2c39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c39-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2c39-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2c39-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2c39-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c39-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c39-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2c39-122">IDL</span><span class="sxs-lookup"><span data-stu-id="d2c39-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2c39-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2c39-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




