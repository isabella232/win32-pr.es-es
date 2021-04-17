---
description: La estructura de la información de la impresora \_ \_ 2 especifica información detallada de la impresora.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Estructura de PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546366"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="8ae2a-103">Estructura de la información de la impresora \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="8ae2a-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="8ae2a-104">La estructura de la información de la **impresora \_ \_ 2** especifica información detallada de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ae2a-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="8ae2a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ae2a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ae2a-107">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-108">Puntero a una cadena terminada en null que identifica el servidor que controla la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="8ae2a-109">Si esta cadena es **null**, la impresora se controla localmente.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-110">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-111">Puntero a una cadena terminada en null que especifica el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-112">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-113">Puntero a una cadena terminada en null que identifica el punto de recurso compartido de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="8ae2a-114">(Esta cadena solo se usa si la impresora \_ \_Se estableció una constante compartida de atributo para el miembro **attributes** .)</span><span class="sxs-lookup"><span data-stu-id="8ae2a-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-115">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-116">Puntero a una cadena terminada en null que identifica los puertos utilizados para transmitir datos a la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="8ae2a-117">Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="8ae2a-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-118">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-119">Puntero a una cadena terminada en null que especifica el nombre del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-120">**pComment**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-121">Un puntero a una cadena terminada en null que proporciona una breve descripción de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-123">Un puntero a una cadena terminada en null que especifica la ubicación física de la impresora (por ejemplo, "Bldg.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="8ae2a-124">38, habitación 1164 ").</span><span class="sxs-lookup"><span data-stu-id="8ae2a-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-125">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-126">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados, como la orientación del papel y la resolución.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-127">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-128">Un puntero a una cadena terminada en null que especifica el nombre del archivo que se usa para crear la página del separador.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="8ae2a-129">Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-130">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-131">Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión utilizado por la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="8ae2a-132">Puede usar la función [**EnumPrintProcessors**](enumprintprocessors.md) para obtener una lista de procesadores de impresión instalados en un servidor.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-133">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-134">Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="8ae2a-135">Puede usar la función [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para obtener una lista de tipos de datos admitidos por un procesador de impresión específico.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-137">Puntero a una cadena terminada en null que especifica los parámetros predeterminados del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-138">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-139">Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="8ae2a-140">Este miembro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-141">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-142">Atributos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-142">The printer attributes.</span></span> <span data-ttu-id="8ae2a-143">Este miembro puede ser cualquier combinación razonable de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="8ae2a-144">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-144">Value</span></span>                                   | <span data-ttu-id="8ae2a-145">Significado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-146">atributo de impresora \_ \_ directo</span><span class="sxs-lookup"><span data-stu-id="8ae2a-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="8ae2a-147">El trabajo se envía directamente a la impresora (no se pone en cola).</span><span class="sxs-lookup"><span data-stu-id="8ae2a-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="8ae2a-148">el atributo de impresora se \_ \_ \_ completa \_ primero</span><span class="sxs-lookup"><span data-stu-id="8ae2a-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="8ae2a-149">Si se establece set y Printer para la puesta en cola de impresión, los trabajos que hayan finalizado la cola de impresión estarán programados para imprimirse antes que los trabajos que no hayan completado la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="8ae2a-150">atributo de impresora- \_ \_ habilitar \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="8ae2a-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="8ae2a-151">Si se establece, se llama a **DevQueryPrint** .</span><span class="sxs-lookup"><span data-stu-id="8ae2a-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="8ae2a-152">**DevQueryPrint** puede producir un error si las configuraciones de documento e impresora no coinciden.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="8ae2a-153">Si se establece esta marca, se mantendrán los documentos no coincidentes en la cola.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="8ae2a-154">atributo de impresora \_ \_ oculto</span><span class="sxs-lookup"><span data-stu-id="8ae2a-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="8ae2a-155">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="8ae2a-156">atributo de impresora \_ \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="8ae2a-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="8ae2a-157">Si se establece, los trabajos se mantienen una vez que se imprimen.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="8ae2a-158">Si no se anula, se eliminan los trabajos.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="8ae2a-159">atributo de impresora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="8ae2a-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="8ae2a-160">La impresora es una impresora local.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="8ae2a-161">\_red de atributos de impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="8ae2a-162">La impresora es una conexión de impresora de red.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="8ae2a-163">atributo de impresora \_ \_ publicado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="8ae2a-164">Indica si la impresora está publicada en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="8ae2a-165">atributo de impresora \_ \_ en cola</span><span class="sxs-lookup"><span data-stu-id="8ae2a-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="8ae2a-166">Si se establece, la impresora se pone en cola y comienza la impresión después de que la última página se haya puesto en cola.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="8ae2a-167">Si no se establece y \_ \_ no se establece el atributo de impresora Direct, la impresora se pone en cola y se imprime durante la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="8ae2a-168">atributo de impresora \_ \_ solo sin formato \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="8ae2a-169">Indica que solo se pueden poner en cola los trabajos de impresión de tipo de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="8ae2a-170">atributo de impresora \_ \_ compartido</span><span class="sxs-lookup"><span data-stu-id="8ae2a-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="8ae2a-171">La impresora está compartida.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="8ae2a-172">En Windows XP y versiones posteriores de Windows, también se puede usar el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="8ae2a-173">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-173">Value</span></span>                   | <span data-ttu-id="8ae2a-174">Significado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-175">\_fax de atributo de impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="8ae2a-176">Si se establece, la impresora es una impresora de fax.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="8ae2a-177">Solo se puede establecer mediante [**AddPrinter (**](addprinter.md), pero puede ser recuperado por [**EnumPrinters**](enumprinters.md) y [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="8ae2a-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="8ae2a-178">En Windows Vista y versiones posteriores de Windows, también se pueden usar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="8ae2a-179">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-179">Value</span></span>                               | <span data-ttu-id="8ae2a-180">Significado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-181">\_ \_ nombre descriptivo del atributo de impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="8ae2a-182">Un equipo se ha conectado a esta impresora y se le ha dado un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="8ae2a-183">\_máquina de atributos de impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="8ae2a-184">La impresora es una conexión por equipo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="8ae2a-185">atributo de impresora \_ \_ Push \_ User</span><span class="sxs-lookup"><span data-stu-id="8ae2a-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="8ae2a-186">La impresora se instaló mediante la Directiva de usuario de las conexiones de impresión de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="8ae2a-187">el \_ atributo de impresora \_ insertó el \_ equipo</span><span class="sxs-lookup"><span data-stu-id="8ae2a-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="8ae2a-188">La impresora se instaló mediante la Directiva de equipo de las conexiones de impresión de extracción.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="8ae2a-189">En Windows Server 2003, también se puede usar el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="8ae2a-190">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-190">Value</span></span>                  | <span data-ttu-id="8ae2a-191">Significado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-192">atributo de impresora \_ \_ TS</span><span class="sxs-lookup"><span data-stu-id="8ae2a-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="8ae2a-193">Indica que la impresora está conectada actualmente a través de un servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8ae2a-194">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-195">Valor de prioridad que el administrador de trabajos de impresión utiliza para enrutar los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-196">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-197">Valor de prioridad predeterminado asignado a cada trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-199">La primera hora en la que la impresora imprimirá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="8ae2a-200">Este valor se expresa como minutos transcurridos desde 12:00 AM GMT (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="8ae2a-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-202">La hora más reciente a la que la impresora imprimirá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="8ae2a-203">Este valor se expresa como minutos transcurridos desde 12:00 AM GMT (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="8ae2a-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-204">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-205">El estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-205">The printer status.</span></span> <span data-ttu-id="8ae2a-206">Este miembro puede ser cualquier combinación razonable de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="8ae2a-207">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-207">Value</span></span>                               | <span data-ttu-id="8ae2a-208">Significado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-209">Estado de la impresora \_ \_ ocupado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="8ae2a-210">La impresora está ocupada.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="8ae2a-211">puerta de estado de la impresora \_ \_ \_ abierta</span><span class="sxs-lookup"><span data-stu-id="8ae2a-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="8ae2a-212">La puerta de la impresora está abierta.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="8ae2a-213">\_error de estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="8ae2a-214">La impresora está en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="8ae2a-215">Estado de la impresora \_ \_ inicializando</span><span class="sxs-lookup"><span data-stu-id="8ae2a-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="8ae2a-216">La impresora se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="8ae2a-217">\_e/s de estado de impresora \_ \_ activa</span><span class="sxs-lookup"><span data-stu-id="8ae2a-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="8ae2a-218">La impresora está en un estado de entrada/salida activo</span><span class="sxs-lookup"><span data-stu-id="8ae2a-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="8ae2a-219">\_ \_ alimentación manual de estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="8ae2a-220">La impresora está en un estado de alimentación manual.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="8ae2a-221">Estado de la impresora \_ \_ sin \_ tóner</span><span class="sxs-lookup"><span data-stu-id="8ae2a-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="8ae2a-222">Se ha agotado el tóner de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="8ae2a-223">Estado de la impresora \_ \_ no \_ disponible</span><span class="sxs-lookup"><span data-stu-id="8ae2a-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="8ae2a-224">La impresora no está disponible para imprimir.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="8ae2a-225">Estado de la impresora \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="8ae2a-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="8ae2a-226">La impresora no está conectada.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="8ae2a-227">\_Estado de la impresora \_ sin \_ \_ memoria</span><span class="sxs-lookup"><span data-stu-id="8ae2a-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="8ae2a-228">La impresora se ha quedado sin memoria.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="8ae2a-229">bandeja de salida de estado de la impresora \_ \_ \_ \_ llena</span><span class="sxs-lookup"><span data-stu-id="8ae2a-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="8ae2a-230">La bandeja de salida de la impresora está llena.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="8ae2a-231">Página de estado de la impresora \_ \_ \_ aparcan</span><span class="sxs-lookup"><span data-stu-id="8ae2a-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="8ae2a-232">La impresora no puede imprimir la página actual.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="8ae2a-233">\_atasco de \_ papel del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="8ae2a-234">El papel está atascado en la impresora</span><span class="sxs-lookup"><span data-stu-id="8ae2a-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="8ae2a-235">\_papel del estado de la impresora \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="8ae2a-236">La impresora se ha quedado sin papel.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="8ae2a-237">\_problema de \_ papel del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="8ae2a-238">La impresora tiene un problema de papel.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="8ae2a-239">Estado de la impresora en \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="8ae2a-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="8ae2a-240">La impresora está en pausa.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="8ae2a-241">Estado de la impresora \_ \_ pendiente de \_ eliminación</span><span class="sxs-lookup"><span data-stu-id="8ae2a-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="8ae2a-242">La impresora se está eliminando.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="8ae2a-243">Estado de la impresora- \_ \_ \_ guardar energía</span><span class="sxs-lookup"><span data-stu-id="8ae2a-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="8ae2a-244">La impresora está en modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="8ae2a-245">\_impresión del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="8ae2a-246">La impresora se está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="8ae2a-247">\_procesamiento del estado de la impresora \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="8ae2a-248">La impresora está procesando un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="8ae2a-249">servidor de estado de impresora \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="8ae2a-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="8ae2a-250">No se conoce el estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="8ae2a-251">Estado de la impresora \_ \_ tóner \_ bajo</span><span class="sxs-lookup"><span data-stu-id="8ae2a-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="8ae2a-252">La impresora tiene poco tóner.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="8ae2a-253">Estado de la impresora- \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="8ae2a-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="8ae2a-254">La impresora tiene un error que requiere que el usuario haga algo.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="8ae2a-255">Estado de la impresora en \_ \_ espera</span><span class="sxs-lookup"><span data-stu-id="8ae2a-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="8ae2a-256">La impresora está en espera.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="8ae2a-257">\_preparación del \_ estado \_ de la impresora</span><span class="sxs-lookup"><span data-stu-id="8ae2a-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="8ae2a-258">La impresora se está preparando.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="8ae2a-259">**cJobs**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-260">El número de trabajos de impresión que se han puesto en cola para la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="8ae2a-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="8ae2a-262">Número medio de páginas por minuto que se han impreso en la impresora.</span><span class="sxs-lookup"><span data-stu-id="8ae2a-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ae2a-263">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ae2a-263">Requirements</span></span>



| <span data-ttu-id="8ae2a-264">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae2a-264">Requirement</span></span> | <span data-ttu-id="8ae2a-265">Value</span><span class="sxs-lookup"><span data-stu-id="8ae2a-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae2a-266">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ae2a-266">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae2a-267">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ae2a-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ae2a-268">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ae2a-268">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae2a-269">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ae2a-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ae2a-270">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ae2a-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ae2a-271"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae2a-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8ae2a-272">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8ae2a-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8ae2a-273">Información de la **\_ impresora \_ \_ 2W** (Unicode) y la información de la **\_ impresora \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8ae2a-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="8ae2a-274">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ae2a-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae2a-275">Impresión</span><span class="sxs-lookup"><span data-stu-id="8ae2a-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-276">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8ae2a-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="8ae2a-278">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-279">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-280">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-281">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="8ae2a-282">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="8ae2a-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

