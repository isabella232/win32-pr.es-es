---
description: La función SetPrinterData establece los datos de configuración de una impresora o un servidor de impresión.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Función SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909369"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="21cf0-103">SetPrinterData función)</span><span class="sxs-lookup"><span data-stu-id="21cf0-103">SetPrinterData function</span></span>

<span data-ttu-id="21cf0-104">La función **SetPrinterData** establece los datos de configuración de una impresora o un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="21cf0-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="21cf0-105">Para especificar la clave del registro en la que se almacenan los datos, llame a la función [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="21cf0-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="21cf0-106">Llamar a **SetPrinterData** es equivalente a llamar a la función **SetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="21cf0-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="21cf0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21cf0-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="21cf0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21cf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cf0-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21cf0-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cf0-110">Identificador de la impresora o del servidor de impresión para el que la función establece los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="21cf0-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="21cf0-111">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="21cf0-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="21cf0-112">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21cf0-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cf0-113">Puntero a una cadena terminada en null que identifica los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="21cf0-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="21cf0-114">En el caso de las impresoras, esta cadena es el nombre de un valor del registro en la clave "PrinterDriverData" de la impresora del registro.</span><span class="sxs-lookup"><span data-stu-id="21cf0-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="21cf0-115">En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="21cf0-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="21cf0-116">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="21cf0-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cf0-117">Código que indica el tipo de datos al que apunta el parámetro *pdata* .</span><span class="sxs-lookup"><span data-stu-id="21cf0-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="21cf0-118">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="21cf0-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="21cf0-119">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21cf0-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cf0-120">Puntero a una matriz de bytes que contiene los datos de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="21cf0-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="21cf0-121">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21cf0-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21cf0-122">Tamaño, en bytes, de la matriz.</span><span class="sxs-lookup"><span data-stu-id="21cf0-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cf0-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21cf0-123">Return value</span></span>

