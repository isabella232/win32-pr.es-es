---
description: Notifica que hay un recuadro informativo que se va a mostrar para el botón de contenido adicional asociado al elemento especificado por la estructura SMDATA correspondiente.
title: Mensaje de SMC_DISPLAYCHEVRONTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497884"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="846c9-103">Mensaje de DISPLAYCHEVRONTIP de SMC \_</span><span class="sxs-lookup"><span data-stu-id="846c9-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="846c9-104">Notifica que hay un recuadro informativo que se va a mostrar para el botón de contenido adicional asociado al elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="846c9-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="846c9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="846c9-105">Parameters</span></span>

<span data-ttu-id="846c9-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="846c9-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="846c9-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="846c9-107">Return value</span></span>

<span data-ttu-id="846c9-108">Vuelva \_ a aceptar para mostrar el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="846c9-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="846c9-109">Devuelve S \_ false para impedir que se muestre el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="846c9-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="846c9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="846c9-110">Remarks</span></span>

<span data-ttu-id="846c9-111">El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.</span><span class="sxs-lookup"><span data-stu-id="846c9-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="846c9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="846c9-112">Requirements</span></span>



| <span data-ttu-id="846c9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="846c9-113">Requirement</span></span> | <span data-ttu-id="846c9-114">Value</span><span class="sxs-lookup"><span data-stu-id="846c9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="846c9-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="846c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="846c9-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="846c9-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="846c9-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="846c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="846c9-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="846c9-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="846c9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="846c9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="846c9-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="846c9-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="846c9-121">IDL</span><span class="sxs-lookup"><span data-stu-id="846c9-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="846c9-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="846c9-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




