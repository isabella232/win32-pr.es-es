---
description: Define la estructura del archivo de encabezado Monitor de red.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Estructura de CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652661"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="0f424-103">CAPTUREFILE \_ estructura de valores de encabezado \_</span><span class="sxs-lookup"><span data-stu-id="0f424-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="0f424-104">La estructura de **\_ \_ los valores del encabezado CAPTUREFILE** define la estructura del archivo de encabezado monitor de red.</span><span class="sxs-lookup"><span data-stu-id="0f424-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f424-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f424-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="0f424-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f424-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f424-107">**Signature**</span><span class="sxs-lookup"><span data-stu-id="0f424-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-108">Identificador único: ' GMBU.</span><span class="sxs-lookup"><span data-stu-id="0f424-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-109">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="0f424-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-110">Binario, decimal codificado (secundaria).</span><span class="sxs-lookup"><span data-stu-id="0f424-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="0f424-111">El valor de este miembro debe ser cero (0).</span><span class="sxs-lookup"><span data-stu-id="0f424-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="0f424-112">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="0f424-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-113">Decimal codificado binario (principal).</span><span class="sxs-lookup"><span data-stu-id="0f424-113">Binary coded decimal (major).</span></span> <span data-ttu-id="0f424-114">Este valor debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="0f424-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="0f424-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-116">Tipo de topología.</span><span class="sxs-lookup"><span data-stu-id="0f424-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-117">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="0f424-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-118">Hora de captura.</span><span class="sxs-lookup"><span data-stu-id="0f424-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-119">**FrameTableOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-120">Tabla de índice de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0f424-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-121">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-122">Tamaño de la tabla de índice de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0f424-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-123">**UserDataOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-124">Desplazamiento de datos del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f424-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-125">**UserDataLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-126">Longitud de los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="0f424-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-127">**CommentDataOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-128">Desplazamiento de datos de comentario.</span><span class="sxs-lookup"><span data-stu-id="0f424-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-129">**CommentDataLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-130">Longitud de los datos de comentario.</span><span class="sxs-lookup"><span data-stu-id="0f424-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-131">**StatisticsOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-132">Desplazamiento a la estructura **Statistics** .</span><span class="sxs-lookup"><span data-stu-id="0f424-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-133">**StatisticsLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-134">Longitud de la estructura de **estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="0f424-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-135">**NetworkInfoOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-136">Desplazamiento a la estructura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="0f424-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-137">**NetworkInfoLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-138">Longitud de la estructura **NETWORKINFO** .</span><span class="sxs-lookup"><span data-stu-id="0f424-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-139">**ConversationStatsOffset**</span><span class="sxs-lookup"><span data-stu-id="0f424-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-140">Este miembro no se usa.</span><span class="sxs-lookup"><span data-stu-id="0f424-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0f424-141">**ConversationStatsLength**</span><span class="sxs-lookup"><span data-stu-id="0f424-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f424-142">Este miembro no se usa.</span><span class="sxs-lookup"><span data-stu-id="0f424-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f424-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f424-143">Requirements</span></span>



| <span data-ttu-id="0f424-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f424-144">Requirement</span></span> | <span data-ttu-id="0f424-145">Value</span><span class="sxs-lookup"><span data-stu-id="0f424-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f424-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f424-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0f424-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0f424-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f424-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f424-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0f424-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f424-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f424-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f424-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f424-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f424-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




