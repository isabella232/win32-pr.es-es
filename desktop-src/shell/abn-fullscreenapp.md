---
description: Notifica a una Appbar cuando una aplicación de pantalla completa se abre o se cierra. Esta notificación se envía en forma de un mensaje definido por la aplicación que se establece mediante el \_ nuevo mensaje ABN.
title: Mensaje de ABN_FULLSCREENAPP (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153925"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="2e6bf-104">Mensaje de ABN \_ FULLSCREENAPP</span><span class="sxs-lookup"><span data-stu-id="2e6bf-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="2e6bf-105">Notifica a una Appbar cuando una aplicación de pantalla completa se abre o se cierra.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="2e6bf-106">Esta notificación se envía en forma de un mensaje definido por la aplicación que se establece mediante el [**\_ nuevo mensaje ABN**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="2e6bf-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="2e6bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e6bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e6bf-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="2e6bf-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="2e6bf-109">Marca que especifica si una aplicación de pantalla completa se está abriendo o cerrando.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="2e6bf-110">Este parámetro es **true** si la aplicación se está abriendo o **false** si se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e6bf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e6bf-111">Return value</span></span>

<span data-ttu-id="2e6bf-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e6bf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e6bf-113">Remarks</span></span>

<span data-ttu-id="2e6bf-114">Cuando se abre una aplicación de pantalla completa, un Appbar debe colocarse en la parte inferior del orden z.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="2e6bf-115">Cuando se está cerrando, el control Appbar debe restaurar su posición de orden z.</span><span class="sxs-lookup"><span data-stu-id="2e6bf-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6bf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e6bf-116">Requirements</span></span>



| <span data-ttu-id="2e6bf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6bf-117">Requirement</span></span> | <span data-ttu-id="2e6bf-118">Value</span><span class="sxs-lookup"><span data-stu-id="2e6bf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6bf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6bf-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2e6bf-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2e6bf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6bf-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e6bf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e6bf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e6bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6bf-124"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6bf-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




