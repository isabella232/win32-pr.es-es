---
description: Fotograma real del controlador.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Estructura de marco (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677289"
---
# <a name="frame-structure"></a><span data-ttu-id="83840-103">Estructura de marco</span><span class="sxs-lookup"><span data-stu-id="83840-103">FRAME structure</span></span>

<span data-ttu-id="83840-104">La estructura del **marco** es un fotograma real del controlador.</span><span class="sxs-lookup"><span data-stu-id="83840-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="83840-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83840-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="83840-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="83840-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="83840-107">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="83840-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="83840-108">Tiempo transcurrido, en microsegundos, entre el inicio de la captura y el momento en que se capturó el fotograma.</span><span class="sxs-lookup"><span data-stu-id="83840-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="83840-109">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="83840-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="83840-110">Longitud del marco MAC.</span><span class="sxs-lookup"><span data-stu-id="83840-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="83840-111">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="83840-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="83840-112">Longitud de fotograma real copiada.</span><span class="sxs-lookup"><span data-stu-id="83840-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="83840-113">**MacFrame**</span><span class="sxs-lookup"><span data-stu-id="83840-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="83840-114">Datos de marco.</span><span class="sxs-lookup"><span data-stu-id="83840-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83840-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83840-115">Requirements</span></span>



| <span data-ttu-id="83840-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83840-116">Requirement</span></span> | <span data-ttu-id="83840-117">Value</span><span class="sxs-lookup"><span data-stu-id="83840-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83840-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83840-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83840-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="83840-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="83840-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83840-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83840-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="83840-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="83840-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83840-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83840-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83840-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




