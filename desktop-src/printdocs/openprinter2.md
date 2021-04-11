---
description: Recupera un identificador de la impresora, el servidor de impresión u otros tipos de controladores del subsistema de impresión especificados, mientras se establecen algunas de las opciones de la impresora.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Función OpenPrinter2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910486"
---
# <a name="openprinter2-function"></a><span data-ttu-id="4387e-103">OpenPrinter2 función)</span><span class="sxs-lookup"><span data-stu-id="4387e-103">OpenPrinter2 function</span></span>

<span data-ttu-id="4387e-104">Recupera un identificador de la impresora, el servidor de impresión u otros tipos de controladores del subsistema de impresión especificados, mientras se establecen algunas de las opciones de la impresora.</span><span class="sxs-lookup"><span data-stu-id="4387e-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="4387e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4387e-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="4387e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4387e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4387e-107">*pPrinterName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4387e-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4387e-108">Puntero a una cadena terminada en null que especifica el nombre de la impresora o el servidor de impresión, el objeto de impresora, el XcvMonitor o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="4387e-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="4387e-109">Para un objeto de impresora, use: Nombreimpresora, trabajo xxxx.</span><span class="sxs-lookup"><span data-stu-id="4387e-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="4387e-110">Para un XcvMonitor, use: ServerName, XcvMonitor Nombremonitor.</span><span class="sxs-lookup"><span data-stu-id="4387e-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="4387e-111">Para un XcvPort, use: ServerName, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="4387e-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="4387e-112">**Windows Vista:** Si **es null**, indica el servidor de impresión local.</span><span class="sxs-lookup"><span data-stu-id="4387e-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="4387e-113">*phPrinter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4387e-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4387e-114">Puntero a una variable que recibe un identificador para el objeto de impresora o de servidor de impresión abierto.</span><span class="sxs-lookup"><span data-stu-id="4387e-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="4387e-115">*pDefault* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4387e-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4387e-116">Un puntero a una estructura de [**\_ valores predeterminados de impresora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="4387e-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="4387e-117">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4387e-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4387e-118">*pOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4387e-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4387e-119">Puntero a una estructura [**de \_ Opciones de impresora**](printer-options.md) .</span><span class="sxs-lookup"><span data-stu-id="4387e-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="4387e-120">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4387e-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4387e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4387e-121">Return value</span></span>

<span data-ttu-id="4387e-122">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4387e-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4387e-123">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4387e-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="4387e-124">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="4387e-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4387e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4387e-125">Remarks</span></span>

