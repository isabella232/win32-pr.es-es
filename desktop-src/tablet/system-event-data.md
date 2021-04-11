---
description: Contiene información acerca de un evento de Tablet PC.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Estructura de SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279379"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="0f798-103">Estructura de datos de \_ eventos del sistema \_</span><span class="sxs-lookup"><span data-stu-id="0f798-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="0f798-104">Contiene información acerca de un evento de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0f798-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f798-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f798-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="0f798-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f798-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f798-107">**bModifier**</span><span class="sxs-lookup"><span data-stu-id="0f798-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-108">Valores de bit para los modificadores.</span><span class="sxs-lookup"><span data-stu-id="0f798-108">Bit values for the modifiers.</span></span> <span data-ttu-id="0f798-109">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0f798-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="0f798-110">**wKey**</span><span class="sxs-lookup"><span data-stu-id="0f798-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-111">Digitalice el código para el carácter del teclado.</span><span class="sxs-lookup"><span data-stu-id="0f798-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="0f798-112">**xPos**</span><span class="sxs-lookup"><span data-stu-id="0f798-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-113">Posición X del evento.</span><span class="sxs-lookup"><span data-stu-id="0f798-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="0f798-114">**yPos**</span><span class="sxs-lookup"><span data-stu-id="0f798-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-115">Posición Y del evento.</span><span class="sxs-lookup"><span data-stu-id="0f798-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="0f798-116">**bCursorMode**</span><span class="sxs-lookup"><span data-stu-id="0f798-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-117">El tipo de cursor que causó el evento.</span><span class="sxs-lookup"><span data-stu-id="0f798-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="0f798-118">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0f798-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="0f798-119">**dwButtonState**</span><span class="sxs-lookup"><span data-stu-id="0f798-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="0f798-120">Estado de los botones en el momento del evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="0f798-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f798-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f798-121">Remarks</span></span>

<span data-ttu-id="0f798-122">Los siguientes eventos del sistema se definen para su uso en el miembro **bModifier** .</span><span class="sxs-lookup"><span data-stu-id="0f798-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="0f798-123">Value</span><span class="sxs-lookup"><span data-stu-id="0f798-123">Value</span></span>               | <span data-ttu-id="0f798-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f798-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="0f798-125">SE \_ modificador se \_ Ctrl</span><span class="sxs-lookup"><span data-stu-id="0f798-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="0f798-126">Se presionó la tecla control.</span><span class="sxs-lookup"><span data-stu-id="0f798-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="0f798-127">\_modificador se \_ Alt Alt</span><span class="sxs-lookup"><span data-stu-id="0f798-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="0f798-128">Se presionó la tecla Alt.</span><span class="sxs-lookup"><span data-stu-id="0f798-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="0f798-129">\_desplazamiento del modificador se \_</span><span class="sxs-lookup"><span data-stu-id="0f798-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="0f798-130">Se presionó la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="0f798-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="0f798-131">Los siguientes eventos del sistema se definen para su uso en el miembro **bCursorMode** .</span><span class="sxs-lookup"><span data-stu-id="0f798-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="0f798-132">Value</span><span class="sxs-lookup"><span data-stu-id="0f798-132">Value</span></span>              | <span data-ttu-id="0f798-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f798-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="0f798-134">\_cursor normal de se \_</span><span class="sxs-lookup"><span data-stu-id="0f798-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="0f798-135">Indica la punta del lápiz.</span><span class="sxs-lookup"><span data-stu-id="0f798-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="0f798-136">\_cursor de borrador de se \_</span><span class="sxs-lookup"><span data-stu-id="0f798-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="0f798-137">Indica el borrador del lápiz.</span><span class="sxs-lookup"><span data-stu-id="0f798-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0f798-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f798-138">Requirements</span></span>



| <span data-ttu-id="0f798-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f798-139">Requirement</span></span> | <span data-ttu-id="0f798-140">Value</span><span class="sxs-lookup"><span data-stu-id="0f798-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0f798-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f798-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0f798-142">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0f798-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f798-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f798-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0f798-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0f798-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="0f798-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f798-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f798-146">**IStylusPlugin:: SystemEvent (método)**</span><span class="sxs-lookup"><span data-stu-id="0f798-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="0f798-147">**ITabletEventSink:: SystemEvent (método)**</span><span class="sxs-lookup"><span data-stu-id="0f798-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




