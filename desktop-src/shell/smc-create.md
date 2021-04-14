---
description: Le notifica que se ha creado una banda de menús.
title: Mensaje de SMC_CREATE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997800"
---
# <a name="smc_create-message"></a><span data-ttu-id="d1ce9-103">\_Crear mensaje de SMC</span><span class="sxs-lookup"><span data-stu-id="d1ce9-103">SMC\_CREATE message</span></span>

<span data-ttu-id="d1ce9-104">Le notifica que se ha creado una banda de menús.</span><span class="sxs-lookup"><span data-stu-id="d1ce9-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="d1ce9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1ce9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ce9-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="d1ce9-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="d1ce9-107">Un puntero al miembro **pvUserData** de una estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="d1ce9-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ce9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1ce9-108">Return value</span></span>

<span data-ttu-id="d1ce9-109">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d1ce9-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1ce9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1ce9-110">Remarks</span></span>

<span data-ttu-id="d1ce9-111">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="d1ce9-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ce9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ce9-112">Requirements</span></span>



| <span data-ttu-id="d1ce9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ce9-113">Requirement</span></span> | <span data-ttu-id="d1ce9-114">Value</span><span class="sxs-lookup"><span data-stu-id="d1ce9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ce9-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1ce9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ce9-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1ce9-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d1ce9-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1ce9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ce9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1ce9-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1ce9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1ce9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ce9-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ce9-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1ce9-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d1ce9-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1ce9-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1ce9-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




