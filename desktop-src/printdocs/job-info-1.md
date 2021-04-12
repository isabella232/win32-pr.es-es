---
description: La \_ estructura Job info \_ 1 especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se pone en cola el trabajo, el nombre del equipo que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, etc.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Estructura de JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361415"
---
# <a name="job_info_1-structure"></a><span data-ttu-id="f059e-103">Estructura de información de trabajo \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="f059e-103">JOB\_INFO\_1 structure</span></span>

<span data-ttu-id="f059e-104">La estructura **Job \_ info \_ 1** especifica información del trabajo de impresión, como el valor del identificador de trabajo, el nombre de la impresora para la que se pone en cola el trabajo, el nombre del equipo que creó el trabajo de impresión, el nombre del usuario que posee el trabajo de impresión, etc.</span><span class="sxs-lookup"><span data-stu-id="f059e-104">The **JOB\_INFO\_1** structure specifies print-job information such as the job-identifier value, the name of the printer for which the job is spooled, the name of the machine that created the print job, the name of the user that owns the print job, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="f059e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f059e-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="f059e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f059e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f059e-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="f059e-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-108">Identificador del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-108">A job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="f059e-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-110">Puntero a una cadena terminada en null que especifica el nombre de la impresora para la que se pone en cola el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="f059e-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-112">Puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="f059e-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-114">Puntero a una cadena terminada en null que especifica el nombre del usuario al que pertenece el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-114">A pointer to a null-terminated string that specifies the name of the user that owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="f059e-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-116">Un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="f059e-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="f059e-117">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="f059e-117">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-118">Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-118">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-119">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="f059e-119">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-120">Puntero a una cadena terminada en null que especifica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-120">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="f059e-121">Este miembro debe comprobarse antes del *Estado* y, si *pStatus* es **null**, el estado se define mediante el contenido del miembro status.</span><span class="sxs-lookup"><span data-stu-id="f059e-121">This member should be checked prior to *Status* and, if *pStatus* is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-122">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f059e-122">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-123">El estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-123">The job status.</span></span> <span data-ttu-id="f059e-124">El valor de este miembro puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f059e-124">The value of this member can be zero or a combination of one or more of the following values.</span></span> <span data-ttu-id="f059e-125">Un valor de cero indica que la cola de impresión se pausó una vez finalizada la cola de impresión del documento.</span><span class="sxs-lookup"><span data-stu-id="f059e-125">A value of zero indicates that the print queue was paused after the document finished spooling.</span></span>



