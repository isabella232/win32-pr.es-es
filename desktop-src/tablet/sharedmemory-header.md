---
description: Almacena información sobre las secciones de la memoria compartida.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Estructura de SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678155"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="c1739-103">\_Estructura del encabezado SHAREDMEMORY</span><span class="sxs-lookup"><span data-stu-id="c1739-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="c1739-104">Almacena información sobre las secciones de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="c1739-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1739-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1739-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="c1739-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1739-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1739-107">**cbTotal**</span><span class="sxs-lookup"><span data-stu-id="c1739-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-108">Tamaño, en bytes, de los datos a los que hace referencia esta estructura de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c1739-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-109">**cbOffsetSns**</span><span class="sxs-lookup"><span data-stu-id="c1739-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-110">Tamaño, en bytes, que los números de serie se desplazan de la estructura de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c1739-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-111">**idxEvent**</span><span class="sxs-lookup"><span data-stu-id="c1739-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-112">Índice del evento.</span><span class="sxs-lookup"><span data-stu-id="c1739-112">The event index.</span></span> <span data-ttu-id="c1739-113">Este valor se incrementa con eventos sucesivos.</span><span class="sxs-lookup"><span data-stu-id="c1739-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-114">**dwEvent**</span><span class="sxs-lookup"><span data-stu-id="c1739-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-115">Evento asociado a este encabezado.</span><span class="sxs-lookup"><span data-stu-id="c1739-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-116">**Cid**</span><span class="sxs-lookup"><span data-stu-id="c1739-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-117">Identificador de cursor al que hace referencia el encabezado de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="c1739-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="c1739-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-119">Número de serie del encabezado de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="c1739-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-120">**sysEvt**</span><span class="sxs-lookup"><span data-stu-id="c1739-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-121">El evento del sistema, prefijo SE \_ \* asocia a este encabezado.</span><span class="sxs-lookup"><span data-stu-id="c1739-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="c1739-122">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c1739-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-123">**sysEvtData**</span><span class="sxs-lookup"><span data-stu-id="c1739-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-124">La estructura de [**\_ \_ datos de eventos del sistema**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) asociada al evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="c1739-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-125">**cPackets**</span><span class="sxs-lookup"><span data-stu-id="c1739-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-126">Un recuento de los paquetes asociados a la sección memoria compartida actual.</span><span class="sxs-lookup"><span data-stu-id="c1739-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-127">**cbPackets**</span><span class="sxs-lookup"><span data-stu-id="c1739-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-128">Tamaño, en bytes, de los paquetes asociados a la sección memoria compartida actual.</span><span class="sxs-lookup"><span data-stu-id="c1739-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="c1739-129">**fSnsPresent**</span><span class="sxs-lookup"><span data-stu-id="c1739-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="c1739-130">Marca que indica si los números de serie están presentes en la sección memoria compartida actual.</span><span class="sxs-lookup"><span data-stu-id="c1739-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1739-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1739-131">Remarks</span></span>

<span data-ttu-id="c1739-132">Los siguientes valores se definen para el miembro **sysEvt** .</span><span class="sxs-lookup"><span data-stu-id="c1739-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="c1739-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1739-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1739-134">**\_datos de eventos del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="c1739-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