<span data-ttu-id="21cf0-124">Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="21cf0-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="21cf0-125">Si se produce un error en la función, el valor devuelto es un valor de error.</span><span class="sxs-lookup"><span data-stu-id="21cf0-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21cf0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21cf0-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21cf0-127">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="21cf0-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="21cf0-128">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="21cf0-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="21cf0-129">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="21cf0-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="21cf0-130">Para recuperar los datos de configuración existentes de una impresora, llame a la función [**GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="21cf0-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="21cf0-131">Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="21cf0-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="21cf0-132">Value</span><span class="sxs-lookup"><span data-stu-id="21cf0-132">Value</span></span>                                                               | <span data-ttu-id="21cf0-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21cf0-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cf0-134">**SPLREG \_ permitir el \_ usuario \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="21cf0-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="21cf0-135">Windows XP con Service Pack 2 (SP2) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="21cf0-136">Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="21cf0-137">**SPLREG \_ beep \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="21cf0-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-138">**\_Directorio de \_ cola de impresión predeterminado de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-139">**\_registro de eventos de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-140">**\_ \_ menú emergente de SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="21cf0-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="21cf0-141">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="21cf0-142">**\_ \_ \_ valor predeterminado de prioridad de subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-143">**\_prioridad de \_ subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-144">**SPLREG \_ \_ grupos de \_ aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="21cf0-145">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-146">**SPLREG \_ tiempo de aislamiento de controladores de impresión \_ antes de \_ \_ \_ \_ reciclar**</span><span class="sxs-lookup"><span data-stu-id="21cf0-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="21cf0-147">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-148">**SPLREG de \_ aislamiento de controlador de impresión máximo de \_ \_ \_ \_ objetos antes del \_ \_ reciclaje**</span><span class="sxs-lookup"><span data-stu-id="21cf0-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="21cf0-149">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-150">**\_tiempo de \_ \_ espera de \_ inactividad de controlador de impresión SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="21cf0-151">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-152">**SPLREG \_ \_ Directiva de \_ ejecución de aislamiento de controladores de \_ impresión \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="21cf0-153">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-154">**SPLREG \_ \_ Directiva de \_ \_ invalidación de aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="21cf0-155">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="21cf0-156">**\_elemento emergente de reintento de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="21cf0-157">Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.</span><span class="sxs-lookup"><span data-stu-id="21cf0-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="21cf0-158">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="21cf0-159">**\_prioridad de \_ subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-160">**\_ \_ \_ prioridad predeterminada del subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="21cf0-161">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="21cf0-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="21cf0-162">Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="21cf0-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="21cf0-163">Los siguientes valores de *pValueName* determinan el comportamiento de impresión del grupo cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="21cf0-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="21cf0-164">Value</span><span class="sxs-lookup"><span data-stu-id="21cf0-164">Value</span></span>                                       | <span data-ttu-id="21cf0-165">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21cf0-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cf0-166">**\_ \_ error al reiniciar el trabajo \_ de SPLREG en el \_ grupo \_**</span><span class="sxs-lookup"><span data-stu-id="21cf0-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="21cf0-167">El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="21cf0-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="21cf0-168">Esta configuración se usa con **el \_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="21cf0-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="21cf0-169">**\_ \_ trabajo de reinicio de SPLREG \_ en \_ grupo \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="21cf0-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="21cf0-170">Un valor distinto de cero en *pdata* indica que está habilitado el **\_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_** .</span><span class="sxs-lookup"><span data-stu-id="21cf0-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="21cf0-171">La hora especificada en **el \_ trabajo de reinicio de SPLREG \_ en el \_ \_ \_ error de grupo** es un tiempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="21cf0-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="21cf0-172">La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:</span><span class="sxs-lookup"><span data-stu-id="21cf0-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="21cf0-173">**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**</span><span class="sxs-lookup"><span data-stu-id="21cf0-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="21cf0-174">Llame a la función [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para establecer estos valores.</span><span class="sxs-lookup"><span data-stu-id="21cf0-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="21cf0-175">Configuración del monitor de Puerto</span><span class="sxs-lookup"><span data-stu-id="21cf0-175">Port monitor setting</span></span>     | <span data-ttu-id="21cf0-176">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="21cf0-176">Data type</span></span>      | <span data-ttu-id="21cf0-177">Significado</span><span class="sxs-lookup"><span data-stu-id="21cf0-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cf0-178">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="21cf0-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="21cf0-179">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="21cf0-179">**REG\_DWORD**</span></span> | <span data-ttu-id="21cf0-180">Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="21cf0-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="21cf0-181">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="21cf0-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="21cf0-182">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="21cf0-182">**REG\_DWORD**</span></span> | <span data-ttu-id="21cf0-183">Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="21cf0-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="21cf0-184">En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="21cf0-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="21cf0-185">La representación del lado cliente de un trabajo de impresión se puede configurar para cada impresora mediante el establecimiento de los siguientes valores en *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="21cf0-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="21cf0-186">Configuración</span><span class="sxs-lookup"><span data-stu-id="21cf0-186">Setting</span></span>                      | <span data-ttu-id="21cf0-187">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="21cf0-187">Data type</span></span>      | <span data-ttu-id="21cf0-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="21cf0-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cf0-189">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="21cf0-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="21cf0-190">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="21cf0-190">**REG\_DWORD**</span></span> | <span data-ttu-id="21cf0-191">Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="21cf0-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="21cf0-192">Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="21cf0-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="21cf0-193">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="21cf0-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="21cf0-194">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="21cf0-194">**REG\_DWORD**</span></span> | <span data-ttu-id="21cf0-195">Un valor de 0, o si este valor no está presente en el registro, hace que los trabajos de impresión se representen en el cliente.</span><span class="sxs-lookup"><span data-stu-id="21cf0-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="21cf0-196">Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor.</span><span class="sxs-lookup"><span data-stu-id="21cf0-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="21cf0-197">Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="21cf0-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="21cf0-198">Un valor de 1 representará los trabajos de impresión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="21cf0-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="21cf0-199">Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="21cf0-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21cf0-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21cf0-200">Requirements</span></span>



| <span data-ttu-id="21cf0-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="21cf0-201">Requirement</span></span> | <span data-ttu-id="21cf0-202">Value</span><span class="sxs-lookup"><span data-stu-id="21cf0-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21cf0-203">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21cf0-203">Minimum supported client</span></span><br/> | <span data-ttu-id="21cf0-204">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="21cf0-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="21cf0-205">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21cf0-205">Minimum supported server</span></span><br/> | <span data-ttu-id="21cf0-206">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21cf0-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="21cf0-207">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21cf0-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="21cf0-208"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21cf0-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="21cf0-209">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21cf0-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="21cf0-210"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21cf0-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="21cf0-211">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21cf0-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21cf0-212"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="21cf0-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="21cf0-213">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="21cf0-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="21cf0-214">**SetPrinterDataW** (Unicode) y **SetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="21cf0-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="21cf0-215">Vea también</span><span class="sxs-lookup"><span data-stu-id="21cf0-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cf0-216">Impresión</span><span class="sxs-lookup"><span data-stu-id="21cf0-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="21cf0-217">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="21cf0-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="21cf0-218">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="21cf0-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="21cf0-219">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="21cf0-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="21cf0-220">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="21cf0-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="21cf0-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="21cf0-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="21cf0-222">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="21cf0-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

