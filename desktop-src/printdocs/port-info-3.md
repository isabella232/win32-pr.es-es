---
description: La \_ \_ estructura de la información de puerto 3 especifica el valor de estado de un puerto de impresora.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Estructura de PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706301"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="8669b-103">Estructura de la información de puerto \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="8669b-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="8669b-104">La estructura de la **información de puerto \_ \_ 3** especifica el valor de estado de un puerto de impresora.</span><span class="sxs-lookup"><span data-stu-id="8669b-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="8669b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8669b-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="8669b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8669b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8669b-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="8669b-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8669b-108">Nuevo valor de estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="8669b-108">The new port status value.</span></span> <span data-ttu-id="8669b-109">Este valor se usa solo si el miembro **pszStatus** es **null**.</span><span class="sxs-lookup"><span data-stu-id="8669b-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="8669b-110">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8669b-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="8669b-111">Value</span><span class="sxs-lookup"><span data-stu-id="8669b-111">Value</span></span>                            | <span data-ttu-id="8669b-112">Significado</span><span class="sxs-lookup"><span data-stu-id="8669b-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="8669b-113">0</span><span class="sxs-lookup"><span data-stu-id="8669b-113">0</span></span>                                | <span data-ttu-id="8669b-114">Borra el estado del puerto de impresora.</span><span class="sxs-lookup"><span data-stu-id="8669b-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="8669b-115">Estado de puerto \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="8669b-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="8669b-116">La impresora del puerto está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8669b-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="8669b-117">\_atasco de \_ papel de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="8669b-118">La impresora del puerto tiene un atasco de papel.</span><span class="sxs-lookup"><span data-stu-id="8669b-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="8669b-119">\_papel del estado del puerto \_ \_</span><span class="sxs-lookup"><span data-stu-id="8669b-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="8669b-120">La impresora del puerto no tiene papel.</span><span class="sxs-lookup"><span data-stu-id="8669b-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="8669b-121">bandeja de salida de estado de puerto \_ \_ \_ \_ llena</span><span class="sxs-lookup"><span data-stu-id="8669b-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="8669b-122">La bandeja de salida de printer's del puerto está llena.</span><span class="sxs-lookup"><span data-stu-id="8669b-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="8669b-123">\_problema de \_ papel de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="8669b-124">La impresora del puerto tiene un problema de papel.</span><span class="sxs-lookup"><span data-stu-id="8669b-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="8669b-125">Estado de puerto \_ \_ sin \_ tóner</span><span class="sxs-lookup"><span data-stu-id="8669b-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="8669b-126">La impresora del puerto no tiene tóner.</span><span class="sxs-lookup"><span data-stu-id="8669b-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="8669b-127">Estado de puerto \_ \_ puerta \_ abierta</span><span class="sxs-lookup"><span data-stu-id="8669b-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="8669b-128">La puerta de la impresora del puerto está abierta.</span><span class="sxs-lookup"><span data-stu-id="8669b-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="8669b-129">Estado del puerto de \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="8669b-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="8669b-130">La impresora del puerto requiere la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8669b-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="8669b-131">\_estado \_ de puerto \_ de \_ memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="8669b-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="8669b-132">La impresora del puerto no tiene memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="8669b-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="8669b-133">tóner de estado de puerto \_ \_ \_ bajo</span><span class="sxs-lookup"><span data-stu-id="8669b-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="8669b-134">La impresora del puerto tiene poco tóner.</span><span class="sxs-lookup"><span data-stu-id="8669b-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="8669b-135">\_preparación del \_ estado \_ de los puertos</span><span class="sxs-lookup"><span data-stu-id="8669b-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="8669b-136">La impresora del puerto se está preparando.</span><span class="sxs-lookup"><span data-stu-id="8669b-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="8669b-137">\_ahorro de \_ energía de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="8669b-138">La impresora del puerto está en modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="8669b-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8669b-139">**pszStatus**</span><span class="sxs-lookup"><span data-stu-id="8669b-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8669b-140">Puntero a una nueva cadena de valor de estado del puerto de impresora que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="8669b-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="8669b-141">Utilice este miembro si no hay ningún valor de estado adecuado entre los enumerados para **dwStatus**.</span><span class="sxs-lookup"><span data-stu-id="8669b-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="8669b-142">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="8669b-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="8669b-143">La gravedad del valor de estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="8669b-143">The severity of the port status value.</span></span>

<span data-ttu-id="8669b-144">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8669b-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="8669b-145">Value</span><span class="sxs-lookup"><span data-stu-id="8669b-145">Value</span></span>                       | <span data-ttu-id="8669b-146">Significado</span><span class="sxs-lookup"><span data-stu-id="8669b-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="8669b-147">\_error de \_ tipo de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="8669b-148">El valor de estado del puerto indica un error.</span><span class="sxs-lookup"><span data-stu-id="8669b-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="8669b-149">\_Advertencia de \_ tipo de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="8669b-150">El valor de estado del puerto es una advertencia.</span><span class="sxs-lookup"><span data-stu-id="8669b-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="8669b-151">\_información de \_ tipo de estado de puerto \_</span><span class="sxs-lookup"><span data-stu-id="8669b-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="8669b-152">El valor del estado del puerto es informativo.</span><span class="sxs-lookup"><span data-stu-id="8669b-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8669b-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8669b-153">Remarks</span></span>

<span data-ttu-id="8669b-154">Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad puerto de \_ \_ tipo \_ error, el administrador de trabajos de impresión deja de enviar trabajos al puerto.</span><span class="sxs-lookup"><span data-stu-id="8669b-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="8669b-155">El administrador de trabajos de impresión no reanuda el envío de trabajos al puerto hasta que se realice otra llamada a [**SetPort**](setport.md) para borrar el estado.</span><span class="sxs-lookup"><span data-stu-id="8669b-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="8669b-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8669b-156">Requirements</span></span>



| <span data-ttu-id="8669b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8669b-157">Requirement</span></span> | <span data-ttu-id="8669b-158">Value</span><span class="sxs-lookup"><span data-stu-id="8669b-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8669b-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8669b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8669b-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8669b-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8669b-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8669b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8669b-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8669b-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8669b-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8669b-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8669b-164"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8669b-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8669b-165">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8669b-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8669b-166">Info. de **\_ Puerto \_ \_ 3W** (Unicode) y la **\_ información de puerto \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8669b-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="8669b-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="8669b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8669b-168">Impresión</span><span class="sxs-lookup"><span data-stu-id="8669b-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8669b-169">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8669b-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8669b-170">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="8669b-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




