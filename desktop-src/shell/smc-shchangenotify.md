---
description: Le informa de que se ha producido un cambio.
title: Mensaje de SMC_SHCHANGENOTIFY (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985562"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="86a0b-103">Mensaje de SHCHANGENOTIFY de SMC \_</span><span class="sxs-lookup"><span data-stu-id="86a0b-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="86a0b-104">Le informa de que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="86a0b-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="86a0b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86a0b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a0b-106">*psmc*</span><span class="sxs-lookup"><span data-stu-id="86a0b-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="86a0b-107">Puntero a una estructura [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) con información sobre el cambio.</span><span class="sxs-lookup"><span data-stu-id="86a0b-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a0b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86a0b-108">Return value</span></span>

<span data-ttu-id="86a0b-109">Devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="86a0b-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a0b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86a0b-110">Remarks</span></span>

<span data-ttu-id="86a0b-111">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="86a0b-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a0b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86a0b-112">Requirements</span></span>



| <span data-ttu-id="86a0b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="86a0b-113">Requirement</span></span> | <span data-ttu-id="86a0b-114">Value</span><span class="sxs-lookup"><span data-stu-id="86a0b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a0b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86a0b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="86a0b-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86a0b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86a0b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86a0b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="86a0b-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86a0b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86a0b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86a0b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="86a0b-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86a0b-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="86a0b-121">IDL</span><span class="sxs-lookup"><span data-stu-id="86a0b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86a0b-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86a0b-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