| <span data-ttu-id="f059e-126">Value</span><span class="sxs-lookup"><span data-stu-id="f059e-126">Value</span></span>                           | <span data-ttu-id="f059e-127">Significado</span><span class="sxs-lookup"><span data-stu-id="f059e-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f059e-128">Estado del trabajo \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="f059e-128">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="f059e-129">El controlador no puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-129">The driver cannot print the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f059e-130">Estado del trabajo \_ \_ completado</span><span class="sxs-lookup"><span data-stu-id="f059e-130">JOB\_STATUS\_COMPLETE</span></span>           | <span data-ttu-id="f059e-131">**Windows XP y versiones posteriores:** El trabajo se envía a la impresora, pero es posible que el trabajo no se imprima todavía.</span><span class="sxs-lookup"><span data-stu-id="f059e-131">**Windows XP and later:** Job is sent to the printer, but the job may not be printed yet.</span></span><br/> <span data-ttu-id="f059e-132">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f059e-132">See Remarks for more information.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f059e-133">Estado del trabajo \_ \_ eliminado</span><span class="sxs-lookup"><span data-stu-id="f059e-133">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="f059e-134">El trabajo se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="f059e-134">Job has been deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f059e-135">\_eliminación de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f059e-135">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="f059e-136">Se está eliminando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-136">Job is being deleted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f059e-137">\_error de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f059e-137">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="f059e-138">Se ha asociado un error al trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-138">An error is associated with the job.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f059e-139">Estado del trabajo \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="f059e-139">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="f059e-140">La impresora está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f059e-140">Printer is offline.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f059e-141">Estado del trabajo \_ \_ PAPEROUT</span><span class="sxs-lookup"><span data-stu-id="f059e-141">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="f059e-142">La impresora no tiene papel.</span><span class="sxs-lookup"><span data-stu-id="f059e-142">Printer is out of paper.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f059e-143">Estado del trabajo en \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="f059e-143">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="f059e-144">El trabajo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="f059e-144">Job is paused.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f059e-145">Estado del trabajo \_ \_ impreso</span><span class="sxs-lookup"><span data-stu-id="f059e-145">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="f059e-146">El trabajo se ha impreso.</span><span class="sxs-lookup"><span data-stu-id="f059e-146">Job has printed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f059e-147">\_impresión de estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f059e-147">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="f059e-148">El trabajo está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="f059e-148">Job is printing.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f059e-149">reinicio del estado del trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f059e-149">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="f059e-150">El trabajo se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="f059e-150">Job has been restarted.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f059e-151">Estado del trabajo \_ \_ retenido</span><span class="sxs-lookup"><span data-stu-id="f059e-151">JOB\_STATUS\_RETAINED</span></span>           | <span data-ttu-id="f059e-152">**Windows Vista y versiones posteriores:** El trabajo se ha conservado en la cola de impresión y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="f059e-152">**Windows Vista and later:** Job has been retained in the print queue and cannot be deleted.</span></span> <span data-ttu-id="f059e-153">Esto puede deberse a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f059e-153">This can be caused by the following:</span></span><br/> <span data-ttu-id="f059e-154">1) el trabajo se reservó manualmente mediante una llamada a SetJob y el administrador de trabajos de impresión está esperando a que se libere el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-154">1) The job was manually retained by a call to SetJob and the spooler is waiting for the job to be released.</span></span><br/> <span data-ttu-id="f059e-155">2) el trabajo no ha terminado la impresión y debe finalizar la impresión antes de que se pueda eliminar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f059e-155">2) The job has not finished printing and must finish printing before it can be automatically deleted.</span></span><br/> <span data-ttu-id="f059e-156">Vea [**SetJob**](setjob.md) para obtener más información acerca de los comandos de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-156">See [**SetJob**](setjob.md) for more information about print job commands.</span></span><br/> |
| <span data-ttu-id="f059e-157">puesta en cola del \_ Estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f059e-157">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="f059e-158">El trabajo está en cola.</span><span class="sxs-lookup"><span data-stu-id="f059e-158">Job is spooling.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f059e-159">Estado del trabajo de \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="f059e-159">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="f059e-160">La impresora tiene un error que requiere que el usuario haga algo.</span><span class="sxs-lookup"><span data-stu-id="f059e-160">Printer has an error that requires the user to do something.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="f059e-161">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="f059e-161">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-162">La prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f059e-162">The job priority.</span></span> <span data-ttu-id="f059e-163">Este miembro puede ser uno de los valores siguientes o estar en el intervalo comprendido entre 1 y 99 ( \_ prioridad mínima a través de la \_ prioridad máxima).</span><span class="sxs-lookup"><span data-stu-id="f059e-163">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="f059e-164">Value</span><span class="sxs-lookup"><span data-stu-id="f059e-164">Value</span></span>         | <span data-ttu-id="f059e-165">Significado</span><span class="sxs-lookup"><span data-stu-id="f059e-165">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="f059e-166">\_prioridad mínima</span><span class="sxs-lookup"><span data-stu-id="f059e-166">MIN\_PRIORITY</span></span> | <span data-ttu-id="f059e-167">Prioridad mínima.</span><span class="sxs-lookup"><span data-stu-id="f059e-167">Minimum priority.</span></span> |
| <span data-ttu-id="f059e-168">\_prioridad máxima</span><span class="sxs-lookup"><span data-stu-id="f059e-168">MAX\_PRIORITY</span></span> | <span data-ttu-id="f059e-169">Prioridad máxima.</span><span class="sxs-lookup"><span data-stu-id="f059e-169">Maximum priority.</span></span> |
| <span data-ttu-id="f059e-170">prioridad de DEF \_</span><span class="sxs-lookup"><span data-stu-id="f059e-170">DEF\_PRIORITY</span></span> | <span data-ttu-id="f059e-171">Prioridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f059e-171">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f059e-172">**Position**</span><span class="sxs-lookup"><span data-stu-id="f059e-172">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-173">Posición del trabajo en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="f059e-173">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-174">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="f059e-174">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-175">Número total de páginas que contiene el documento.</span><span class="sxs-lookup"><span data-stu-id="f059e-175">The total number of pages that the document contains.</span></span> <span data-ttu-id="f059e-176">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="f059e-176">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-177">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="f059e-177">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-178">Número de páginas que se han imprimido.</span><span class="sxs-lookup"><span data-stu-id="f059e-178">The number of pages that have printed.</span></span> <span data-ttu-id="f059e-179">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="f059e-179">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="f059e-180">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="f059e-180">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="f059e-181">Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora A la que se puso en cola este documento.</span><span class="sxs-lookup"><span data-stu-id="f059e-181">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time that this document was spooled.</span></span>

<span data-ttu-id="f059e-182">Este valor de hora está en formato de horario universal coordinado (UTC).</span><span class="sxs-lookup"><span data-stu-id="f059e-182">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="f059e-183">Debe convertirlo en un valor de hora local antes de mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="f059e-183">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="f059e-184">Puede usar la función [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="f059e-184">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f059e-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f059e-185">Remarks</span></span>

<span data-ttu-id="f059e-186">Los monitores de puerto que no son compatibles con TrueEndOfJob establecerán el trabajo como \_ estado \_ del trabajo impreso justo después de enviar el trabajo a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f059e-186">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f059e-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f059e-187">Requirements</span></span>



| <span data-ttu-id="f059e-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="f059e-188">Requirement</span></span> | <span data-ttu-id="f059e-189">Value</span><span class="sxs-lookup"><span data-stu-id="f059e-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f059e-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f059e-190">Minimum supported client</span></span><br/> | <span data-ttu-id="f059e-191">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f059e-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f059e-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f059e-192">Minimum supported server</span></span><br/> | <span data-ttu-id="f059e-193">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f059e-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f059e-194">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f059e-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="f059e-195"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f059e-195"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f059e-196">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f059e-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f059e-197">**\_ Información del trabajo \_ \_ 1W** (Unicode) y la **\_ información del trabajo \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f059e-197">**\_JOB\_INFO\_1W** (Unicode) and **\_JOB\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="f059e-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="f059e-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f059e-199">Impresión</span><span class="sxs-lookup"><span data-stu-id="f059e-199">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f059e-200">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f059e-200">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f059e-201">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="f059e-201">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="f059e-202">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="f059e-202">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="f059e-203">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="f059e-203">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

