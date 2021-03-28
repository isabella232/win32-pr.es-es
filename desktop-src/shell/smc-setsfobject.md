---
description: Le notifica que guarde el objeto que se ha pasado.
title: Mensaje de SMC_SETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277630"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="52286-103">Mensaje de SETSFOBJECT de SMC \_</span><span class="sxs-lookup"><span data-stu-id="52286-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="52286-104">Le notifica que guarde el objeto que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="52286-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="52286-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52286-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52286-106">*suscripto*</span><span class="sxs-lookup"><span data-stu-id="52286-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="52286-107">IID asociado al objeto.</span><span class="sxs-lookup"><span data-stu-id="52286-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="52286-108">*FV*</span><span class="sxs-lookup"><span data-stu-id="52286-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="52286-109">Puntero a la interfaz en el objeto especificado por *IID*.</span><span class="sxs-lookup"><span data-stu-id="52286-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52286-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52286-110">Return value</span></span>

<span data-ttu-id="52286-111">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="52286-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="52286-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52286-112">Remarks</span></span>

<span data-ttu-id="52286-113">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="52286-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="52286-114">La notificación de **SMC \_ SETSFOBJECT** se usa con el flujo de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="52286-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="52286-115">El objeto se guarda en un formulario guardado en el registro y no se hace nada con el recuento de referencias en el objeto pasado.</span><span class="sxs-lookup"><span data-stu-id="52286-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="52286-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52286-116">Requirements</span></span>



| <span data-ttu-id="52286-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="52286-117">Requirement</span></span> | <span data-ttu-id="52286-118">Value</span><span class="sxs-lookup"><span data-stu-id="52286-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52286-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52286-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52286-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52286-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="52286-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52286-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52286-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52286-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52286-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52286-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52286-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52286-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="52286-125">IDL</span><span class="sxs-lookup"><span data-stu-id="52286-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52286-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52286-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




