---
description: La estructura de la información de la impresora \_ \_ 5 especifica información detallada de la impresora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Estructura de PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720616"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="03c7e-103">Estructura de la información de la impresora \_ \_ 5</span><span class="sxs-lookup"><span data-stu-id="03c7e-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="03c7e-104">La estructura de la información de la **impresora \_ \_ 5** especifica información detallada de la impresora.</span><span class="sxs-lookup"><span data-stu-id="03c7e-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c7e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="03c7e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="03c7e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03c7e-107">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="03c7e-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="03c7e-108">Puntero a una cadena terminada en null que especifica el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="03c7e-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="03c7e-109">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="03c7e-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="03c7e-110">Puntero a una cadena terminada en null que identifica los puertos utilizados para transmitir datos a la impresora.</span><span class="sxs-lookup"><span data-stu-id="03c7e-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="03c7e-111">Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="03c7e-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="03c7e-112">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="03c7e-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="03c7e-113">Atributos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="03c7e-113">The printer attributes.</span></span> <span data-ttu-id="03c7e-114">Este miembro puede ser cualquier combinación razonable de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="03c7e-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="03c7e-115">Value</span><span class="sxs-lookup"><span data-stu-id="03c7e-115">Value</span></span>                                   | <span data-ttu-id="03c7e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="03c7e-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c7e-117">atributo de impresora \_ \_ directo</span><span class="sxs-lookup"><span data-stu-id="03c7e-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="03c7e-118">El trabajo se envía directamente a la impresora (no se pone en cola).</span><span class="sxs-lookup"><span data-stu-id="03c7e-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="03c7e-119">el atributo de impresora se \_ \_ \_ completa \_ primero</span><span class="sxs-lookup"><span data-stu-id="03c7e-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="03c7e-120">Si se establece set y Printer para la puesta en cola de impresión, los trabajos que hayan finalizado la cola de impresión estarán programados para imprimirse antes que los trabajos que no hayan completado la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="03c7e-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="03c7e-121">atributo de impresora- \_ \_ habilitar \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="03c7e-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="03c7e-122">Si se establece, se llama a **DevQueryPrint** .</span><span class="sxs-lookup"><span data-stu-id="03c7e-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="03c7e-123">**DevQueryPrint** puede producir un error si las configuraciones de documento e impresora no coinciden.</span><span class="sxs-lookup"><span data-stu-id="03c7e-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="03c7e-124">Si se establece esta marca, se mantendrán los documentos no coincidentes en la cola.</span><span class="sxs-lookup"><span data-stu-id="03c7e-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="03c7e-125">atributo de impresora \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="03c7e-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="03c7e-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="03c7e-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="03c7e-127">atributo de impresora \_ \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="03c7e-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="03c7e-128">Si se establece, los trabajos se mantienen una vez que se imprimen.</span><span class="sxs-lookup"><span data-stu-id="03c7e-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="03c7e-129">Si no se anula, se eliminan los trabajos.</span><span class="sxs-lookup"><span data-stu-id="03c7e-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="03c7e-130">atributo de impresora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="03c7e-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="03c7e-131">La impresora es una impresora local.</span><span class="sxs-lookup"><span data-stu-id="03c7e-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="03c7e-132">\_red de atributos de impresora \_</span><span class="sxs-lookup"><span data-stu-id="03c7e-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="03c7e-133">La impresora es una conexión de impresora de red.</span><span class="sxs-lookup"><span data-stu-id="03c7e-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="03c7e-134">atributo de impresora \_ \_ publicado</span><span class="sxs-lookup"><span data-stu-id="03c7e-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="03c7e-135">Indica si la impresora está publicada en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="03c7e-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="03c7e-136">atributo de impresora \_ \_ en cola</span><span class="sxs-lookup"><span data-stu-id="03c7e-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="03c7e-137">Si se establece, la impresora se pone en cola y comienza la impresión después de que la última página se haya puesto en cola.</span><span class="sxs-lookup"><span data-stu-id="03c7e-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="03c7e-138">Si no se establece y \_ \_ no se establece el atributo de impresora Direct, la impresora se pone en cola y se imprime durante la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="03c7e-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="03c7e-139">atributo de impresora \_ \_ solo sin formato \_</span><span class="sxs-lookup"><span data-stu-id="03c7e-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="03c7e-140">Indica que solo se pueden poner en cola los trabajos de impresión de tipo de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="03c7e-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="03c7e-141">atributo de impresora \_ \_ compartido</span><span class="sxs-lookup"><span data-stu-id="03c7e-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="03c7e-142">La impresora está compartida.</span><span class="sxs-lookup"><span data-stu-id="03c7e-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="03c7e-143">En Windows XP y versiones posteriores de Windows, también se puede usar el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="03c7e-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="03c7e-144">Value</span><span class="sxs-lookup"><span data-stu-id="03c7e-144">Value</span></span>                   | <span data-ttu-id="03c7e-145">Significado</span><span class="sxs-lookup"><span data-stu-id="03c7e-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c7e-146">\_fax de atributo de impresora \_</span><span class="sxs-lookup"><span data-stu-id="03c7e-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="03c7e-147">Si se establece, la impresora es una impresora de fax.</span><span class="sxs-lookup"><span data-stu-id="03c7e-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="03c7e-148">Solo se puede establecer mediante [**AddPrinter (**](addprinter.md), pero puede ser recuperado por [**EnumPrinters**](enumprinters.md) y [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="03c7e-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="03c7e-149">En Windows Vista y versiones posteriores de Windows, también se pueden usar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="03c7e-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="03c7e-150">Value</span><span class="sxs-lookup"><span data-stu-id="03c7e-150">Value</span></span>                               | <span data-ttu-id="03c7e-151">Significado</span><span class="sxs-lookup"><span data-stu-id="03c7e-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03c7e-152">\_ \_ nombre descriptivo del atributo de impresora \_</span><span class="sxs-lookup"><span data-stu-id="03c7e-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="03c7e-153">Un equipo se ha conectado a esta impresora y se le ha dado un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="03c7e-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="03c7e-154">\_máquina de atributos de impresora \_</span><span class="sxs-lookup"><span data-stu-id="03c7e-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="03c7e-155">La impresora es una conexión por equipo.</span><span class="sxs-lookup"><span data-stu-id="03c7e-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="03c7e-156">atributo de impresora \_ \_ Push \_ User</span><span class="sxs-lookup"><span data-stu-id="03c7e-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="03c7e-157">La impresora se instaló mediante la Directiva de usuario de las conexiones de impresión de la impresora.</span><span class="sxs-lookup"><span data-stu-id="03c7e-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="03c7e-158">el \_ atributo de impresora \_ insertó el \_ equipo</span><span class="sxs-lookup"><span data-stu-id="03c7e-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="03c7e-159">La impresora se instaló mediante la Directiva de equipo de las conexiones de impresión de extracción.</span><span class="sxs-lookup"><span data-stu-id="03c7e-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="03c7e-160">**DeviceNotSelectedTimeout**</span><span class="sxs-lookup"><span data-stu-id="03c7e-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="03c7e-161">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="03c7e-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03c7e-162">**TransmissionRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="03c7e-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="03c7e-163">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="03c7e-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03c7e-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c7e-164">Requirements</span></span>



| <span data-ttu-id="03c7e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c7e-165">Requirement</span></span> | <span data-ttu-id="03c7e-166">Value</span><span class="sxs-lookup"><span data-stu-id="03c7e-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c7e-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c7e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="03c7e-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03c7e-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="03c7e-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c7e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="03c7e-170">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03c7e-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="03c7e-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03c7e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c7e-172"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03c7e-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="03c7e-173">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="03c7e-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03c7e-174">Información de la **\_ impresora \_ \_ 5W** (Unicode) e información de la **\_ impresora \_ \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03c7e-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="03c7e-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="03c7e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c7e-176">Impresión</span><span class="sxs-lookup"><span data-stu-id="03c7e-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="03c7e-177">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="03c7e-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="03c7e-178">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="03c7e-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="03c7e-179">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="03c7e-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="03c7e-180">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="03c7e-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="03c7e-181">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="03c7e-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="03c7e-182">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="03c7e-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="03c7e-183">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="03c7e-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="03c7e-184">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="03c7e-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




