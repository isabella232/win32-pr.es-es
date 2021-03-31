---
description: La \_ estructura Job info \_ 2 describe un conjunto completo de valores asociados a un trabajo.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Estructura de JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279025"
---
# <a name="job_info_2-structure"></a><span data-ttu-id="2871b-103">Estructura de información de trabajo \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="2871b-103">JOB\_INFO\_2 structure</span></span>

<span data-ttu-id="2871b-104">La estructura **Job \_ info \_ 2** describe un conjunto completo de valores asociados a un trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-104">The **JOB\_INFO\_2** structure describes a full set of values associated with a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2871b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2871b-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a><span data-ttu-id="2871b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2871b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2871b-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="2871b-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-108">Un valor de identificador de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="2871b-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-110">Puntero a una cadena terminada en null que especifica el nombre de la impresora para la que se pone en cola el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="2871b-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-112">Puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="2871b-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-114">Un puntero a una cadena terminada en null que especifica el nombre del usuario que posee el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="2871b-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-116">Un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="2871b-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="2871b-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="2871b-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-118">Puntero a una cadena terminada en null que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error durante la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="2871b-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-120">Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="2871b-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-122">Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión que se debe usar para imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="2871b-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-124">Puntero a una cadena terminada en null que especifica los parámetros del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="2871b-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-126">Puntero a una cadena terminada en null que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="2871b-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-128">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de entorno y de inicialización del dispositivo para el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="2871b-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="2871b-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-130">Puntero a una cadena terminada en null que especifica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="2871b-131">Este miembro debe comprobarse antes del **Estado** y, si **pStatus** es **null**, el estado se define mediante el contenido del miembro status.</span><span class="sxs-lookup"><span data-stu-id="2871b-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2871b-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-133">El valor de este miembro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2871b-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="2871b-134">En esta versión no se admite la recuperación y configuración de descriptores de seguridad de documentos.</span><span class="sxs-lookup"><span data-stu-id="2871b-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-135">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2871b-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-136">El estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-136">The job status.</span></span> <span data-ttu-id="2871b-137">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2871b-137">This member can be one or more of the following values.</span></span>

