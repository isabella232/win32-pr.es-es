---
description: Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola de impresión grandes con tamaños expresados con 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: Estructura de JOB_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5a6ccd7bf589ed341c9aceab86205cd9852c0896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649253"
---
# <a name="job_info_4-structure"></a><span data-ttu-id="78be9-103">Estructura de información de trabajo \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="78be9-103">JOB\_INFO\_4 structure</span></span>

<span data-ttu-id="78be9-104">Describe un conjunto completo de valores asociados a un trabajo y admite archivos de cola de impresión grandes con tamaños expresados con 64 bits.</span><span class="sxs-lookup"><span data-stu-id="78be9-104">Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.</span></span>

## <a name="syntax"></a><span data-ttu-id="78be9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78be9-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_4 {
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
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a><span data-ttu-id="78be9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="78be9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78be9-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="78be9-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-108">Un valor de identificador de trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-108">A job identifier value.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="78be9-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-110">Puntero a una cadena terminada en null que especifica el nombre de la impresora para la que se pone en cola el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-110">A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-111">**pMachineName**</span><span class="sxs-lookup"><span data-stu-id="78be9-111">**pMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-112">Puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-112">A pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-113">**pUserName**</span><span class="sxs-lookup"><span data-stu-id="78be9-113">**pUserName**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-114">Un puntero a una cadena terminada en null que especifica el nombre del usuario que posee el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-114">A pointer to a null-terminated string that specifies the name of the user who owns the print job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-115">**pDocument**</span><span class="sxs-lookup"><span data-stu-id="78be9-115">**pDocument**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-116">Un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="78be9-116">A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>

</dd> <dt>

<span data-ttu-id="78be9-117">**pNotifyName**</span><span class="sxs-lookup"><span data-stu-id="78be9-117">**pNotifyName**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-118">Puntero a una cadena terminada en null que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error durante la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-118">A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-119">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="78be9-119">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-120">Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-120">A pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-121">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="78be9-121">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-122">Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión que se debe usar para imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-122">A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-123">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="78be9-123">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-124">Puntero a una cadena terminada en null que especifica los parámetros del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-124">A pointer to a null-terminated string that specifies print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-125">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="78be9-125">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-126">Puntero a una cadena terminada en null que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-126">A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-127">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="78be9-127">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-128">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de entorno y de inicialización del dispositivo para el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="78be9-128">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-129">**pStatus**</span><span class="sxs-lookup"><span data-stu-id="78be9-129">**pStatus**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-130">Puntero a una cadena terminada en null que especifica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-130">A pointer to a null-terminated string that specifies the status of the print job.</span></span> <span data-ttu-id="78be9-131">Este miembro debe comprobarse antes del **Estado** y, si **pStatus** es **null**, el estado se define mediante el contenido del miembro status.</span><span class="sxs-lookup"><span data-stu-id="78be9-131">This member should be checked prior to **Status** and, if **pStatus** is **NULL**, the status is defined by the contents of the Status member.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-132">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="78be9-132">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-133">El valor de este miembro es **null**.</span><span class="sxs-lookup"><span data-stu-id="78be9-133">The value of this member is **NULL**.</span></span> <span data-ttu-id="78be9-134">En esta versión no se admite la recuperación y configuración de descriptores de seguridad de documentos.</span><span class="sxs-lookup"><span data-stu-id="78be9-134">Retrieval and setting of document security descriptors is not supported in this release.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-135">**Estado**</span><span class="sxs-lookup"><span data-stu-id="78be9-135">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-136">El estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-136">The job status.</span></span> <span data-ttu-id="78be9-137">Este miembro puede ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="78be9-137">This member can be one or more of the following values:</span></span>

