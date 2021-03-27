---
description: Notifica a una Appbar que el estado de ocultar automáticamente o siempre en la barra de tareas ha cambiado&\# 8212; es decir, el usuario ha seleccionado o desactivado el &\# 0034; Siempre visible&\# 0034 o &\# 0034; Ocultar automáticamente&\# 0034; en la hoja de propiedades de la barra de tareas.
title: Mensaje de ABN_STATECHANGE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907733"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="fcbef-103">Mensaje de ABN. \_</span><span class="sxs-lookup"><span data-stu-id="fcbef-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="fcbef-104">Notifica a una Appbar que el estado de ocultación automática o siempre visible de la barra de tareas ha cambiado es decir, el usuario ha activado o desactivado la casilla "siempre visible" o "ocultar automáticamente" en la hoja de propiedades de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="fcbef-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="fcbef-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcbef-105">Parameters</span></span>

<span data-ttu-id="fcbef-106">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fcbef-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fcbef-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbef-107">Return value</span></span>

<span data-ttu-id="fcbef-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fcbef-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbef-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcbef-109">Remarks</span></span>

<span data-ttu-id="fcbef-110">Un Appbar puede usar este mensaje de notificación para establecer su estado de conformidad con el de la barra de tareas, si lo desea.</span><span class="sxs-lookup"><span data-stu-id="fcbef-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbef-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbef-111">Requirements</span></span>



| <span data-ttu-id="fcbef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbef-112">Requirement</span></span> | <span data-ttu-id="fcbef-113">Value</span><span class="sxs-lookup"><span data-stu-id="fcbef-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbef-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcbef-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fcbef-115">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fcbef-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fcbef-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcbef-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fcbef-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fcbef-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcbef-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcbef-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcbef-119"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbef-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




