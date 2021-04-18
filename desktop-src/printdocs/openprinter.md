---
description: La función OpenPrinter recupera un identificador de la impresora o del servidor de impresión especificado u otros tipos de controladores en el subsistema de impresión.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Función OpenPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648415"
---
# <a name="openprinter-function"></a><span data-ttu-id="8a1a3-103">OpenPrinter función)</span><span class="sxs-lookup"><span data-stu-id="8a1a3-103">OpenPrinter function</span></span>

<span data-ttu-id="8a1a3-104">La función **OpenPrinter** recupera un identificador de la impresora o del servidor de impresión especificado u otros tipos de controladores en el subsistema de impresión.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a1a3-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="8a1a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a1a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1a3-107">*pPrinterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a1a3-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1a3-108">Un puntero a una cadena terminada en null que especifica el nombre de la impresora o el servidor de impresión, el objeto Printer, el XcvMonitor o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="8a1a3-109">Para un objeto de impresora, use: Nombreimpresora, trabajo xxxx.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="8a1a3-110">Para un XcvMonitor, use: ServerName, XcvMonitor Nombremonitor.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="8a1a3-111">Para un XcvPort, use: ServerName, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="8a1a3-112">Si **es null**, indica el servidor de impresión local.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="8a1a3-113">*phPrinter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a1a3-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1a3-114">Puntero a una variable que recibe un identificador (no seguro para subprocesos) para el objeto de impresora o servidor de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="8a1a3-115">El parámetro *phPrinter* puede devolver un identificador de Xcv para su uso con la función XcvData.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="8a1a3-116">Para obtener más información sobre XcvData, consulte el DDK.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="8a1a3-117">*pDefault* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a1a3-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a1a3-118">Un puntero a una estructura de [**\_ valores predeterminados de impresora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="8a1a3-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="8a1a3-119">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1a3-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a1a3-120">Return value</span></span>

<span data-ttu-id="8a1a3-121">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8a1a3-122">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a1a3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a1a3-123">Remarks</span></span>

