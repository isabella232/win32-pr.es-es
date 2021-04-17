---
description: La función SetJob pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada. También puede usar la función SetJob para establecer los parámetros del trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Función SetJob (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687966"
---
# <a name="setjob-function"></a><span data-ttu-id="c6dec-104">SetJob función)</span><span class="sxs-lookup"><span data-stu-id="c6dec-104">SetJob function</span></span>

<span data-ttu-id="c6dec-105">La función **SetJob** pausa, reanuda, cancela o reinicia un trabajo de impresión en una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="c6dec-105">The **SetJob** function pauses, resumes, cancels, or restarts a print job on a specified printer.</span></span> <span data-ttu-id="c6dec-106">También puede usar la función **SetJob** para establecer los parámetros del trabajo de impresión, como la prioridad del trabajo de impresión y el nombre del documento.</span><span class="sxs-lookup"><span data-stu-id="c6dec-106">You can also use the **SetJob** function to set print job parameters, such as the print job priority and the document name.</span></span>

<span data-ttu-id="c6dec-107">Puede usar la función **SetJob** para proporcionar un comando a un trabajo de impresión o para establecer los parámetros de un trabajo de impresión, o para realizar ambas acciones en la misma llamada.</span><span class="sxs-lookup"><span data-stu-id="c6dec-107">You can use the **SetJob** function to give a command to a print job, or to set print job parameters, or to do both in the same call.</span></span> <span data-ttu-id="c6dec-108">El valor del parámetro *Command* no afecta al modo en que la función utiliza los parámetros *LEVEL* y *pJob* .</span><span class="sxs-lookup"><span data-stu-id="c6dec-108">The value of the *Command* parameter does not affect how the function uses the *Level* and *pJob* parameters.</span></span> <span data-ttu-id="c6dec-109">Además, puede usar **SetJob** con la [**información de trabajo \_ \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-109">Also, you can use **SetJob** with [**JOB\_INFO\_3**](job-info-3.md) to link together a set of print jobs.</span></span> <span data-ttu-id="c6dec-110">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c6dec-110">See Remarks for more information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dec-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6dec-111">Syntax</span></span>


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="c6dec-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6dec-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6dec-113">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6dec-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dec-114">Identificador del objeto de impresora de interés.</span><span class="sxs-lookup"><span data-stu-id="c6dec-114">A handle to the printer object of interest.</span></span> <span data-ttu-id="c6dec-115">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c6dec-115">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c6dec-116">*JobID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6dec-116">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dec-117">Identificador que especifica el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-117">Identifier that specifies the print job.</span></span> <span data-ttu-id="c6dec-118">Para obtener un identificador de trabajo de impresión, llame a la función [**AddJob**](addjob.md) o a la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .</span><span class="sxs-lookup"><span data-stu-id="c6dec-118">You obtain a print job identifier by calling the [**AddJob**](addjob.md) function or the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span>

<span data-ttu-id="c6dec-119">Si el parámetro *LEVEL* está establecido en 3, el parámetro *JobID* debe coincidir con el miembro **JobID** de la estructura [**Job \_ info \_ 3**](job-info-3.md) indicada por *pJob*</span><span class="sxs-lookup"><span data-stu-id="c6dec-119">If the *Level* parameter is set to 3, the *JobId* parameter must match the **JobId** member of the [**JOB\_INFO\_3**](job-info-3.md) structure pointed to by *pJob*</span></span>

</dd> <dt>

<span data-ttu-id="c6dec-120">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c6dec-120">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dec-121">El tipo de estructura de información de trabajo al que apunta el parámetro *pJob* .</span><span class="sxs-lookup"><span data-stu-id="c6dec-121">The type of job information structure pointed to by the *pJob* parameter.</span></span>

<span data-ttu-id="c6dec-122">**Todas las versiones de Windows**: puede establecer el parámetro *LEVEL* en 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c6dec-122">**All versions of Windows**: You can set the *Level* parameter to 0, 1, or 2.</span></span> <span data-ttu-id="c6dec-123">Al establecer *LEVEL* en 0, *PJob* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-123">When you set *Level* to 0, *pJob* should be **NULL**.</span></span> <span data-ttu-id="c6dec-124">Utilice estos valores cuando no esté configurando ningún parámetro de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-124">Use these values when you are not setting any print job parameters.</span></span>

<span data-ttu-id="c6dec-125">También puede establecer el parámetro *LEVEL* en 3.</span><span class="sxs-lookup"><span data-stu-id="c6dec-125">You can also set the *Level* parameter to 3.</span></span>

<span data-ttu-id="c6dec-126">A partir de **Windows Vista**: también puede establecer el parámetro *LEVEL* en 4.</span><span class="sxs-lookup"><span data-stu-id="c6dec-126">Starting with **Windows Vista**: You can also set the *Level* parameter to 4.</span></span>

</dd> <dt>

<span data-ttu-id="c6dec-127">*pJob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6dec-127">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dec-128">Puntero a una estructura que establece los parámetros del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-128">A pointer to a structure that sets the print job parameters.</span></span>

<span data-ttu-id="c6dec-129">**Todas las versiones de Windows**: *pJob* pueden apuntar a una estructura Job [**\_ info \_ 1**](job-info-1.md) o [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c6dec-129">**All versions of Windows**: *pJob* can point to a [**JOB\_INFO\_1**](job-info-1.md) or [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

<span data-ttu-id="c6dec-130">*pJob* también puede apuntar a una estructura [**Job \_ info \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="c6dec-130">*pJob* can also point to a [**JOB\_INFO\_3**](job-info-3.md) structure.</span></span> <span data-ttu-id="c6dec-131">Debe tener **acceso de \_ trabajo \_ administrar** el permiso de acceso para los trabajos especificados por los miembros **JobID** y **NextJobId** de la estructura **Job \_ info \_ 3** .</span><span class="sxs-lookup"><span data-stu-id="c6dec-131">You must have **JOB\_ACCESS\_ADMINISTER** access permission for the jobs specified by the **JobId** and **NextJobId** members of the **JOB\_INFO\_3** structure.</span></span>

<span data-ttu-id="c6dec-132">A partir de **Windows Vista**: *pJob* también puede apuntar a una estructura [**Job \_ info \_ 4**](job-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="c6dec-132">Starting with **Windows Vista**: *pJob* can also point to a [**JOB\_INFO\_4**](job-info-4.md) structure.</span></span>

<span data-ttu-id="c6dec-133">Si el parámetro *LEVEL* es 0, *PJob* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-133">If the *Level* parameter is 0, *pJob* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c6dec-134">*Comando* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6dec-134">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dec-135">Operación de trabajo de impresión que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="c6dec-135">The print job operation to perform.</span></span> <span data-ttu-id="c6dec-136">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6dec-136">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c6dec-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c6dec-137">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="c6dec-138">Significado</span><span class="sxs-lookup"><span data-stu-id="c6dec-138">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <span data-ttu-id="c6dec-139"><dt>**\_cancelación de control de trabajo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-139"><dt>**JOB\_CONTROL\_CANCEL**</dt></span></span> </dl>                                    | <span data-ttu-id="c6dec-140">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="c6dec-140">Do not use.</span></span> <span data-ttu-id="c6dec-141">Para eliminar un trabajo de impresión, use el **control de trabajo \_ \_ eliminar**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-141">To delete a print job, use **JOB\_CONTROL\_DELETE**.</span></span><br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <span data-ttu-id="c6dec-142"><dt>**pausar control de trabajo \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-142"><dt>**JOB\_CONTROL\_PAUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="c6dec-143">Pausar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-143">Pause the print job.</span></span><br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <span data-ttu-id="c6dec-144"><dt>**reinicio del control de trabajo \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-144"><dt>**JOB\_CONTROL\_RESTART**</dt></span></span> </dl>                                 | <span data-ttu-id="c6dec-145">Reinicie el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-145">Restart the print job.</span></span> <span data-ttu-id="c6dec-146">Un trabajo solo se puede reiniciar si se imprimió.</span><span class="sxs-lookup"><span data-stu-id="c6dec-146">A job can only be restarted if it was printing.</span></span><br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <span data-ttu-id="c6dec-147"><dt>**\_reanudación de control de trabajo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-147"><dt>**JOB\_CONTROL\_RESUME**</dt></span></span> </dl>                                    | <span data-ttu-id="c6dec-148">Reanudar un trabajo de impresión en pausa.</span><span class="sxs-lookup"><span data-stu-id="c6dec-148">Resume a paused print job.</span></span><br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <span data-ttu-id="c6dec-149"><dt>**\_eliminación de control de trabajo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-149"><dt>**JOB\_CONTROL\_DELETE**</dt></span></span> </dl>                                    | <span data-ttu-id="c6dec-150">Elimine el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-150">Delete the print job.</span></span><br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <span data-ttu-id="c6dec-151"><dt>**\_control \_ de trabajo enviado a la \_ \_ impresora**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-151"><dt>**JOB\_CONTROL\_SENT\_TO\_PRINTER**</dt></span></span> </dl>       | <span data-ttu-id="c6dec-152">Lo usan los monitores de puerto para finalizar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-152">Used by port monitors to end the print job.</span></span><br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <span data-ttu-id="c6dec-153"><dt>**\_última página de control de trabajo \_ \_ \_ expulsada**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-153"><dt>**JOB\_CONTROL\_LAST\_PAGE\_EJECTED**</dt></span></span> </dl> | <span data-ttu-id="c6dec-154">Lo usan los monitores de idioma para finalizar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-154">Used by language monitors to end the print job.</span></span><br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <span data-ttu-id="c6dec-155"><dt>**\_conservar control de trabajo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-155"><dt>**JOB\_CONTROL\_RETAIN**</dt></span></span> </dl>                                    | <span data-ttu-id="c6dec-156">**Windows Vista y versiones posteriores**: Mantenga el trabajo en la cola después de imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="c6dec-156">**Windows Vista and later**: Keep the job in the queue after it prints.</span></span><br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <span data-ttu-id="c6dec-157"><dt>**\_versión de control de trabajo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-157"><dt>**JOB\_CONTROL\_RELEASE**</dt></span></span> </dl>                                 | <span data-ttu-id="c6dec-158">**Windows Vista y versiones posteriores**: libere el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-158">**Windows Vista and later**: Release the print job.</span></span><br/>                     |



 

<span data-ttu-id="c6dec-159">Puede usar la misma llamada a la función **SetJob** para establecer los parámetros del trabajo de impresión y proporcionar un comando a un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-159">You can use the same call to the **SetJob** function to set print job parameters and to give a command to a print job.</span></span> <span data-ttu-id="c6dec-160">Por lo tanto, el *comando* no tiene que ser 0 si está estableciendo parámetros de trabajo de impresión, aunque puede ser.</span><span class="sxs-lookup"><span data-stu-id="c6dec-160">Thus, *Command* does not need to be 0 if you are setting print job parameters, although it can be.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6dec-161">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6dec-161">Return value</span></span>

<span data-ttu-id="c6dec-162">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c6dec-162">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c6dec-163">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c6dec-163">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dec-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6dec-164">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6dec-165">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c6dec-165">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c6dec-166">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c6dec-166">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c6dec-167">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="c6dec-167">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c6dec-168">Puede usar la función **SetJob** para establecer varios parámetros de trabajo de impresión proporcionando un puntero a una estructura de información de trabajo [**\_ \_ 1**](job-info-1.md), [**información de trabajo \_ \_ 2**](job-info-2.md), [**información de trabajo \_ \_ 3**](job-info-3.md)o [**información de trabajo \_ \_ 4**](job-info-4.md) que contenga los datos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c6dec-168">You can use the **SetJob** function to set various print job parameters by supplying a pointer to a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), [**JOB\_INFO\_3**](job-info-3.md), or [**JOB\_INFO\_4**](job-info-4.md) structure that contains the necessary data.</span></span>

<span data-ttu-id="c6dec-169">Para quitar o eliminar todos los trabajos de impresión de una impresora determinada, llame a la función [**SetPrinter**](setprinter.md) con su parámetro de *comando* establecido en **purga de \_ control \_ de impresora**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-169">To remove or delete all of the print jobs for a particular printer, call the [**SetPrinter**](setprinter.md) function with its *Command* parameter set to **PRINTER\_CONTROL\_PURGE**.</span></span>

<span data-ttu-id="c6dec-170">Los siguientes miembros de una estructura Job info [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) se omiten en una llamada a **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **size**, **almeterd**, **Time** y **TotalPages**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-170">The following members of a [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure are ignored on a call to **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted**, **Time**, and **TotalPages**.</span></span>

<span data-ttu-id="c6dec-171">Para cambiar la posición de un trabajo de impresión en la cola de impresión, debe disponer del permiso de acceso de **\_ \_ Administración** de acceso de impresora para una impresora.</span><span class="sxs-lookup"><span data-stu-id="c6dec-171">You must have **PRINTER\_ACCESS\_ADMINISTER** access permission for a printer in order to change a print job's position in the print queue.</span></span>

<span data-ttu-id="c6dec-172">Si no desea establecer la posición de un trabajo de impresión en la cola de impresión, debe establecer el miembro **Position** de la estructura Job info [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) en la posición del **trabajo \_ \_ sin especificar**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-172">If you do not want to set a print job's position in the print queue, you should set the **Position** member of the [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_4**](job-info-4.md) structure to **JOB\_POSITION\_UNSPECIFIED**.</span></span>

<span data-ttu-id="c6dec-173">Use la función **SetJob** con la estructura [**Job \_ info \_ 3**](job-info-3.md) para vincular un conjunto de trabajos de impresión (también conocido como cadena).</span><span class="sxs-lookup"><span data-stu-id="c6dec-173">Use the **SetJob** function with the [**JOB\_INFO\_3**](job-info-3.md) structure to link together a set of print jobs (also known as a chain).</span></span> <span data-ttu-id="c6dec-174">Esto resulta útil en situaciones en las que un único documento consta de varias partes que se desean representar por separado.</span><span class="sxs-lookup"><span data-stu-id="c6dec-174">This is useful in situations where a single document consists of several parts that you want to render separately.</span></span> <span data-ttu-id="c6dec-175">Para imprimir los trabajos a, B, C y D en orden, llame a **SetJob** con la [**información de trabajo \_ \_ 4**](job-info-4.md) para vincular a b, b a c y c a D.</span><span class="sxs-lookup"><span data-stu-id="c6dec-175">To print jobs A, B, C, and D in order, call **SetJob** with [**JOB\_INFO\_4**](job-info-4.md) to link A to B, B to C, and C to D.</span></span>

<span data-ttu-id="c6dec-176">Si vincula los trabajos de impresión, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6dec-176">If you link print jobs, note the following:</span></span>

-   <span data-ttu-id="c6dec-177">Los trabajos se pueden agregar al principio o al final de una cadena.</span><span class="sxs-lookup"><span data-stu-id="c6dec-177">Jobs can be added to the beginning or end of a chain.</span></span>
-   <span data-ttu-id="c6dec-178">Todos los trabajos de la cadena deben tener el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-178">All jobs in the chain must have the same data type.</span></span>
-   <span data-ttu-id="c6dec-179">La cadena debe estar completamente vinculada antes de que comience la cola de impresión; de lo contrario, el administrador de trabajos de impresión puede imprimir y eliminar los trabajos en cola antes de vincularlos todos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-179">The chain must be completely linked before spooling begins, otherwise the spooler may print and delete spooled jobs before you link them all.</span></span> <span data-ttu-id="c6dec-180">Hay dos maneras de evitar que la cadena se imprima prematuramente:</span><span class="sxs-lookup"><span data-stu-id="c6dec-180">There are two ways to keep the chain from printing prematurely:</span></span>

    -   <span data-ttu-id="c6dec-181">PAUSE el primer trabajo de la cadena hasta que la cadena esté completamente vinculada.</span><span class="sxs-lookup"><span data-stu-id="c6dec-181">Pause the first job in the chain until the chain is completely linked.</span></span> <span data-ttu-id="c6dec-182">El estado en pausa del primer trabajo rige el estado de todos los trabajos de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c6dec-182">The paused state of the first job governs the state of all jobs in the chain.</span></span>
    -   <span data-ttu-id="c6dec-183">Mantener el primer trabajo incompleto, es decir, no llamar a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) para el primer trabajo.</span><span class="sxs-lookup"><span data-stu-id="c6dec-183">Keep the first job incomplete, that is, do not call [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) or [**ScheduleJob**](schedulejob.md) for the first job.</span></span> <span data-ttu-id="c6dec-184">Sin embargo, si está habilitada la opción ' imprimir mientras se pone en cola ' (valor predeterminado), este método bloquea el puerto mientras se compila la cadena, lo que también impide la impresión de trabajos no relacionados.</span><span class="sxs-lookup"><span data-stu-id="c6dec-184">However, if 'print while spooling' is enabled (the default), this method blocks the port while the chain is built, which also prevents the printing of non-related jobs.</span></span>

-   <span data-ttu-id="c6dec-185">La aplicación debe controlar el caso en el que el usuario elimina un trabajo en la cadena antes de que la cadena finalice la impresión.</span><span class="sxs-lookup"><span data-stu-id="c6dec-185">The application must handle the case where the user deletes a job in the chain before the chain finishes printing.</span></span> <span data-ttu-id="c6dec-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **un \_ parámetro no válido** cuando no existe un JobID.</span><span class="sxs-lookup"><span data-stu-id="c6dec-186">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **INVALID\_PARAMETER** when a JobID does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dec-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6dec-187">Requirements</span></span>



| <span data-ttu-id="c6dec-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6dec-188">Requirement</span></span> | <span data-ttu-id="c6dec-189">Value</span><span class="sxs-lookup"><span data-stu-id="c6dec-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dec-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6dec-190">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dec-191">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6dec-191">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c6dec-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6dec-192">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dec-193">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6dec-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c6dec-194">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6dec-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6dec-195"><dt>WinSpool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-195"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c6dec-196">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6dec-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6dec-197"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-197"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c6dec-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6dec-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6dec-199"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c6dec-199"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c6dec-200">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c6dec-200">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c6dec-201">**SetJobW** (Unicode) y **SetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c6dec-201">**SetJobW** (Unicode) and **SetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="c6dec-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6dec-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dec-203">Impresión</span><span class="sxs-lookup"><span data-stu-id="c6dec-203">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c6dec-204">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="c6dec-204">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c6dec-205">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="c6dec-205">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="c6dec-206">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="c6dec-206">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="c6dec-207">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c6dec-207">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c6dec-208">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c6dec-208">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="c6dec-209">**Información de trabajo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c6dec-209">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="c6dec-210">**Información de trabajo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c6dec-210">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="c6dec-211">**Información de trabajo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c6dec-211">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="c6dec-212">**Información del trabajo \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c6dec-212">**JOB\_INFO\_4**</span></span>](job-info-4.md)
</dt> </dl>

 

