---
description: La función ScheduleJob solicita que el administrador de trabajos de impresión programe un trabajo de impresión especificado para imprimirlo.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Función ScheduleJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716485"
---
# <a name="schedulejob-function"></a><span data-ttu-id="c84ed-103">ScheduleJob función)</span><span class="sxs-lookup"><span data-stu-id="c84ed-103">ScheduleJob function</span></span>

<span data-ttu-id="c84ed-104">La función **ScheduleJob** solicita que el administrador de trabajos de impresión programe un trabajo de impresión especificado para imprimirlo.</span><span class="sxs-lookup"><span data-stu-id="c84ed-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c84ed-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="c84ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c84ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84ed-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c84ed-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84ed-108">Identificador de la impresora para el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="c84ed-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="c84ed-109">Debe ser una impresora local configurada como una impresora en cola.</span><span class="sxs-lookup"><span data-stu-id="c84ed-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="c84ed-110">Si *hPrinter* es un identificador de una conexión de impresora remota, o si la impresora está configurada para impresión directa, se produce un error en la función **ScheduleJob** .</span><span class="sxs-lookup"><span data-stu-id="c84ed-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="c84ed-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="c84ed-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="c84ed-112">*hPrinter* debe ser el mismo identificador de impresora especificado en la llamada a [**AddJob**](addjob.md) que obtuvo el identificador de trabajo de impresión *dwJobID* .</span><span class="sxs-lookup"><span data-stu-id="c84ed-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c84ed-113">*dwJobID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c84ed-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84ed-114">Trabajo de impresión que se va a programar.</span><span class="sxs-lookup"><span data-stu-id="c84ed-114">The print job to be scheduled.</span></span> <span data-ttu-id="c84ed-115">Para obtener este identificador de trabajo de impresión, llame a la función [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="c84ed-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84ed-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c84ed-116">Return value</span></span>

<span data-ttu-id="c84ed-117">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c84ed-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c84ed-118">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c84ed-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84ed-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c84ed-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c84ed-120">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c84ed-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c84ed-121">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c84ed-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c84ed-122">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="c84ed-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c84ed-123">Debe llamar correctamente a la función [**AddJob**](addjob.md) antes de llamar a la función **ScheduleJob** .</span><span class="sxs-lookup"><span data-stu-id="c84ed-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="c84ed-124">**AddJob** obtiene el identificador del trabajo de impresión que se pasa a **ScheduleJob** como *dwJobID*.</span><span class="sxs-lookup"><span data-stu-id="c84ed-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="c84ed-125">Ambas llamadas deben usar el mismo valor para *hPrinter*.</span><span class="sxs-lookup"><span data-stu-id="c84ed-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="c84ed-126">La función **ScheduleJob** comprueba si existe un archivo de cola válido.</span><span class="sxs-lookup"><span data-stu-id="c84ed-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="c84ed-127">Si hay un archivo de cola no válido, o si está vacío, **ScheduleJob** elimina tanto el archivo de cola como la entrada de trabajo de impresión correspondiente en el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="c84ed-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84ed-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84ed-128">Requirements</span></span>



| <span data-ttu-id="c84ed-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84ed-129">Requirement</span></span> | <span data-ttu-id="c84ed-130">Value</span><span class="sxs-lookup"><span data-stu-id="c84ed-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84ed-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84ed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c84ed-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c84ed-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c84ed-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84ed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c84ed-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c84ed-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c84ed-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c84ed-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84ed-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c84ed-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c84ed-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c84ed-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c84ed-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c84ed-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c84ed-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c84ed-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84ed-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84ed-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c84ed-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84ed-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84ed-142">Impresión</span><span class="sxs-lookup"><span data-stu-id="c84ed-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c84ed-143">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="c84ed-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c84ed-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="c84ed-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="c84ed-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c84ed-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




