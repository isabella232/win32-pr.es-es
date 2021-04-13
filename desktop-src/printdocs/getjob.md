---
description: La función GetJob recupera información acerca de un trabajo de impresión especificado.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Función GetJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276779"
---
# <a name="getjob-function"></a><span data-ttu-id="9a7d2-103">GetJob función)</span><span class="sxs-lookup"><span data-stu-id="9a7d2-103">GetJob function</span></span>

<span data-ttu-id="9a7d2-104">La función **GetJob** recupera información acerca de un trabajo de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-104">The **GetJob** function retrieves information about a specified print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a7d2-105">Syntax</span></span>


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="9a7d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a7d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7d2-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-108">Identificador de la impresora para la que se recuperan los datos del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-108">A handle to the printer for which the print-job data is retrieved.</span></span> <span data-ttu-id="9a7d2-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9a7d2-110">*JobID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-110">*JobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-111">Identifica el trabajo de impresión para el que se van a recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="9a7d2-112">Use la función [**AddJob**](addjob.md) o la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9a7d2-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-114">Tipo de información que se devuelve en el búfer de *pJob* .</span><span class="sxs-lookup"><span data-stu-id="9a7d2-114">The type of information returned in the *pJob* buffer.</span></span> <span data-ttu-id="9a7d2-115">Si el *nivel* es 1, *pJob* recibe una estructura [**Job \_ info \_ 1**](job-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7d2-115">If *Level* is 1, *pJob* receives a [**JOB\_INFO\_1**](job-info-1.md) structure.</span></span> <span data-ttu-id="9a7d2-116">Si el *nivel* es 2, *pJob* recibe una estructura [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7d2-116">If *Level* is 2, *pJob* receives a [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a7d2-117">*pJob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-117">*pJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-118">Un puntero a un búfer que recibe la información de [**trabajo \_ \_ 1**](job-info-1.md) o una estructura de la [**información de trabajo \_ \_ 2**](job-info-2.md) que contiene información sobre el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-118">A pointer to a buffer that receives a [**JOB\_INFO\_1**](job-info-1.md) or a [**JOB\_INFO\_2**](job-info-2.md) structure containing information about the job.</span></span> <span data-ttu-id="9a7d2-119">El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-119">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="9a7d2-120">Para determinar el tamaño de búfer necesario, llame a **GetJob** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-120">To determine the required buffer size, call **GetJob** with *cbBuf* set to zero.</span></span> <span data-ttu-id="9a7d2-121">**GetJob** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-121">**GetJob** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="9a7d2-122">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-123">Tamaño, en bytes, de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-123">The size, in bytes, of the array.</span></span>

</dd> <dt>

<span data-ttu-id="9a7d2-124">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a7d2-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7d2-125">Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-125">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7d2-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a7d2-126">Return value</span></span>

<span data-ttu-id="9a7d2-127">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-127">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9a7d2-128">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-128">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7d2-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a7d2-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a7d2-130">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9a7d2-131">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9a7d2-132">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="9a7d2-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a7d2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7d2-133">Requirements</span></span>



| <span data-ttu-id="9a7d2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7d2-134">Requirement</span></span> | <span data-ttu-id="9a7d2-135">Value</span><span class="sxs-lookup"><span data-stu-id="9a7d2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7d2-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7d2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7d2-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9a7d2-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a7d2-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7d2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7d2-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a7d2-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a7d2-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a7d2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7d2-141"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a7d2-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9a7d2-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a7d2-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a7d2-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a7d2-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9a7d2-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a7d2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a7d2-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9a7d2-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9a7d2-146">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9a7d2-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9a7d2-147">**GetJobW** (Unicode) y **GetJobA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9a7d2-147">**GetJobW** (Unicode) and **GetJobA** (ANSI)</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="9a7d2-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a7d2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7d2-149">Impresión</span><span class="sxs-lookup"><span data-stu-id="9a7d2-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-150">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="9a7d2-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-151">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="9a7d2-151">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-152">**Información de trabajo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9a7d2-152">**JOB\_INFO\_1**</span></span>](job-info-1.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-153">**Información de trabajo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9a7d2-153">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-154">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="9a7d2-154">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="9a7d2-155">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="9a7d2-155">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