| <span data-ttu-id="78be9-138">Value</span><span class="sxs-lookup"><span data-stu-id="78be9-138">Value</span></span>                           | <span data-ttu-id="78be9-139">Significado</span><span class="sxs-lookup"><span data-stu-id="78be9-139">Meaning</span></span>                                                      |
|---------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="78be9-140">Estado del trabajo \_ \_ bloqueado \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="78be9-140">JOB\_STATUS\_BLOCKED\_DEVQ</span></span>      | <span data-ttu-id="78be9-141">El controlador no puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-141">The driver cannot print the job.</span></span>                             |
| <span data-ttu-id="78be9-142">Estado del trabajo \_ \_ eliminado</span><span class="sxs-lookup"><span data-stu-id="78be9-142">JOB\_STATUS\_DELETED</span></span>            | <span data-ttu-id="78be9-143">El trabajo se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="78be9-143">Job has been deleted.</span></span>                                        |
| <span data-ttu-id="78be9-144">\_eliminación de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="78be9-144">JOB\_STATUS\_DELETING</span></span>           | <span data-ttu-id="78be9-145">Se está eliminando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-145">Job is being deleted.</span></span>                                        |
| <span data-ttu-id="78be9-146">\_error de estado de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="78be9-146">JOB\_STATUS\_ERROR</span></span>              | <span data-ttu-id="78be9-147">Se ha asociado un error al trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-147">An error is associated with the job.</span></span>                         |
| <span data-ttu-id="78be9-148">Estado del trabajo \_ \_ sin conexión</span><span class="sxs-lookup"><span data-stu-id="78be9-148">JOB\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="78be9-149">La impresora está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="78be9-149">Printer is offline.</span></span>                                          |
| <span data-ttu-id="78be9-150">Estado del trabajo \_ \_ PAPEROUT</span><span class="sxs-lookup"><span data-stu-id="78be9-150">JOB\_STATUS\_PAPEROUT</span></span>           | <span data-ttu-id="78be9-151">La impresora no tiene papel.</span><span class="sxs-lookup"><span data-stu-id="78be9-151">Printer is out of paper.</span></span>                                     |
| <span data-ttu-id="78be9-152">Estado del trabajo en \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="78be9-152">JOB\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="78be9-153">El trabajo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="78be9-153">Job is paused.</span></span>                                               |
| <span data-ttu-id="78be9-154">Estado del trabajo \_ \_ impreso</span><span class="sxs-lookup"><span data-stu-id="78be9-154">JOB\_STATUS\_PRINTED</span></span>            | <span data-ttu-id="78be9-155">El trabajo se ha impreso.</span><span class="sxs-lookup"><span data-stu-id="78be9-155">Job has printed.</span></span>                                             |
| <span data-ttu-id="78be9-156">\_impresión de estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="78be9-156">JOB\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="78be9-157">El trabajo está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="78be9-157">Job is printing.</span></span>                                             |
| <span data-ttu-id="78be9-158">reinicio del estado del trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="78be9-158">JOB\_STATUS\_RESTART</span></span>            | <span data-ttu-id="78be9-159">El trabajo se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="78be9-159">Job has been restarted.</span></span>                                      |
| <span data-ttu-id="78be9-160">puesta en cola del \_ Estado del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="78be9-160">JOB\_STATUS\_SPOOLING</span></span>           | <span data-ttu-id="78be9-161">El trabajo está en cola.</span><span class="sxs-lookup"><span data-stu-id="78be9-161">Job is spooling.</span></span>                                             |
| <span data-ttu-id="78be9-162">Estado del trabajo de \_ \_ intervención del usuario \_</span><span class="sxs-lookup"><span data-stu-id="78be9-162">JOB\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="78be9-163">La impresora tiene un error que requiere que el usuario haga algo.</span><span class="sxs-lookup"><span data-stu-id="78be9-163">Printer has an error that requires the user to do something.</span></span> |



 

<span data-ttu-id="78be9-164">En Windows XP y versiones posteriores de Windows, también se pueden usar los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="78be9-164">In Windows XP and later versions of Windows, the following values can also be used:</span></span>

