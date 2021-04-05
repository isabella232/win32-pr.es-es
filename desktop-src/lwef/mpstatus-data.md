---
title: MPSTATUS_DATA estructura (MpClient. h)
description: Contiene datos sobre el estado actual de un componente del producto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSTATUS_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802876"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="42b26-105">\_Estructura de datos MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="42b26-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="42b26-106">Contiene datos sobre el estado actual de un componente del producto.</span><span class="sxs-lookup"><span data-stu-id="42b26-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b26-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42b26-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="42b26-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="42b26-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="42b26-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="42b26-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-110">Tipo: **[ **\_ ID. de MPCOMPONENT**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="42b26-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-111">IDENTIFICADOR de componente específico para el que se ha comunicado el estado.</span><span class="sxs-lookup"><span data-stu-id="42b26-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="42b26-112">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="42b26-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="42b26-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-114">Estado solicitado para el componente.</span><span class="sxs-lookup"><span data-stu-id="42b26-114">Status requested for the component.</span></span> <span data-ttu-id="42b26-115">**hResult** en los datos de devolución de llamada indica si la solicitud se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="42b26-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="42b26-116">**ComponentStatus**</span><span class="sxs-lookup"><span data-stu-id="42b26-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-117">Datos de estado adicionales en función del valor de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="42b26-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="42b26-118">En la actualidad, da como resultado un puntero a una estructura ficticia para todos los valores posibles de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="42b26-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="42b26-119">**P1**</span><span class="sxs-lookup"><span data-stu-id="42b26-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-120">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-121">Cuando **ComponentID**  ==  **MPCOMPONENT \_ como \_ Signature**.</span><span class="sxs-lookup"><span data-stu-id="42b26-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="42b26-122">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-123">**P2**</span><span class="sxs-lookup"><span data-stu-id="42b26-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-124">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-125">Cuando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ Signature**.</span><span class="sxs-lookup"><span data-stu-id="42b26-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="42b26-126">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-127">**P3**</span><span class="sxs-lookup"><span data-stu-id="42b26-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-128">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-129">Cuando **ComponentID**  ==  **MPCOMPONENT \_ \_ monitor en tiempo real**.</span><span class="sxs-lookup"><span data-stu-id="42b26-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="42b26-130">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="42b26-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-132">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-133">Cuando **ComponentID**  ==  **MPCOMPONENT la \_ \_ protección de acceso**.</span><span class="sxs-lookup"><span data-stu-id="42b26-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="42b26-134">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-135">**P5**</span><span class="sxs-lookup"><span data-stu-id="42b26-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-136">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-137">Cuando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ PROTECTION**.</span><span class="sxs-lookup"><span data-stu-id="42b26-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="42b26-138">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-139">**microarquitectura**</span><span class="sxs-lookup"><span data-stu-id="42b26-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-140">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-141">Cuando **ComponentID**  ==  **MPCOMPONENT \_ Behavior \_ monitor**.</span><span class="sxs-lookup"><span data-stu-id="42b26-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="42b26-142">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="42b26-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-144">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-145">Cuando **ComponentID**  ==  **MPCOMPONENT \_ se \_ examina automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="42b26-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="42b26-146">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-147">**P8**</span><span class="sxs-lookup"><span data-stu-id="42b26-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-148">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-149">Cuando **ComponentID**  ==  **MPCOMPONENT \_ \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="42b26-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="42b26-150">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="42b26-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-152">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-153">Cuando **ComponentID**  ==  **MPCOMPONENT \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="42b26-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="42b26-154">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-155">**Pennsylvania**</span><span class="sxs-lookup"><span data-stu-id="42b26-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-156">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-157">Cuando **ComponentID**  ==  **MPCOMPONENT \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="42b26-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="42b26-158">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b26-159">**PB**</span><span class="sxs-lookup"><span data-stu-id="42b26-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="42b26-160">Tipo: **PMPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="42b26-161">Cuando **ComponentID**  ==  **MPCOMPONENT \_ Elam**.</span><span class="sxs-lookup"><span data-stu-id="42b26-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="42b26-162">Consulte [**MPSTATUS \_ DATAEX \_ Unused**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="42b26-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42b26-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42b26-163">Requirements</span></span>



| <span data-ttu-id="42b26-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b26-164">Requirement</span></span> | <span data-ttu-id="42b26-165">Value</span><span class="sxs-lookup"><span data-stu-id="42b26-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42b26-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42b26-166">Minimum supported client</span></span><br/> | <span data-ttu-id="42b26-167">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="42b26-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="42b26-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42b26-168">Minimum supported server</span></span><br/> | <span data-ttu-id="42b26-169">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="42b26-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42b26-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42b26-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b26-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="42b26-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b26-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="42b26-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b26-173">**identificador de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="42b26-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="42b26-174">**MPSTATUS \_ DATAEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="42b26-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





