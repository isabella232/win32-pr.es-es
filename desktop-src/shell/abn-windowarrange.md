---
description: Notifica a una Appbar que el usuario ha seleccionado el comando en cascada, mosaico horizontal o mosaico vertical en el menú contextual de la barra de tareas.
title: Mensaje de ABN_WINDOWARRANGE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540587"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="b2e50-103">Mensaje de ABN \_ WINDOWARRANGE</span><span class="sxs-lookup"><span data-stu-id="b2e50-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="b2e50-104">Notifica a una Appbar que el usuario ha seleccionado el comando en cascada, mosaico horizontal o mosaico vertical en el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="b2e50-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b2e50-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2e50-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e50-106">*fBeginning*</span><span class="sxs-lookup"><span data-stu-id="b2e50-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e50-107">Marca que especifica si se está iniciando la operación Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="b2e50-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="b2e50-108">Este parámetro es **true** si se está iniciando la operación y las ventanas todavía no se han cambiado.</span><span class="sxs-lookup"><span data-stu-id="b2e50-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="b2e50-109">Es **false** si se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="b2e50-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e50-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2e50-110">Return value</span></span>

<span data-ttu-id="b2e50-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b2e50-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e50-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2e50-112">Remarks</span></span>

<span data-ttu-id="b2e50-113">El sistema envía este mensaje de notificación dos veces primero con *lParam* establecido en **true** y, a continuación, con *lParam* establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="b2e50-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="b2e50-114">La primera notificación se envía antes de que las ventanas estén en cascada o en mosaico, y la segunda se envía después de que se haya realizado la operación Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="b2e50-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e50-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2e50-115">Requirements</span></span>



| <span data-ttu-id="b2e50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e50-116">Requirement</span></span> | <span data-ttu-id="b2e50-117">Value</span><span class="sxs-lookup"><span data-stu-id="b2e50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e50-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2e50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e50-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b2e50-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b2e50-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2e50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e50-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2e50-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2e50-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2e50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e50-123"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e50-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




