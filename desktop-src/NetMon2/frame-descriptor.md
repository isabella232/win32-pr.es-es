---
description: La estructura de descriptores de fotogramas \_ proporciona información descriptiva sobre fotogramas sin formato.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Estructura de FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677291"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="5856a-103">\_Estructura de descriptor de marco</span><span class="sxs-lookup"><span data-stu-id="5856a-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="5856a-104">La estructura de **\_ descriptores de fotogramas** proporciona información descriptiva sobre fotogramas sin formato.</span><span class="sxs-lookup"><span data-stu-id="5856a-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="5856a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5856a-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="5856a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5856a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5856a-107">**FramePointer**</span><span class="sxs-lookup"><span data-stu-id="5856a-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-108">Puntero a los datos del marco.</span><span class="sxs-lookup"><span data-stu-id="5856a-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-109">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="5856a-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-110">Hora del sistema, en microsegundos, en que se capturó el fotograma.</span><span class="sxs-lookup"><span data-stu-id="5856a-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="5856a-111">Este tiempo se usa normalmente para determinar el intervalo entre las veces que se capturaron dos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="5856a-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-112">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="5856a-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-113">Longitud del marco.</span><span class="sxs-lookup"><span data-stu-id="5856a-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-114">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="5856a-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-115">Longitud de fotograma real copiada.</span><span class="sxs-lookup"><span data-stu-id="5856a-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-116">**ETYPE**</span><span class="sxs-lookup"><span data-stu-id="5856a-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-117">ETYPE nombre.</span><span class="sxs-lookup"><span data-stu-id="5856a-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-118">**SAP**</span><span class="sxs-lookup"><span data-stu-id="5856a-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-119">Valor de SAP.</span><span class="sxs-lookup"><span data-stu-id="5856a-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-120">**LowProtocol**</span><span class="sxs-lookup"><span data-stu-id="5856a-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-121">Índice de protocolo encontrado.</span><span class="sxs-lookup"><span data-stu-id="5856a-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-122">**LowProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="5856a-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-123">Desplazamiento a los datos de protocolo obtenidos de **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="5856a-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-124">**HighPort**</span><span class="sxs-lookup"><span data-stu-id="5856a-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-125">Puerto del protocolo alto identificado en **LowProtocol**.</span><span class="sxs-lookup"><span data-stu-id="5856a-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="5856a-126">**HighProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="5856a-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5856a-127">Desplazamiento a los datos de protocolo obtenidos de **HighPort**.</span><span class="sxs-lookup"><span data-stu-id="5856a-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5856a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5856a-128">Requirements</span></span>



| <span data-ttu-id="5856a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5856a-129">Requirement</span></span> | <span data-ttu-id="5856a-130">Value</span><span class="sxs-lookup"><span data-stu-id="5856a-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5856a-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5856a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5856a-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5856a-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5856a-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5856a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5856a-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5856a-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5856a-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5856a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5856a-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5856a-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




