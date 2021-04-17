---
description: La estructura del DESENCADENAdor indica una acción que debe llevar a cabo el controlador en un momento determinado.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Estructura del DESENCADENAdor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678207"
---
# <a name="trigger-structure"></a><span data-ttu-id="96a9e-103">Estructura del DESENCADENAdor</span><span class="sxs-lookup"><span data-stu-id="96a9e-103">TRIGGER structure</span></span>

<span data-ttu-id="96a9e-104">La estructura del **desencadenador** indica una acción que debe llevar a cabo el controlador en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="96a9e-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a9e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96a9e-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="96a9e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="96a9e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96a9e-107">**TriggerActive**</span><span class="sxs-lookup"><span data-stu-id="96a9e-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-108">Valor booleano que determina si el controlador debe prestar atención al desencadenador.</span><span class="sxs-lookup"><span data-stu-id="96a9e-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="96a9e-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-110">Código de operación del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="96a9e-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="96a9e-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-112">Acción que el desencadenador debe llevar a cabo si se activa.</span><span class="sxs-lookup"><span data-stu-id="96a9e-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-113">**TriggerFlags**</span><span class="sxs-lookup"><span data-stu-id="96a9e-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-114">Marcas de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="96a9e-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-115">**TriggerPatternMatch**</span><span class="sxs-lookup"><span data-stu-id="96a9e-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-116">Coincidencia de patrón de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="96a9e-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-117">**TriggerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="96a9e-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-118">Tamaño del búfer del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="96a9e-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="96a9e-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="96a9e-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="96a9e-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="96a9e-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96a9e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96a9e-121">Requirements</span></span>



| <span data-ttu-id="96a9e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a9e-122">Requirement</span></span> | <span data-ttu-id="96a9e-123">Value</span><span class="sxs-lookup"><span data-stu-id="96a9e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="96a9e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96a9e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="96a9e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="96a9e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="96a9e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96a9e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="96a9e-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96a9e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="96a9e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96a9e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a9e-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a9e-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




