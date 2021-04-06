---
description: Notifica al servicio Administrador de trabajos de impresión si un trabajo de impresión XPS está en cola o en la fase de representación y qué parte del procesamiento está en curso actualmente.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Función ReportJobProcessingProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002403"
---
# <a name="reportjobprocessingprogress-function"></a><span data-ttu-id="4a6a8-103">ReportJobProcessingProgress función)</span><span class="sxs-lookup"><span data-stu-id="4a6a8-103">ReportJobProcessingProgress function</span></span>

<span data-ttu-id="4a6a8-104">Notifica al servicio Administrador de trabajos de impresión si un trabajo de impresión XPS está en cola o en la fase de representación y qué parte del procesamiento está en curso actualmente.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-104">Reports to the Print Spooler service whether an XPS print job is in the spooling or the rendering phase and what part of the processing is currently underway.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a6a8-105">Syntax</span></span>


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a><span data-ttu-id="4a6a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a6a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6a8-107">*printerHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a6a8-107">*printerHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6a8-108">Identificador de impresora para el que la función va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-108">A printer handle for which the function is to retrieve information.</span></span> <span data-ttu-id="4a6a8-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4a6a8-110">*jobId* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4a6a8-110">*jobId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6a8-111">Identifica el trabajo de impresión para el que se van a recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-111">Identifies the print job for which to retrieve data.</span></span> <span data-ttu-id="4a6a8-112">Use la función [**AddJob**](addjob.md) o la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-112">Use the [**AddJob**](addjob.md) function or [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function to get a print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4a6a8-113">*jobOperation*</span><span class="sxs-lookup"><span data-stu-id="4a6a8-113">*jobOperation*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6a8-114">Especifica si el trabajo está en la fase de puesta en cola o en la fase de representación.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-114">Specifies whether the job is in the spooling phase or the rendering phase.</span></span>

</dd> <dt>

<span data-ttu-id="4a6a8-115">*jobProgress*</span><span class="sxs-lookup"><span data-stu-id="4a6a8-115">*jobProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6a8-116">Especifica qué parte del procesamiento está en curso actualmente.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-116">Specifies what part of the processing is currently underway.</span></span> <span data-ttu-id="4a6a8-117">Este valor hace referencia a los eventos de la fase de puesta en cola o de representación, en función del valor de *jobOperation*.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-117">This value refers to events in either the spooling or rendering phase depending on the value of *jobOperation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6a8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a6a8-118">Return value</span></span>

<span data-ttu-id="4a6a8-119">Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-119">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="4a6a8-120">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="4a6a8-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6a8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a6a8-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a6a8-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4a6a8-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4a6a8-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a6a8-125">**ReportJobProcessingProgress** solo notificará el progreso del trabajo de impresión XPS si el trabajo de impresión se encuentra en la fase de puesta en cola o representación.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-125">**ReportJobProcessingProgress** will only report the progress of the XPS print job if the print job is in the spooling or rendering phase.</span></span> <span data-ttu-id="4a6a8-126">**ReportJobProcessingProgress** producirá un error si se llama cuando el trabajo de impresión XPS no está en la fase de puesta en cola o representación.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-126">**ReportJobProcessingProgress** will fail if it is called when the XPS print job is not in the spooling or rendering phase.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a6a8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a6a8-127">Requirements</span></span>



| <span data-ttu-id="4a6a8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a6a8-128">Requirement</span></span> | <span data-ttu-id="4a6a8-129">Value</span><span class="sxs-lookup"><span data-stu-id="4a6a8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6a8-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a6a8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6a8-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a6a8-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4a6a8-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a6a8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6a8-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a6a8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a6a8-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a6a8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6a8-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a6a8-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4a6a8-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a6a8-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a6a8-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a6a8-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4a6a8-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a6a8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a6a8-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a6a8-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4a6a8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a6a8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6a8-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="4a6a8-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4a6a8-142">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4a6a8-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4a6a8-143">**EPrintXPSJobOperation**</span><span class="sxs-lookup"><span data-stu-id="4a6a8-143">**EPrintXPSJobOperation**</span></span>](eprintxpsjoboperation.md)
</dt> <dt>

[<span data-ttu-id="4a6a8-144">**EPrintXPSJobProgress**</span><span class="sxs-lookup"><span data-stu-id="4a6a8-144">**EPrintXPSJobProgress**</span></span>](eprintxpsjobprogress.md)
</dt> </dl>

 