<span data-ttu-id="8a1a3-124">No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="8a1a3-125">Un identificador obtenido para una impresora remota mediante una llamada a **OpenPrinter** para una impresora remota obtiene acceso a la impresora a través de una memoria caché local en el servicio Administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="8a1a3-126">Esta caché no es precisa en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="8a1a3-127">Para obtener datos precisos, reemplace la llamada a OpenPrinter por [**OpenPrinter2**](openprinter2.md) con POptions. dwFlags establecida en la opción de impresora \_ \_ sin \_ caché.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="8a1a3-128">Tenga en cuenta que solo OpenPrinter2W es funcional.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="8a1a3-129">La función devuelve un identificador de impresora que utiliza otras llamadas a la API de impresión y omite la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="8a1a3-130">Este método se bloquea mientras se espera la comunicación de red con la impresora remota, por lo que podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="8a1a3-131">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8a1a3-132">La llamada a esta función desde un subproceso que administra la interacción con la interfaz de usuario puede hacer que la aplicación parezca que no responde.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="8a1a3-133">Un identificador obtenido mediante una llamada a **OpenPrinter** para una impresora remota tendrá acceso a la impresora a través de una memoria caché local en el servicio Administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="8a1a3-134">Esta caché es, por diseño, no precisa en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="8a1a3-135">Si necesita obtener datos precisos, reemplace la llamada a **OpenPrinter** por [**OpenPrinter2**](openprinter2.md) con *pOptions. dwFlags* establecida en la [**opción de impresora \_ \_ sin \_ caché**](printer-options.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="8a1a3-136">Tenga en cuenta que solo **OpenPrinter2W** es funcional.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="8a1a3-137">De este modo, la función devuelve un identificador de impresora que hace que otras llamadas a la API de impresión omitan la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="8a1a3-138">Tenga en cuenta que este enfoque se bloqueará mientras se espera la comunicación de red de ida y vuelta a la impresora remota, por lo que es posible que no se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="8a1a3-139">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8a1a3-140">Por lo tanto, llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8a1a3-141">El identificador al que apunta *phPrinter* no es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="8a1a3-142">Si los autores de las llamadas necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de la impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="8a1a3-143">Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="8a1a3-144">El parámetro *pDefault* le permite especificar el tipo de datos y los valores de modo de dispositivo que se usan para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="8a1a3-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="8a1a3-145">Sin embargo, puede invalidar estos valores mediante la función [**SetJob**](setjob.md) después de haber iniciado un documento.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="8a1a3-146">La configuración de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definida en la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora del parámetro *pDefault* no se usa cuando el valor del miembro *pDatatype* de la estructura [**doc \_ info \_ 1**](doc-info-1.md) que se pasó en el parámetro *pDocInfo* de la llamada [**StartDocPrinter**](startdocprinter.md) es "RAW".</span><span class="sxs-lookup"><span data-stu-id="8a1a3-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="8a1a3-147">Cuando un documento de alto nivel (como un archivo de Adobe PDF o Microsoft Word) u otros datos de impresora (como PCL, PS o HPGL) se envían directamente a una impresora con *pDatatype* establecido en "RAW", el documento debe describir por completo la configuración del trabajo de impresión de estilo **DEVMODE** en el idioma que comprenda el hardware.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="8a1a3-148">Puede llamar a la función **OpenPrinter** para abrir un identificador a un servidor de impresión o para determinar los derechos de acceso que un cliente tiene a un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="8a1a3-149">Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName* , establezca los miembros **pDatatype** y **pDevMode** de la estructura [**de \_ valores predeterminados**](printer-defaults.md) de la impresora en **null** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor, como servidor \_ todos los \_ accesos.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="8a1a3-150">Cuando termine con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="8a1a3-151">Use el miembro **DesiredAccess** de la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora para especificar los derechos de acceso que necesita a la impresora.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="8a1a3-152">Los derechos de acceso pueden ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-152">The access rights can be one of the following.</span></span> <span data-ttu-id="8a1a3-153">(Si *pDefault* es **null**, los derechos de acceso son Printer \_ uso de acceso \_ ).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="8a1a3-154">Valor de acceso deseado</span><span class="sxs-lookup"><span data-stu-id="8a1a3-154">Desired Access value</span></span>                        | <span data-ttu-id="8a1a3-155">Significado</span><span class="sxs-lookup"><span data-stu-id="8a1a3-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1a3-156">\_administrar el acceso a las impresoras \_</span><span class="sxs-lookup"><span data-stu-id="8a1a3-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="8a1a3-157">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="8a1a3-158">\_uso de acceso a impresoras \_</span><span class="sxs-lookup"><span data-stu-id="8a1a3-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="8a1a3-159">Para realizar operaciones de impresión básicas.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="8a1a3-160">\_todo el \_ acceso a la impresora</span><span class="sxs-lookup"><span data-stu-id="8a1a3-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="8a1a3-161">Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto la sincronización (consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="8a1a3-162">\_acceso limitado de administración de acceso a impresoras \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a1a3-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="8a1a3-163">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="8a1a3-164">Este valor está disponible a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="8a1a3-165">valores de seguridad genéricos, como WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="8a1a3-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="8a1a3-166">Para permitir derechos de acceso de control específicos.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-166">To allow specific control access rights.</span></span> <span data-ttu-id="8a1a3-167">Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="8a1a3-168">Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada **OpenPrinter** con un valor devuelto de cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor error de \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="8a1a3-169">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8a1a3-169">Examples</span></span>

<span data-ttu-id="8a1a3-170">Para obtener un programa de ejemplo que usa esta función, consulte [Cómo: imprimir con la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1a3-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a1a3-171">Requirements</span></span>



| <span data-ttu-id="8a1a3-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1a3-172">Requirement</span></span> | <span data-ttu-id="8a1a3-173">Value</span><span class="sxs-lookup"><span data-stu-id="8a1a3-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1a3-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a1a3-174">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1a3-175">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8a1a3-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8a1a3-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a1a3-176">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1a3-177">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a1a3-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a1a3-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a1a3-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a1a3-179"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a1a3-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a1a3-180">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a1a3-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a1a3-181"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a1a3-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8a1a3-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a1a3-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a1a3-183"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8a1a3-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8a1a3-184">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8a1a3-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a1a3-185">**OpenPrinterW** (Unicode) y **OpenPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a1a3-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="8a1a3-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a1a3-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1a3-187">Impresión</span><span class="sxs-lookup"><span data-stu-id="8a1a3-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-188">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8a1a3-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-189">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-191">**\_valores predeterminados de impresora**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-192">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-193">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="8a1a3-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="8a1a3-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