| <span data-ttu-id="78be9-165">Value</span><span class="sxs-lookup"><span data-stu-id="78be9-165">Value</span></span>                 | <span data-ttu-id="78be9-166">Significado</span><span class="sxs-lookup"><span data-stu-id="78be9-166">Meaning</span></span>                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78be9-167">Estado del trabajo \_ \_ completado</span><span class="sxs-lookup"><span data-stu-id="78be9-167">JOB\_STATUS\_COMPLETE</span></span> | <span data-ttu-id="78be9-168">El trabajo se envía a la impresora, pero es posible que no se imprima todavía.</span><span class="sxs-lookup"><span data-stu-id="78be9-168">The job is sent to the printer, but may not be printed yet.</span></span> <span data-ttu-id="78be9-169">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="78be9-169">See Remarks for more information.</span></span> |
| <span data-ttu-id="78be9-170">Estado del trabajo \_ \_ retenido</span><span class="sxs-lookup"><span data-stu-id="78be9-170">JOB\_STATUS\_RETAINED</span></span> | <span data-ttu-id="78be9-171">El trabajo se ha conservado en la cola de impresión después de la impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-171">The job has been retained in the print queue following printing.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="78be9-172">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="78be9-172">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-173">La prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-173">The job priority.</span></span> <span data-ttu-id="78be9-174">Este miembro puede ser uno de los valores siguientes o en el intervalo comprendido entre 1 y 99 ( \_ prioridad mínima a través de la \_ prioridad máxima).</span><span class="sxs-lookup"><span data-stu-id="78be9-174">This member can be one of the following values, or in the range between 1 through 99 (MIN\_PRIORITY through MAX\_PRIORITY).</span></span>



| <span data-ttu-id="78be9-175">Value</span><span class="sxs-lookup"><span data-stu-id="78be9-175">Value</span></span>         | <span data-ttu-id="78be9-176">Significado</span><span class="sxs-lookup"><span data-stu-id="78be9-176">Meaning</span></span>           |
|---------------|-------------------|
| <span data-ttu-id="78be9-177">\_prioridad mínima</span><span class="sxs-lookup"><span data-stu-id="78be9-177">MIN\_PRIORITY</span></span> | <span data-ttu-id="78be9-178">Prioridad mínima.</span><span class="sxs-lookup"><span data-stu-id="78be9-178">Minimum priority.</span></span> |
| <span data-ttu-id="78be9-179">\_prioridad máxima</span><span class="sxs-lookup"><span data-stu-id="78be9-179">MAX\_PRIORITY</span></span> | <span data-ttu-id="78be9-180">Prioridad máxima.</span><span class="sxs-lookup"><span data-stu-id="78be9-180">Maximum priority.</span></span> |
| <span data-ttu-id="78be9-181">prioridad de DEF \_</span><span class="sxs-lookup"><span data-stu-id="78be9-181">DEF\_PRIORITY</span></span> | <span data-ttu-id="78be9-182">Prioridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="78be9-182">Default priority.</span></span> |



 

</dd> <dt>

<span data-ttu-id="78be9-183">**Position**</span><span class="sxs-lookup"><span data-stu-id="78be9-183">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-184">Posición del trabajo en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="78be9-184">The job's position in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="78be9-185">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-186">La primera vez que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-186">The earliest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-187">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="78be9-187">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-188">La última vez que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-188">The latest time that the job can be printed.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-189">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="78be9-189">**TotalPages**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-190">Número de páginas necesarias para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-190">The number of pages required for the job.</span></span> <span data-ttu-id="78be9-191">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="78be9-191">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-192">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="78be9-192">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-193">Los cuatro bytes inferiores del tamaño, en bytes, del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-193">The lower four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="78be9-194">Vea también el miembro **SizeHigh** a continuación.</span><span class="sxs-lookup"><span data-stu-id="78be9-194">See also the **SizeHigh** member below.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-195">**Enviado**</span><span class="sxs-lookup"><span data-stu-id="78be9-195">**Submitted**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-196">Estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora A la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-196">A [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>

