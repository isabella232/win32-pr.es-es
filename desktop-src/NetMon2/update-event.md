---
description: Los eventos de actualización de la \_ estructura de eventos. Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento mediante NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Estructura de UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677670"
---
# <a name="update_event-structure"></a><span data-ttu-id="0b12b-104">ACTUALIZAR la \_ estructura de eventos</span><span class="sxs-lookup"><span data-stu-id="0b12b-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="0b12b-105">Los eventos de actualización de la estructura de **\_ eventos** .</span><span class="sxs-lookup"><span data-stu-id="0b12b-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="0b12b-106">Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento mediante NPP.</span><span class="sxs-lookup"><span data-stu-id="0b12b-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b12b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b12b-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="0b12b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b12b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b12b-109">**Evento**</span><span class="sxs-lookup"><span data-stu-id="0b12b-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-110">Evento real que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="0b12b-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-111">**Acción**</span><span class="sxs-lookup"><span data-stu-id="0b12b-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-112">Acción realizada.</span><span class="sxs-lookup"><span data-stu-id="0b12b-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-113">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0b12b-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-114">Indicación del estado de la red.</span><span class="sxs-lookup"><span data-stu-id="0b12b-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0b12b-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-116">Variable de contador auxiliar.</span><span class="sxs-lookup"><span data-stu-id="0b12b-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-117">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="0b12b-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-118">Los eventos marcados, en microsegundos.</span><span class="sxs-lookup"><span data-stu-id="0b12b-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-119">**lpUserContext**</span><span class="sxs-lookup"><span data-stu-id="0b12b-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-120">Contexto de usuario proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0b12b-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="0b12b-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-122">Controlador o uso de NAL.</span><span class="sxs-lookup"><span data-stu-id="0b12b-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-123">**FramesDropped**</span><span class="sxs-lookup"><span data-stu-id="0b12b-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-124">Fotogramas RTF quitados en el búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="0b12b-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="0b12b-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-126">No se devuelve ningún dato con esta opción de modificador.</span><span class="sxs-lookup"><span data-stu-id="0b12b-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-127">**lpFrameTable**</span><span class="sxs-lookup"><span data-stu-id="0b12b-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-128">Solo RTF.</span><span class="sxs-lookup"><span data-stu-id="0b12b-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-129">**lpPacketQueue**</span><span class="sxs-lookup"><span data-stu-id="0b12b-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-130">Para las retransmisiones.</span><span class="sxs-lookup"><span data-stu-id="0b12b-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-131">**SecurityResponse**</span><span class="sxs-lookup"><span data-stu-id="0b12b-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-132">Respuesta del monitor de seguridad remota.</span><span class="sxs-lookup"><span data-stu-id="0b12b-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="0b12b-133">**lpFinalStats**</span><span class="sxs-lookup"><span data-stu-id="0b12b-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="0b12b-134">Esto solo se rellena en paradas no relacionadas con la seguridad (por ejemplo, desencadenadores).</span><span class="sxs-lookup"><span data-stu-id="0b12b-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b12b-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b12b-135">Remarks</span></span>

<span data-ttu-id="0b12b-136">Los usuarios de C++ deben tener en cuenta que la declaración de esta devolución de llamada debe estar en la parte pública del archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0b12b-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="0b12b-137">La implementación debe estar en la sección protegida del archivo. cpp:</span><span class="sxs-lookup"><span data-stu-id="0b12b-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="0b12b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b12b-138">Requirements</span></span>



| <span data-ttu-id="0b12b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b12b-139">Requirement</span></span> | <span data-ttu-id="0b12b-140">Value</span><span class="sxs-lookup"><span data-stu-id="0b12b-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b12b-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b12b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0b12b-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0b12b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0b12b-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b12b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0b12b-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b12b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b12b-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b12b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b12b-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b12b-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




