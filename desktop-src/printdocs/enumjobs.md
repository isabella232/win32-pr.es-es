---
description: La función EnumJobs recupera información acerca de un conjunto especificado de trabajos de impresión para una impresora especificada.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Función EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277825"
---
# <a name="enumjobs-function"></a><span data-ttu-id="f96e3-103">EnumJobs función)</span><span class="sxs-lookup"><span data-stu-id="f96e3-103">EnumJobs function</span></span>

<span data-ttu-id="f96e3-104">La función **EnumJobs** recupera información acerca de un conjunto especificado de trabajos de impresión para una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="f96e3-104">The **EnumJobs** function retrieves information about a specified set of print jobs for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f96e3-105">Syntax</span></span>


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="f96e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f96e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96e3-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-108">Identificador del objeto de impresora cuyos trabajos de impresión enumera la función.</span><span class="sxs-lookup"><span data-stu-id="f96e3-108">A handle to the printer object whose print jobs the function enumerates.</span></span> <span data-ttu-id="f96e3-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f96e3-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-110">*FirstJob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-110">*FirstJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-111">Posición de base cero dentro de la cola de impresión del primer trabajo de impresión que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="f96e3-111">The zero-based position within the print queue of the first print job to enumerate.</span></span> <span data-ttu-id="f96e3-112">Por ejemplo, un valor de 0 especifica que la enumeración debe comenzar en el primer trabajo de impresión de la cola de impresión; un valor de 9 especifica que la enumeración debe comenzar en el décimo trabajo de impresión en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="f96e3-112">For example, a value of 0 specifies that enumeration should begin at the first print job in the print queue; a value of 9 specifies that enumeration should begin at the tenth print job in the print queue.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-113">*Nojobs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-113">*NoJobs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-114">Número total de trabajos de impresión que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="f96e3-114">The total number of print jobs to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-115">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-116">Tipo de información que se devuelve en el búfer de *pJob* .</span><span class="sxs-lookup"><span data-stu-id="f96e3-116">The type of information returned in the *pJob* buffer.</span></span>



| <span data-ttu-id="f96e3-117">Value</span><span class="sxs-lookup"><span data-stu-id="f96e3-117">Value</span></span>                                                                                                | <span data-ttu-id="f96e3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f96e3-118">Meaning</span></span>                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f96e3-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f96e3-120">*pJob* recibe una matriz de estructuras de [**información de trabajo \_ \_ 1**](job-info-1.md)</span><span class="sxs-lookup"><span data-stu-id="f96e3-120">*pJob* receives an array of [**JOB\_INFO\_1**](job-info-1.md) structures</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f96e3-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f96e3-122">*pJob* recibe una matriz de estructuras [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f96e3-122">*pJob* receives an array of [**JOB\_INFO\_2**](job-info-2.md) structures</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="f96e3-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f96e3-124">*pJob* recibe una matriz de estructuras [**Job \_ info \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="f96e3-124">*pJob* receives an array of [**JOB\_INFO\_3**](job-info-3.md) structures</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f96e3-125">*pJob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-125">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-126">Un puntero a un búfer que recibe una matriz de las estructuras Job [**\_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 3**](job-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="f96e3-126">A pointer to a buffer that receives an array of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures.</span></span> <span data-ttu-id="f96e3-127">El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y cualquier cadena u otros datos a los que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="f96e3-127">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="f96e3-128">Para determinar el tamaño de búfer necesario, llame a **EnumJobs** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="f96e3-128">To determine the required buffer size, call **EnumJobs** with *cbBuf* set to zero.</span></span> <span data-ttu-id="f96e3-129">**EnumJobs** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="f96e3-129">**EnumJobs** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-130">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-130">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-131">Tamaño, en bytes, del búfer *pJob* .</span><span class="sxs-lookup"><span data-stu-id="f96e3-131">The size, in bytes, of the *pJob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-132">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-132">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-133">Puntero a una variable que recibe el número de bytes copiados si la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="f96e3-133">A pointer to a variable that receives the number of bytes copied if the function succeeds.</span></span> <span data-ttu-id="f96e3-134">Si se produce un error en la función, la variable recibe el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="f96e3-134">If the function fails, the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="f96e3-135">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f96e3-135">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f96e3-136">Un puntero a una variable que recibe el número de las estructuras Job [**\_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 3**](job-info-3.md) devueltas en el búfer de *pJob* .</span><span class="sxs-lookup"><span data-stu-id="f96e3-136">A pointer to a variable that receives the number of [**JOB\_INFO\_1**](job-info-1.md), [**JOB\_INFO\_2**](job-info-2.md), or [**JOB\_INFO\_3**](job-info-3.md) structures returned in the *pJob* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96e3-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f96e3-137">Return value</span></span>

<span data-ttu-id="f96e3-138">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f96e3-138">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f96e3-139">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f96e3-139">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f96e3-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f96e3-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f96e3-141">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f96e3-141">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f96e3-142">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f96e3-142">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f96e3-143">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f96e3-143">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f96e3-144">La estructura [**Job \_ info \_ 1**](job-info-1.md) contiene información general sobre el trabajo de impresión; la estructura de la información de [**trabajo \_ \_ 2**](job-info-2.md) tiene información mucho más detallada.</span><span class="sxs-lookup"><span data-stu-id="f96e3-144">The [**JOB\_INFO\_1**](job-info-1.md) structure contains general print-job information; the [**JOB\_INFO\_2**](job-info-2.md) structure has much more detailed information.</span></span> <span data-ttu-id="f96e3-145">La estructura [**Job \_ info \_ 3**](job-info-3.md) contiene información sobre cómo se vinculan los trabajos.</span><span class="sxs-lookup"><span data-stu-id="f96e3-145">The [**JOB\_INFO\_3**](job-info-3.md) structure contains information about how jobs are linked.</span></span>

<span data-ttu-id="f96e3-146">Para determinar el número de trabajos de impresión en la cola de la impresora, llame a la función [**GetPrinter**](getprinter.md) con el parámetro *LEVEL* establecido en 2.</span><span class="sxs-lookup"><span data-stu-id="f96e3-146">To determine the number of print jobs in the printer queue, call the [**GetPrinter**](getprinter.md) function with the *Level* parameter set to 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96e3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f96e3-147">Requirements</span></span>



| <span data-ttu-id="f96e3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96e3-148">Requirement</span></span> | <span data-ttu-id="f96e3-149">Value</span><span class="sxs-lookup"><span data-stu-id="f96e3-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96e3-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f96e3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f96e3-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f96e3-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f96e3-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f96e3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f96e3-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f96e3-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f96e3-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f96e3-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f96e3-155"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f96e3-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f96e3-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="f96e3-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f96e3-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f96e3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f96e3-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f96e3-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f96e3-160">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f96e3-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f96e3-161">**EnumJobsW** (Unicode) y **EnumJobsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f96e3-161">**EnumJobsW** (Unicode) and **EnumJobsA** (ANSI)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="f96e3-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="f96e3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96e3-163">Impresión</span><span class="sxs-lookup"><span data-stu-id="f96e3-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f96e3-164">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f96e3-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f96e3-165">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="f96e3-165">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="f96e3-166">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f96e3-166">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f96e3-167">**Información de trabajo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f96e3-167">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="f96e3-168">**Información de trabajo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f96e3-168">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="f96e3-169">**Información de trabajo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f96e3-169">**JOB\_INFO\_3**</span></span>](job-info-3.md)
</dt> <dt>

[<span data-ttu-id="f96e3-170">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f96e3-170">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f96e3-171">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="f96e3-171">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