<span data-ttu-id="78be9-197">Este valor de hora está en formato de horario universal coordinado (UTC).</span><span class="sxs-lookup"><span data-stu-id="78be9-197">This time value is in Universal Time Coordinate (UTC) format.</span></span> <span data-ttu-id="78be9-198">Debe convertirlo en un valor de hora local antes de mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="78be9-198">You should convert it to a local time value before displaying it.</span></span> <span data-ttu-id="78be9-199">Puede usar la función [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="78be9-199">You can use the [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) function to perform the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-200">**Time**</span><span class="sxs-lookup"><span data-stu-id="78be9-200">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-201">El tiempo total, en milisegundos, que ha transcurrido desde que comenzó la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-201">The total time, in milliseconds, that has elapsed since the job began printing.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-202">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="78be9-202">**PagesPrinted**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-203">Número de páginas que se han imprimido.</span><span class="sxs-lookup"><span data-stu-id="78be9-203">The number of pages that have printed.</span></span> <span data-ttu-id="78be9-204">Este valor puede ser cero si el trabajo de impresión no contiene información de delimitación de página.</span><span class="sxs-lookup"><span data-stu-id="78be9-204">This value may be zero if the print job does not contain page delimiting information.</span></span>

</dd> <dt>

<span data-ttu-id="78be9-205">**SizeHigh**</span><span class="sxs-lookup"><span data-stu-id="78be9-205">**SizeHigh**</span></span>
</dt> <dd>

<span data-ttu-id="78be9-206">Los cuatro bytes superiores del tamaño, en bytes, del trabajo.</span><span class="sxs-lookup"><span data-stu-id="78be9-206">The higher four bytes of the size, in bytes, of the job.</span></span> <span data-ttu-id="78be9-207">Vea también el miembro de **tamaño** anterior.</span><span class="sxs-lookup"><span data-stu-id="78be9-207">See also the **Size** member above.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78be9-208">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78be9-208">Remarks</span></span>

<span data-ttu-id="78be9-209">Los monitores de puerto que no admiten TrueEndOfJob establecerán el trabajo como estado del trabajo \_ \_ impreso inmediatamente después de enviar el trabajo a la impresora.</span><span class="sxs-lookup"><span data-stu-id="78be9-209">Port monitors that do not support TrueEndOfJob will set the job as JOB\_STATUS\_PRINTED immediately after the job is submitted to the printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="78be9-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78be9-210">Requirements</span></span>



| <span data-ttu-id="78be9-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="78be9-211">Requirement</span></span> | <span data-ttu-id="78be9-212">Value</span><span class="sxs-lookup"><span data-stu-id="78be9-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78be9-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78be9-213">Minimum supported client</span></span><br/> | <span data-ttu-id="78be9-214">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78be9-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="78be9-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78be9-215">Minimum supported server</span></span><br/> | <span data-ttu-id="78be9-216">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78be9-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78be9-217">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78be9-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="78be9-218"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="78be9-218"><dt>Winspool.h</dt></span></span> </dl> |
| <span data-ttu-id="78be9-219">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="78be9-219">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="78be9-220">**\_ Información del trabajo \_ \_ 4W** (Unicode) y la **\_ información del trabajo \_ \_ 4A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="78be9-220">**\_JOB\_INFO\_4W** (Unicode) and **\_JOB\_INFO\_4A** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="78be9-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="78be9-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78be9-222">Impresión</span><span class="sxs-lookup"><span data-stu-id="78be9-222">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="78be9-223">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="78be9-223">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="78be9-224">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="78be9-224">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="78be9-225">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="78be9-225">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="78be9-226">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="78be9-226">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="78be9-227">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="78be9-227">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

