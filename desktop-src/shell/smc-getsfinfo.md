---
description: Solicita información sobre un elemento de menú de la carpeta de Shell.
title: Mensaje de SMC_GETSFINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997785"
---
# <a name="smc_getsfinfo-message"></a><span data-ttu-id="68e6d-103">Mensaje de GETSFINFO de SMC \_</span><span class="sxs-lookup"><span data-stu-id="68e6d-103">SMC\_GETSFINFO message</span></span>

<span data-ttu-id="68e6d-104">Solicita información sobre un elemento de menú de la carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="68e6d-104">Requests information about a Shell folder menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="68e6d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68e6d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e6d-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="68e6d-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="68e6d-107">Puntero a una estructura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="68e6d-107">Pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="68e6d-108">Rellene la estructura con la información adecuada y vuelva a \_ Aceptar.</span><span class="sxs-lookup"><span data-stu-id="68e6d-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e6d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68e6d-109">Return value</span></span>

<span data-ttu-id="68e6d-110">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="68e6d-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e6d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68e6d-111">Remarks</span></span>

<span data-ttu-id="68e6d-112">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="68e6d-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e6d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e6d-113">Requirements</span></span>



| <span data-ttu-id="68e6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e6d-114">Requirement</span></span> | <span data-ttu-id="68e6d-115">Value</span><span class="sxs-lookup"><span data-stu-id="68e6d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e6d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="68e6d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68e6d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68e6d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="68e6d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68e6d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68e6d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68e6d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="68e6d-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e6d-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="68e6d-122">IDL</span><span class="sxs-lookup"><span data-stu-id="68e6d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68e6d-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68e6d-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




