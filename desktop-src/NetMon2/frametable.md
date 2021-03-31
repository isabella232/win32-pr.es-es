---
description: La estructura FRAMETABLE, un búfer circular de punteros de Marcos, se reenvía a las aplicaciones adjuntas a la interfaz ITRC de NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Estructura FRAMETABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153863"
---
# <a name="frametable-structure"></a><span data-ttu-id="e0615-103">Estructura FRAMETABLE</span><span class="sxs-lookup"><span data-stu-id="e0615-103">FRAMETABLE structure</span></span>

<span data-ttu-id="e0615-104">La estructura **frametable** , un búfer circular de punteros de Marcos, se reenvía a las aplicaciones adjuntas a la interfaz **ITRC** de NPP.</span><span class="sxs-lookup"><span data-stu-id="e0615-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0615-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0615-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="e0615-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0615-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0615-107">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="e0615-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="e0615-108">La longitud total de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0615-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="e0615-109">**Super**</span><span class="sxs-lookup"><span data-stu-id="e0615-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e0615-110">Primer índice de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0615-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="e0615-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="e0615-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e0615-112">Último índice de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0615-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="e0615-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="e0615-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="e0615-114">Número de fotogramas descritos en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="e0615-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="e0615-115">**Imágenes**</span><span class="sxs-lookup"><span data-stu-id="e0615-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="e0615-116">Matriz real de descriptores de marco.</span><span class="sxs-lookup"><span data-stu-id="e0615-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0615-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0615-117">Requirements</span></span>



| <span data-ttu-id="e0615-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0615-118">Requirement</span></span> | <span data-ttu-id="e0615-119">Value</span><span class="sxs-lookup"><span data-stu-id="e0615-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e0615-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0615-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0615-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e0615-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e0615-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0615-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0615-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0615-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e0615-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0615-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0615-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0615-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




