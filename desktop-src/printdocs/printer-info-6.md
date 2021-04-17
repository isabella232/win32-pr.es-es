---
description: La \_ información de la impresora \_ 6 especifica el valor de estado de una impresora.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Estructura de PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716945"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="801ff-103">Estructura de la información de la impresora \_ \_ 6</span><span class="sxs-lookup"><span data-stu-id="801ff-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="801ff-104">La **información de la impresora \_ \_ 6** especifica el valor de estado de una impresora.</span><span class="sxs-lookup"><span data-stu-id="801ff-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="801ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="801ff-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="801ff-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="801ff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="801ff-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="801ff-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="801ff-108">El estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="801ff-108">The printer status.</span></span> <span data-ttu-id="801ff-109">Este miembro puede ser cualquier combinación razonable de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="801ff-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="801ff-110">Value</span><span class="sxs-lookup"><span data-stu-id="801ff-110">Value</span></span>                               | <span data-ttu-id="801ff-111">Significado</span><span class="sxs-lookup"><span data-stu-id="801ff-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801ff-112">Estado de la impresora \_ \_ ocupado</span><span class="sxs-lookup"><span data-stu-id="801ff-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="801ff-113">La impresora está ocupada.</span><span class="sxs-lookup"><span data-stu-id="801ff-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="801ff-114">puerta de estado de la impresora \_ \_ \_ abierta</span><span class="sxs-lookup"><span data-stu-id="801ff-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="801ff-115">La puerta de la impresora está abierta.</span><span class="sxs-lookup"><span data-stu-id="801ff-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="801ff-116">\_error de estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="801ff-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="801ff-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="801ff-118">Estado de la impresora \_ \_ inicializando</span><span class="sxs-lookup"><span data-stu-id="801ff-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="801ff-119">La impresora se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="801ff-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="801ff-120">\_e/s de estado de impresora \_ \_ activa</span><span class="sxs-lookup"><span data-stu-id="801ff-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="801ff-121">La impresora está en un estado de entrada/salida activo</span><span class="sxs-lookup"><span data-stu-id="801ff-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="801ff-122">\_ \_ alimentación manual de estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="801ff-123">La impresora está en un estado de alimentación manual.</span><span class="sxs-lookup"><span data-stu-id="801ff-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="801ff-124">Estado de la impresora \_ \_ sin \_ tóner</span><span class="sxs-lookup"><span data-stu-id="801ff-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="801ff-125">Se ha agotado el tóner de la impresora.</span><span class="sxs-lookup"><span data-stu-id="801ff-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="801ff-126">Estado de la impresora \_ \_ no \_ disponible</span><span class="sxs-lookup"><span data-stu-id="801ff-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="801ff-127">La impresora no está disponible para imprimir.</span><span class="sxs-lookup"><span data-stu-id="801ff-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="801ff-128">Estado de la impresora \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="801ff-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="801ff-129">La impresora no está conectada.</span><span class="sxs-lookup"><span data-stu-id="801ff-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="801ff-130">\_Estado de la impresora \_ sin \_ \_ memoria</span><span class="sxs-lookup"><span data-stu-id="801ff-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="801ff-131">La impresora se ha quedado sin memoria.</span><span class="sxs-lookup"><span data-stu-id="801ff-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="801ff-132">bandeja de salida de estado de la impresora \_ \_ \_ \_ llena</span><span class="sxs-lookup"><span data-stu-id="801ff-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="801ff-133">La bandeja de salida de la impresora está llena.</span><span class="sxs-lookup"><span data-stu-id="801ff-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="801ff-134">Página de estado de la impresora \_ \_ \_ aparcan</span><span class="sxs-lookup"><span data-stu-id="801ff-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="801ff-135">La impresora no puede imprimir la página actual.</span><span class="sxs-lookup"><span data-stu-id="801ff-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="801ff-136">\_atasco de \_ papel del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="801ff-137">El papel está atascado en la impresora</span><span class="sxs-lookup"><span data-stu-id="801ff-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="801ff-138">\_papel del estado de la impresora \_ \_</span><span class="sxs-lookup"><span data-stu-id="801ff-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="801ff-139">La impresora se ha quedado sin papel.</span><span class="sxs-lookup"><span data-stu-id="801ff-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="801ff-140">\_problema de \_ papel del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="801ff-141">La impresora tiene un problema de papel.</span><span class="sxs-lookup"><span data-stu-id="801ff-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="801ff-142">Estado de la impresora en \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="801ff-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="801ff-143">La impresora está en pausa.</span><span class="sxs-lookup"><span data-stu-id="801ff-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="801ff-144">Estado de la impresora \_ \_ pendiente de \_ eliminación</span><span class="sxs-lookup"><span data-stu-id="801ff-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="801ff-145">La impresora está pendiente de eliminación como resultado de una llamada a la función [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="801ff-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="801ff-146">Estado de la impresora- \_ \_ \_ guardar energía</span><span class="sxs-lookup"><span data-stu-id="801ff-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="801ff-147">La impresora está en modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="801ff-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="801ff-148">\_impresión del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="801ff-149">La impresora se está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="801ff-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="801ff-150">\_procesamiento del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="801ff-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="801ff-151">La impresora está procesando un comando de la función [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="801ff-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="801ff-152">servidor de estado de impresora \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="801ff-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="801ff-153">No se conoce el estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="801ff-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="801ff-154">Estado de la impresora \_ \_ tóner \_ bajo</span><span class="sxs-lookup"><span data-stu-id="801ff-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="801ff-155">La impresora tiene poco tóner.</span><span class="sxs-lookup"><span data-stu-id="801ff-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="801ff-156">Estado de la impresora- \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="801ff-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="801ff-157">La impresora tiene un error que requiere que el usuario haga algo.</span><span class="sxs-lookup"><span data-stu-id="801ff-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="801ff-158">Estado de la impresora en \_ \_ espera</span><span class="sxs-lookup"><span data-stu-id="801ff-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="801ff-159">La impresora está en espera.</span><span class="sxs-lookup"><span data-stu-id="801ff-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="801ff-160">\_preparación del \_ estado \_ de la impresora</span><span class="sxs-lookup"><span data-stu-id="801ff-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="801ff-161">La impresora se está preparando.</span><span class="sxs-lookup"><span data-stu-id="801ff-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="801ff-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="801ff-162">Requirements</span></span>



| <span data-ttu-id="801ff-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="801ff-163">Requirement</span></span> | <span data-ttu-id="801ff-164">Value</span><span class="sxs-lookup"><span data-stu-id="801ff-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801ff-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="801ff-165">Minimum supported client</span></span><br/> | <span data-ttu-id="801ff-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="801ff-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="801ff-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="801ff-167">Minimum supported server</span></span><br/> | <span data-ttu-id="801ff-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="801ff-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="801ff-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="801ff-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="801ff-170"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="801ff-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="801ff-171">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="801ff-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="801ff-172">Información de la **\_ impresora \_ \_ 6W** (Unicode) y la información de la **\_ impresora \_ \_ 6A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="801ff-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="801ff-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="801ff-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801ff-174">Impresión</span><span class="sxs-lookup"><span data-stu-id="801ff-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="801ff-175">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="801ff-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="801ff-176">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="801ff-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="801ff-177">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="801ff-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="801ff-178">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="801ff-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="801ff-179">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="801ff-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="801ff-180">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="801ff-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="801ff-181">**Información de la impresora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="801ff-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