| <span data-ttu-id="2871b-138">Value</span><span class="sxs-lookup"><span data-stu-id="2871b-138">Value</span></span>                           | <span data-ttu-id="2871b-139">Significado</span><span class="sxs-lookup"><span data-stu-id="2871b-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="2871b-140">Estado del trabajo \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="2871b-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="2871b-141">El controlador no puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="2871b-142">Estado del trabajo \_ \_ eliminado</span><span class="sxs-lookup"><span data-stu-id="2871b-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="2871b-143">El trabajo se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="2871b-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="2871b-144">\_eliminación de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="2871b-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="2871b-145">Se está eliminando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="2871b-146">\_error de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="2871b-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="2871b-147">Se ha asociado un error al trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="2871b-148">Estado del trabajo \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="2871b-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="2871b-149">La impresora está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2871b-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="2871b-150">Estado del trabajo \_ \_ PAPEROUT</span><span class="sxs-lookup"><span data-stu-id="2871b-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="2871b-151">La impresora no tiene papel.</span><span class="sxs-lookup"><span data-stu-id="2871b-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="2871b-152">Estado del trabajo en \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="2871b-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="2871b-153">El trabajo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="2871b-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="2871b-154">Estado del trabajo \_ \_ impreso</span><span class="sxs-lookup"><span data-stu-id="2871b-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="2871b-155">El trabajo se ha impreso.</span><span class="sxs-lookup"><span data-stu-id="2871b-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="2871b-156">\_impresión de estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="2871b-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="2871b-157">El trabajo está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="2871b-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="2871b-158">reinicio del estado del trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="2871b-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="2871b-159">El trabajo se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="2871b-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="2871b-160">puesta en cola del \_ Estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="2871b-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="2871b-161">El trabajo está en cola.</span><span class="sxs-lookup"><span data-stu-id="2871b-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="2871b-162">Estado del trabajo de \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="2871b-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="2871b-163">La impresora tiene un error que requiere que el usuario haga algo.</span><span class="sxs-lookup"><span data-stu-id="2871b-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="2871b-164">En Windows XP y versiones posteriores de Windows, también se pueden usar los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="2871b-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="2871b-165">Value</span><span class="sxs-lookup"><span data-stu-id="2871b-165">Value</span></span>                 | <span data-ttu-id="2871b-166">Significado</span><span class="sxs-lookup"><span data-stu-id="2871b-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2871b-167">Estado del trabajo \_ \_ completado</span><span class="sxs-lookup"><span data-stu-id="2871b-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="2871b-168">El trabajo se envía a la impresora, pero es posible que no se imprima todavía.</span><span class="sxs-lookup"><span data-stu-id="2871b-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="2871b-169">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2871b-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="2871b-170">Estado del trabajo \_ \_ retenido</span><span class="sxs-lookup"><span data-stu-id="2871b-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="2871b-171">El trabajo se ha conservado en la cola de impresión después de la impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="2871b-172">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="2871b-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-173">La prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-173">The job priority.</span></span> <span data-ttu-id="2871b-174">Este miembro puede ser uno de los valores siguientes o estar en el intervalo comprendido entre 1 y 99 ( \_ prioridad mínima a través de la \_ prioridad máxima).</span><span class="sxs-lookup"><span data-stu-id="2871b-174">This member can be one of the following values or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="2871b-175">Value</span><span class="sxs-lookup"><span data-stu-id="2871b-175">Value</span></span>         | <span data-ttu-id="2871b-176">Significado</span><span class="sxs-lookup"><span data-stu-id="2871b-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="2871b-177">\_prioridad mínima</span><span class="sxs-lookup"><span data-stu-id="2871b-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="2871b-178">Prioridad mínima.</span><span class="sxs-lookup"><span data-stu-id="2871b-178">Minimum priority.</span></span> |
| <span data-ttu-id="2871b-179">\_prioridad máxima</span><span class="sxs-lookup"><span data-stu-id="2871b-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="2871b-180">Prioridad máxima.</span><span class="sxs-lookup"><span data-stu-id="2871b-180">Maximum priority.</span></span> |
| <span data-ttu-id="2871b-181">prioridad de DEF \_</span><span class="sxs-lookup"><span data-stu-id="2871b-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="2871b-182">Prioridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2871b-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2871b-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="2871b-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-184">Posición del trabajo en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="2871b-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="2871b-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-186">La primera vez que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="2871b-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-188">La última vez que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="2871b-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-190">Número de páginas necesarias para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-190">The number of pages required for the job.</span></span> <span data-ttu-id="2871b-191">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="2871b-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-192">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="2871b-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-193">Tamaño, en bytes, del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-193">The size, in bytes, of the job.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-194">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="2871b-194">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-195">Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora A la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-195">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="2871b-196">Este valor de hora está en formato de horario universal coordinado (UTC).</span><span class="sxs-lookup"><span data-stu-id="2871b-196">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="2871b-197">Debe convertirlo en un valor de hora local antes de mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="2871b-197">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="2871b-198">Puede usar la función [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="2871b-198">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-199">**Time**</span><span class="sxs-lookup"><span data-stu-id="2871b-199">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-200">El tiempo total, en milisegundos, que ha transcurrido desde que comenzó la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="2871b-200">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="2871b-201">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="2871b-201">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="2871b-202">Número de páginas que se han imprimido.</span><span class="sxs-lookup"><span data-stu-id="2871b-202">The number of pages that have printed.</span></span> <span data-ttu-id="2871b-203">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="2871b-203">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2871b-204">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2871b-204">Remarks</span></span>

<span data-ttu-id="2871b-205">Los monitores de puerto que no son compatibles con TrueEndOfJob establecerán el trabajo como \_ estado \_ del trabajo impreso justo después de enviar el trabajo a la impresora.</span><span class="sxs-lookup"><span data-stu-id="2871b-205">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED right after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2871b-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2871b-206">Requirements</span></span>



| <span data-ttu-id="2871b-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="2871b-207">Requirement</span></span> | <span data-ttu-id="2871b-208">Value</span><span class="sxs-lookup"><span data-stu-id="2871b-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2871b-209">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2871b-209">Minimum supported client</span></span><br/> | <span data-ttu-id="2871b-210">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2871b-210">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2871b-211">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2871b-211">Minimum supported server</span></span><br/> | <span data-ttu-id="2871b-212">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2871b-212">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2871b-213">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2871b-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="2871b-214"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2871b-214"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2871b-215">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="2871b-215">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2871b-216">**\_ Información del trabajo \_ \_ 2W** (Unicode) y la **\_ información del trabajo \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2871b-216">**\_JOB\_INFO\_2W** (Unicode) and **\_JOB\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="2871b-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="2871b-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2871b-218">Impresión</span><span class="sxs-lookup"><span data-stu-id="2871b-218">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2871b-219">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="2871b-219">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2871b-220">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="2871b-220">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="2871b-221">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="2871b-221">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="2871b-222">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="2871b-222">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="2871b-223">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="2871b-223">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

