---
description: La función AddJob agrega un trabajo de impresión a la lista de trabajos de impresión que puede programar el administrador de trabajos de impresión. La función recupera el nombre del archivo que puede usar para almacenar el trabajo.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Función AddJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813571"
---
# <a name="addjob-function"></a><span data-ttu-id="86e23-104">AddJob función)</span><span class="sxs-lookup"><span data-stu-id="86e23-104">AddJob function</span></span>

<span data-ttu-id="86e23-105">La función **AddJob** agrega un trabajo de impresión a la lista de trabajos de impresión que puede programar el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="86e23-105">The **AddJob** function adds a print job to the list of print jobs that can be scheduled by the print spooler.</span></span> <span data-ttu-id="86e23-106">La función recupera el nombre del archivo que puede usar para almacenar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="86e23-106">The function retrieves the name of the file you can use to store the job.</span></span>

> [!NOTE]
> <span data-ttu-id="86e23-107">En los sistemas operativos Windows 8 y versiones posteriores, no se recomienda usar **AddJob** directamente porque hay casos (como imprimir en una cola mediante File: o PORTPROMPT:) donde **AddJob** producirá un error.</span><span class="sxs-lookup"><span data-stu-id="86e23-107">In Windows 8 and later operating systems, we do not recommended using **AddJob** directly because there are cases (such as printing to a queue using File: or PORTPROMPT:) where **AddJob** will fail.</span></span> <span data-ttu-id="86e23-108">En su lugar, se recomienda usar la [API de impresión de GDI](gdi-printing.md), la [API de impresión XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)o el método adecuado del espacio de nombres [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , dependiendo del escenario de impresión.</span><span class="sxs-lookup"><span data-stu-id="86e23-108">Instead, you are advised to use [GDI Print API](gdi-printing.md), [XPS Print API](xps-printing.md), [**StartDocPrinter**](startdocprinter.md), or the appropriate method from the [**Windows.Graphics.Printing**](/uwp/api/Windows.Graphics.Printing) namespace, depending on the print scenario.</span></span>
>
> <span data-ttu-id="86e23-109">Si intenta imprimir en una cola mediante **File:** o **PORTPROMPT:**, **AddJob** devolverá el error no \_ admitido.</span><span class="sxs-lookup"><span data-stu-id="86e23-109">If you try to print to a queue using **File:** or **PORTPROMPT:**, **AddJob** will Return the NOT\_SUPPORTED error.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e23-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86e23-110">Syntax</span></span>

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a><span data-ttu-id="86e23-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86e23-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e23-112">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86e23-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e23-113">Identificador que especifica la impresora para el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="86e23-113">A handle that specifies the printer for the print job.</span></span> <span data-ttu-id="86e23-114">Debe ser una impresora local configurada como una impresora en cola.</span><span class="sxs-lookup"><span data-stu-id="86e23-114">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="86e23-115">Si *hPrinter* es un identificador de una conexión de impresora remota, o si la impresora está configurada para impresión directa, se produce un error en la función **AddJob** .</span><span class="sxs-lookup"><span data-stu-id="86e23-115">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **AddJob** function fails.</span></span> <span data-ttu-id="86e23-116">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="86e23-116">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="86e23-117">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="86e23-117">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e23-118">La versión de la estructura de datos de la información del trabajo de impresión que la función almacena en el búfer al que apunta *pdata*.</span><span class="sxs-lookup"><span data-stu-id="86e23-118">The version of the print job information data structure that the function stores into the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86e23-119">Establezca este parámetro en uno.</span><span class="sxs-lookup"><span data-stu-id="86e23-119">Set this parameter to one.</span></span>

</dd> <dt>

<span data-ttu-id="86e23-120">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86e23-120">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e23-121">Un puntero a un búfer que recibe una estructura de datos de [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y una cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="86e23-121">A pointer to a buffer that receives an [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="86e23-122">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86e23-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e23-123">Tamaño, en bytes, del búfer al que apunta *pdata*.</span><span class="sxs-lookup"><span data-stu-id="86e23-123">The size, in bytes, of the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86e23-124">El búfer debe ser lo suficientemente grande como para contener una estructura de [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y una cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="86e23-124">The buffer needs to be large enough to contain an [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure and a path string.</span></span>

</dd> <dt>

<span data-ttu-id="86e23-125">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86e23-125">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86e23-126">Puntero a una variable que recibe el tamaño total, en bytes, de la estructura de datos [**ADDJOB \_ info \_ 1**](addjob-info-1.md) más la cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="86e23-126">A pointer to a variable that receives the total size, in bytes, of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) data structure plus the path string.</span></span> <span data-ttu-id="86e23-127">Si este valor es menor o igual que *cbBuf* y la función se ejecuta correctamente, se trata del número real de bytes escritos en el búfer señalado por *pdata*.</span><span class="sxs-lookup"><span data-stu-id="86e23-127">If this value is less than or equal to *cbBuf* and the function succeeds, this is the actual number of bytes written to the buffer pointed to by *pData*.</span></span> <span data-ttu-id="86e23-128">Si este número es mayor que *cbBuf*, el búfer es demasiado pequeño y debe volver a llamar a la función con un tamaño de búfer de al menos tan grande como \* *pcbNeeded*.</span><span class="sxs-lookup"><span data-stu-id="86e23-128">If this number is greater than *cbBuf*, the buffer is too small, and you must call the function again with a buffer size at least as large as \**pcbNeeded*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e23-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86e23-129">Return value</span></span>

<span data-ttu-id="86e23-130">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="86e23-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="86e23-131">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="86e23-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e23-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86e23-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86e23-133">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="86e23-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="86e23-134">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="86e23-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="86e23-135">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="86e23-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="86e23-136">Puede llamar a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el archivo de cola de impresión especificado por el miembro de la **ruta de acceso** de la estructura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y, a continuación, llamar a la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para escribir en él los datos del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="86e23-136">You can call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the spool file specified by the **Path** member of the [**ADDJOB\_INFO\_1**](addjob-info-1.md) structure, and then call the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to write print job data to it.</span></span> <span data-ttu-id="86e23-137">Una vez hecho esto, llame a la función [**ScheduleJob**](schedulejob.md) para notificar al administrador de trabajos de impresión que el trabajo de impresión puede ser programado ahora por el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="86e23-137">After that is done, call the [**ScheduleJob**](schedulejob.md) function to notify the print spooler that the print job can now be scheduled by the spooler for printing.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e23-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86e23-138">Requirements</span></span>



| <span data-ttu-id="86e23-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e23-139">Requirement</span></span> | <span data-ttu-id="86e23-140">Value</span><span class="sxs-lookup"><span data-stu-id="86e23-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e23-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86e23-141">Minimum supported client</span></span><br/> | <span data-ttu-id="86e23-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86e23-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86e23-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86e23-143">Minimum supported server</span></span><br/> | <span data-ttu-id="86e23-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86e23-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86e23-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86e23-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e23-146"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86e23-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="86e23-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86e23-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="86e23-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e23-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="86e23-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86e23-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e23-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="86e23-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="86e23-151">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="86e23-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="86e23-152">**AddJobW** (Unicode) y **AddJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="86e23-152">**AddJobW** (Unicode) and **AddJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="86e23-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="86e23-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e23-154">**ADDJOB \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="86e23-154">**ADDJOB\_INFO\_1**</span></span>](addjob-info-1.md)
</dt> <dt>

[<span data-ttu-id="86e23-155">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="86e23-155">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="86e23-156">API de impresión GDI</span><span class="sxs-lookup"><span data-stu-id="86e23-156">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="86e23-157">Impresión</span><span class="sxs-lookup"><span data-stu-id="86e23-157">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="86e23-158">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="86e23-158">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="86e23-159">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="86e23-159">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="86e23-160">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="86e23-160">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="86e23-161">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="86e23-161">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="86e23-162">**Windows. Graphics. Printing**</span><span class="sxs-lookup"><span data-stu-id="86e23-162">**Windows.Graphics.Printing**</span></span>](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[<span data-ttu-id="86e23-163">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="86e23-163">**WriteFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="86e23-164">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="86e23-164">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