<span data-ttu-id="4387e-126">No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="4387e-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="4387e-127">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4387e-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4387e-128">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4387e-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4387e-129">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4387e-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4387e-130">La versión ANSI de esta función no está implementada y devuelve un ERROR \_ no \_ admitido.</span><span class="sxs-lookup"><span data-stu-id="4387e-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="4387e-131">El parámetro *pDefault* le permite especificar el tipo de datos y los valores de modo de dispositivo que se usan para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="4387e-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="4387e-132">Sin embargo, puede invalidar estos valores mediante la función [**SetJob**](setjob.md) después de haber iniciado un documento.</span><span class="sxs-lookup"><span data-stu-id="4387e-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="4387e-133">Puede llamar a la función **OpenPrinter2** para abrir un identificador a un servidor de impresión o para determinar los derechos de acceso de cliente a un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="4387e-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="4387e-134">Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName* , establezca los miembros **pDatatype** y **pDevMode** de la estructura [**de \_ valores predeterminados**](printer-defaults.md) de la impresora en **null** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor, como servidor \_ todos los \_ accesos.</span><span class="sxs-lookup"><span data-stu-id="4387e-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="4387e-135">Cuando haya terminado con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="4387e-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="4387e-136">Use el miembro **DesiredAccess** de la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora para especificar los derechos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="4387e-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="4387e-137">Los derechos de acceso pueden ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4387e-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="4387e-138">Valor de acceso deseado</span><span class="sxs-lookup"><span data-stu-id="4387e-138">Desired Access value</span></span>                        | <span data-ttu-id="4387e-139">Significado</span><span class="sxs-lookup"><span data-stu-id="4387e-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4387e-140">\_administrar el acceso a las impresoras \_</span><span class="sxs-lookup"><span data-stu-id="4387e-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="4387e-141">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4387e-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="4387e-142">\_uso de acceso a impresoras \_</span><span class="sxs-lookup"><span data-stu-id="4387e-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="4387e-143">Para realizar operaciones de impresión básicas.</span><span class="sxs-lookup"><span data-stu-id="4387e-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="4387e-144">\_todo el \_ acceso a la impresora</span><span class="sxs-lookup"><span data-stu-id="4387e-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="4387e-145">Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto SINCRONIZAr.</span><span class="sxs-lookup"><span data-stu-id="4387e-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="4387e-146">Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="4387e-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="4387e-147">\_acceso limitado de administración de acceso a impresoras \_ \_</span><span class="sxs-lookup"><span data-stu-id="4387e-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="4387e-148">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="4387e-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="4387e-149">Este valor está disponible a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4387e-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="4387e-150">valores de seguridad genéricos, como WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="4387e-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="4387e-151">Para permitir derechos de acceso de control específicos.</span><span class="sxs-lookup"><span data-stu-id="4387e-151">To allow specific control access rights.</span></span> <span data-ttu-id="4387e-152">Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="4387e-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="4387e-153">Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada a **OpenPrinter2** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor error de \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="4387e-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="4387e-154">Cuando *pPrinterName* es una impresora local, **OpenPrinter2** omite todos los valores de **dwFlags** a los que apunta la estructura de [**\_ Opciones de impresora**](printer-options.md) con *pOptions*, excepto el cambio de cliente de la opción de impresora \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4387e-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="4387e-155">Si se pasa el último, **OpenPrinter2** devolverá el error de \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="4387e-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="4387e-156">En consecuencia, al abrir una impresora local, **OpenPrinter2** no proporciona ninguna ventaja sobre [**OpenPrinter**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4387e-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="4387e-157">**Windows Vista:** Los datos de la impresora devueltos por **OpenPrinter2** se recuperan de una memoria caché local a menos que la **opción de impresora \_ \_ \_ no** esté establecida en el campo **dwFlags** de la estructura de [**\_ Opciones de impresora**](printer-options.md) a la que hace referencia *pOptions*.</span><span class="sxs-lookup"><span data-stu-id="4387e-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="4387e-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4387e-158">Examples</span></span>

<span data-ttu-id="4387e-159">En este ejemplo, **OpenPrinter2** produce un error cuando el \_ acceso a \_ la impresora Manage \_ Limited se pasa a la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora y el usuario no tiene el permiso adecuado.</span><span class="sxs-lookup"><span data-stu-id="4387e-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="4387e-160">Para obtener un programa de ejemplo que muestra cómo usar esta función, consulte [Cómo: imprimir mediante la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="4387e-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4387e-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4387e-161">Requirements</span></span>



| <span data-ttu-id="4387e-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="4387e-162">Requirement</span></span> | <span data-ttu-id="4387e-163">Value</span><span class="sxs-lookup"><span data-stu-id="4387e-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4387e-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4387e-164">Minimum supported client</span></span><br/> | <span data-ttu-id="4387e-165">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4387e-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4387e-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4387e-166">Minimum supported server</span></span><br/> | <span data-ttu-id="4387e-167">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4387e-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4387e-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4387e-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="4387e-169"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4387e-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4387e-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4387e-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="4387e-171"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4387e-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4387e-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4387e-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4387e-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4387e-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4387e-174">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4387e-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4387e-175">**OpenPrinter2W** (Unicode) y **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4387e-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="4387e-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="4387e-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4387e-177">Impresión</span><span class="sxs-lookup"><span data-stu-id="4387e-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4387e-178">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4387e-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4387e-179">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="4387e-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="4387e-180">**\_valores predeterminados de impresora**</span><span class="sxs-lookup"><span data-stu-id="4387e-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="4387e-181">**Opciones de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="4387e-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="4387e-182">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="4387e-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="4387e-183">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="4387e-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="4387e-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="4387e-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="4387e-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4387e-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

