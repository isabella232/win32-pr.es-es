---
description: La función SetPrinterDataEx establece los datos de configuración de una impresora o un servidor de impresión. La función almacena los datos de configuración en la clave del registro Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Función SetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278645"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="74ba1-104">SetPrinterDataEx función)</span><span class="sxs-lookup"><span data-stu-id="74ba1-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="74ba1-105">La función **SetPrinterDataEx** establece los datos de configuración de una impresora o un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ba1-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="74ba1-106">La función almacena los datos de configuración en la clave del registro de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ba1-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ba1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74ba1-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="74ba1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74ba1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ba1-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-110">Identificador de la impresora o del servidor de impresión para el que la función establece los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="74ba1-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="74ba1-111">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="74ba1-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="74ba1-112">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-113">Puntero a una cadena terminada en null que especifica la clave que contiene el valor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="74ba1-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="74ba1-114">Si la clave o las subclaves especificadas no existen, la función las crea.</span><span class="sxs-lookup"><span data-stu-id="74ba1-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="74ba1-115">Para almacenar los datos de configuración que se pueden publicar en el servicio de directorio (DS), especifique una de las siguientes claves del registro predefinidas.</span><span class="sxs-lookup"><span data-stu-id="74ba1-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="74ba1-116">Value</span><span class="sxs-lookup"><span data-stu-id="74ba1-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="74ba1-117">Significado</span><span class="sxs-lookup"><span data-stu-id="74ba1-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="74ba1-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="74ba1-119">Controladores de impresora use esta clave para almacenar las propiedades del controlador.</span><span class="sxs-lookup"><span data-stu-id="74ba1-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="74ba1-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="74ba1-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="74ba1-121">Reserved.</span></span> <span data-ttu-id="74ba1-122">Solo lo utiliza el administrador de trabajos de impresión para almacenar propiedades internas del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ba1-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="74ba1-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="74ba1-124">Las aplicaciones usan esta clave para almacenar propiedades de impresora, como números de activos de impresora.</span><span class="sxs-lookup"><span data-stu-id="74ba1-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="74ba1-125">Los valores que se almacenan en la clave SPLDS_USER_KEY se publican en el servicio de directorio solo si hay una propiedad correspondiente en el esquema.</span><span class="sxs-lookup"><span data-stu-id="74ba1-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="74ba1-126">Un administrador de dominio debe crear la propiedad si aún no existe.</span><span class="sxs-lookup"><span data-stu-id="74ba1-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="74ba1-127">Para publicar una propiedad definida por el usuario después de utilizar **SetPrinterDataEx** para agregar o cambiar un valor, llame a [**SetPrinter**](setprinter.md) con *LEVEL* = 7 y con el miembro **dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) establecido en **DSPRINT_UPDATE**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="74ba1-128">Puede especificar otras claves para almacenar los datos de configuración que no son de DS.</span><span class="sxs-lookup"><span data-stu-id="74ba1-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="74ba1-129">Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso que tenga una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="74ba1-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="74ba1-130">Si *hPrinter* es un identificador de una impresora y *pKeyName* es **null** o una cadena vacía, **SetPrinterDataEx** devuelve **ERROR_INVALID_PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="74ba1-131">Si *hPrinter* es un identificador de un servidor de impresión, *pKeyName* se omite.</span><span class="sxs-lookup"><span data-stu-id="74ba1-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="74ba1-132">No utilice **SPLDS_SPOOLER_KEY**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="74ba1-133">Para cambiar las propiedades de la impresora del administrador de trabajos de impresión, use [**SetPrinter**](setprinter.md) con *LEVEL* = 2.</span><span class="sxs-lookup"><span data-stu-id="74ba1-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="74ba1-134">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-135">Puntero a una cadena terminada en null que identifica los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="74ba1-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="74ba1-136">En el caso de las impresoras, esta cadena especifica el nombre de un valor en la clave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="74ba1-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="74ba1-137">En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="74ba1-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="74ba1-138">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-139">Código que indica el tipo de datos al que apunta el parámetro *pdata* .</span><span class="sxs-lookup"><span data-stu-id="74ba1-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="74ba1-140">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="74ba1-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="74ba1-141">Si *pKeyName* especifica una de las claves de servicio de directorio predefinidas, el *tipo* debe ser **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** o **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="74ba1-142">Si se utiliza **REG_BINARY** , *cbData* debe ser igual a 1 y el servicio de directorio trata los datos como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="74ba1-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="74ba1-143">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-144">Un puntero a un búfer que contiene los datos de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ba1-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="74ba1-145">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74ba1-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ba1-146">Tamaño, en bytes, de la matriz.</span><span class="sxs-lookup"><span data-stu-id="74ba1-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ba1-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74ba1-147">Return value</span></span>

