---
description: La estructura EXPERTFRAMEDESCRIPTOR contiene información sobre un marco. Cuando el experto llama a la función ExpertGetFrame correctamente, Monitor de red pasa la estructura EXPERTFRAMEDESCRIPTOR al experto.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Estructura EXPERTFRAMEDESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497008"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="82d08-104">Estructura EXPERTFRAMEDESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="82d08-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="82d08-105">La estructura **EXPERTFRAMEDESCRIPTOR** contiene información sobre un marco.</span><span class="sxs-lookup"><span data-stu-id="82d08-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="82d08-106">Cuando el experto llama a la función [**ExpertGetFrame**](expertgetframe.md) correctamente, monitor de red pasa la estructura **EXPERTFRAMEDESCRIPTOR** al experto.</span><span class="sxs-lookup"><span data-stu-id="82d08-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d08-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82d08-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="82d08-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="82d08-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="82d08-109">**Númeromarco**</span><span class="sxs-lookup"><span data-stu-id="82d08-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-110">Número de un marco especificado.</span><span class="sxs-lookup"><span data-stu-id="82d08-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-111">**hFrame**</span><span class="sxs-lookup"><span data-stu-id="82d08-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-112">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="82d08-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="82d08-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-114">Puntero a un fotograma sin formato.</span><span class="sxs-lookup"><span data-stu-id="82d08-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-115">**lpRecognizeDataTable**</span><span class="sxs-lookup"><span data-stu-id="82d08-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-116">Tabla que indica la ubicación en la que cada analizador identifica el inicio de los datos.</span><span class="sxs-lookup"><span data-stu-id="82d08-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="82d08-117">**lpPropertyTable**</span><span class="sxs-lookup"><span data-stu-id="82d08-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="82d08-118">Tabla de propiedades de marco que identifica el analizador.</span><span class="sxs-lookup"><span data-stu-id="82d08-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d08-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82d08-119">Remarks</span></span>

<span data-ttu-id="82d08-120">Si el experto especifica FLAGs \_ Attach \_ Properties al llamar a [**ExpertGetFrame**](expertgetframe.md), el miembro **szPropertyText** de cada estructura [**PROPERTYINST**](propertyinst.md) es **null**.</span><span class="sxs-lookup"><span data-stu-id="82d08-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="82d08-121">Si el experto no especifica \_ las propiedades de adjuntar marcas \_ al llamar a la función [**ExpertGetFrame**](expertgetframe.md) , el miembro **lpPropertyTable** es **null** en la devolución.</span><span class="sxs-lookup"><span data-stu-id="82d08-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d08-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d08-122">Requirements</span></span>



| <span data-ttu-id="82d08-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d08-123">Requirement</span></span> | <span data-ttu-id="82d08-124">Value</span><span class="sxs-lookup"><span data-stu-id="82d08-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82d08-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d08-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82d08-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82d08-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="82d08-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82d08-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82d08-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82d08-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82d08-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82d08-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d08-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d08-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