<span data-ttu-id="74ba1-148">Si la función se ejecuta correctamente, el valor devuelto es **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="74ba1-149">Si se produce un error en la función, el valor devuelto es un valor de error.</span><span class="sxs-lookup"><span data-stu-id="74ba1-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74ba1-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74ba1-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74ba1-151">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="74ba1-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="74ba1-152">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74ba1-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="74ba1-153">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="74ba1-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="74ba1-154">Para recuperar los datos de configuración existentes de una impresora o cola de impresión, llame a la función [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="74ba1-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="74ba1-155">Llamar a **SetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData" es equivalente a llamar a la función [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="74ba1-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="74ba1-156">Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="74ba1-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="74ba1-157">Value</span><span class="sxs-lookup"><span data-stu-id="74ba1-157">Value</span></span>                                                               | <span data-ttu-id="74ba1-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74ba1-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ba1-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="74ba1-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="74ba1-160">Windows XP con Service Pack 2 (SP2) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="74ba1-161">Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="74ba1-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="74ba1-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="74ba1-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="74ba1-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="74ba1-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="74ba1-166">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="74ba1-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="74ba1-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="74ba1-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="74ba1-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="74ba1-170">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="74ba1-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="74ba1-172">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="74ba1-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="74ba1-174">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="74ba1-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="74ba1-176">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="74ba1-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="74ba1-178">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="74ba1-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="74ba1-180">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="74ba1-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="74ba1-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="74ba1-182">Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.</span><span class="sxs-lookup"><span data-stu-id="74ba1-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="74ba1-183">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="74ba1-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="74ba1-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="74ba1-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="74ba1-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="74ba1-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="74ba1-187">Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74ba1-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="74ba1-188">Al pasar uno de los siguientes valores predefinidos como *pValueName* , se establece el comportamiento de impresión del grupo cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="74ba1-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="74ba1-189">Value</span><span class="sxs-lookup"><span data-stu-id="74ba1-189">Value</span></span>                                       | <span data-ttu-id="74ba1-190">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74ba1-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ba1-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="74ba1-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="74ba1-192">El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="74ba1-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="74ba1-193">Esta configuración se usa con **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span><span class="sxs-lookup"><span data-stu-id="74ba1-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="74ba1-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="74ba1-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="74ba1-195">Un valor distinto de cero en *pdata* indica que **SPLREG_RESTART_JOB_ON_POOL_ERROR** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="74ba1-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="74ba1-196">La hora especificada en **SPLREG_RESTART_JOB_ON_POOL_ERROR** es un tiempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="74ba1-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="74ba1-197">La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:</span><span class="sxs-lookup"><span data-stu-id="74ba1-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="74ba1-198">**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**</span><span class="sxs-lookup"><span data-stu-id="74ba1-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="74ba1-199">Llame a la función [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para establecer estos valores.</span><span class="sxs-lookup"><span data-stu-id="74ba1-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="74ba1-200">Configuración del monitor de Puerto</span><span class="sxs-lookup"><span data-stu-id="74ba1-200">Port monitor setting</span></span>     | <span data-ttu-id="74ba1-201">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74ba1-201">Data type</span></span>      | <span data-ttu-id="74ba1-202">Significado</span><span class="sxs-lookup"><span data-stu-id="74ba1-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ba1-203">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="74ba1-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="74ba1-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="74ba1-204">**REG_DWORD**</span></span> | <span data-ttu-id="74ba1-205">Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="74ba1-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="74ba1-206">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="74ba1-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="74ba1-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="74ba1-207">**REG_DWORD**</span></span> | <span data-ttu-id="74ba1-208">Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="74ba1-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="74ba1-209">Para asegurarse de que la cola de impresión redirige los trabajos a la siguiente impresora disponible en el grupo (cuando el trabajo de impresión no se imprime en el tiempo establecido), el monitor de puerto debe admitir SNMP y los puertos de red del grupo deben estar configurados como "estado SNMP habilitado".</span><span class="sxs-lookup"><span data-stu-id="74ba1-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="74ba1-210">El monitor de puerto que admite SNMP es el monitor de puerto TCP/IP estándar.</span><span class="sxs-lookup"><span data-stu-id="74ba1-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="74ba1-211">En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74ba1-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="74ba1-212">La representación del lado cliente de los trabajos de impresión se puede configurar estableciendo *pKeyName* en "PrinterDriverData" y *pValueName* en el valor de configuración de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="74ba1-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="74ba1-213">Configuración</span><span class="sxs-lookup"><span data-stu-id="74ba1-213">Setting</span></span>                      | <span data-ttu-id="74ba1-214">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="74ba1-214">Data type</span></span>      | <span data-ttu-id="74ba1-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="74ba1-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ba1-216">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="74ba1-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="74ba1-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="74ba1-217">**REG_DWORD**</span></span> | <span data-ttu-id="74ba1-218">Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ba1-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="74ba1-219">Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ba1-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="74ba1-220">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="74ba1-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="74ba1-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="74ba1-221">**REG_DWORD**</span></span> | <span data-ttu-id="74ba1-222">Un valor de 0, o si este valor no está presente en el registro, hará que los trabajos de impresión se representen en el cliente.</span><span class="sxs-lookup"><span data-stu-id="74ba1-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="74ba1-223">Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor.</span><span class="sxs-lookup"><span data-stu-id="74ba1-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="74ba1-224">Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="74ba1-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="74ba1-225">Un valor de 1 representará los trabajos de impresión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="74ba1-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="74ba1-226">Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="74ba1-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="74ba1-227">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ba1-227">Requirements</span></span>



| <span data-ttu-id="74ba1-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ba1-228">Requirement</span></span> | <span data-ttu-id="74ba1-229">Value</span><span class="sxs-lookup"><span data-stu-id="74ba1-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ba1-230">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ba1-230">Minimum supported client</span></span><br/> | <span data-ttu-id="74ba1-231">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="74ba1-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74ba1-232">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ba1-232">Minimum supported server</span></span><br/> | <span data-ttu-id="74ba1-233">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74ba1-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74ba1-234">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74ba1-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ba1-235"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74ba1-236">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74ba1-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="74ba1-237"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="74ba1-238">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74ba1-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ba1-239"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="74ba1-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="74ba1-240">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="74ba1-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74ba1-241">**SetPrinterDataExW** (Unicode) y **SetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74ba1-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="74ba1-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="74ba1-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ba1-243">Impresión</span><span class="sxs-lookup"><span data-stu-id="74ba1-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74ba1-244">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="74ba1-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="74ba1-245">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="74ba1-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="74ba1-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="74ba1-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="74ba1-247">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="74ba1-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="74ba1-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="74ba1-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

