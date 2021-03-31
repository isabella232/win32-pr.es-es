---
description: La función GetPrinterDataEx recupera los datos de configuración para la impresora o el servidor de impresión especificado.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Función GetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817907"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="8cbb8-103">GetPrinterDataEx función)</span><span class="sxs-lookup"><span data-stu-id="8cbb8-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="8cbb8-104">La función **GetPrinterDataEx** recupera los datos de configuración para la impresora o el servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="8cbb8-105">**GetPrinterDataEx** puede recuperar los valores que almacena la función [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="8cbb8-106">Además, **GetPrinterDataEx** puede recuperar los valores que la función [**SetPrinterDataEx**](setprinterdataex.md) almacenó en una clave especificada.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbb8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cbb8-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8cbb8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cbb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cbb8-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-110">Identificador de la impresora o del servidor de impresión para el que la función recupera datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="8cbb8-111">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-112">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-113">Puntero a una cadena terminada en null que especifica la clave que contiene el valor que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="8cbb8-114">Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso que tenga una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="8cbb8-115">Si *hPrinter* es un identificador de una impresora y *pKeyName* es **null** o una cadena vacía, **GetPrinterDataEx** devuelve **un \_ \_ parámetro de error no válido**.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="8cbb8-116">Si *hPrinter* es un identificador de un servidor de impresión, *pKeyName* se omite.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-117">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-118">Puntero a una cadena terminada en null que identifica los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="8cbb8-119">En el caso de las impresoras, esta cadena especifica el nombre de un valor en la clave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="8cbb8-120">En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-121">*pType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-122">Puntero a una variable que recibe el tipo de datos almacenado en el valor.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="8cbb8-123">La función devuelve el tipo especificado en la llamada a [**SetPrinterDataEx**](setprinterdataex.md) cuando se almacenaron los datos.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="8cbb8-124">Este parámetro puede ser **null** si no se necesita la información.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="8cbb8-125">**GetPrinterDataEx** pasa *PType* como parámetro *lpdwType* de una llamada de función [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-126">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-127">Un puntero a un búfer que recibe los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-128">*nSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-129">Tamaño, en bytes, del búfer al que apunta *pdata*.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="8cbb8-130">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8cbb8-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbb8-131">Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="8cbb8-132">Si el tamaño de búfer especificado por *nSize* es demasiado pequeño, la función devuelve un **error \_ más \_ datos** y *pcbNeeded* indica el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cbb8-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cbb8-133">Return value</span></span>

<span data-ttu-id="8cbb8-134">Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="8cbb8-135">Si se produce un error en la función, el valor devuelto es un valor de error.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cbb8-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cbb8-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8cbb8-137">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8cbb8-138">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8cbb8-139">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8cbb8-140">**GetPrinterDataEx** recupera los datos de configuración de la impresora que se establecieron mediante las funciones [**SetPrinterDataEx**](setprinterdataex.md) y [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="8cbb8-141">Llamar a **GetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData" es equivalente a llamar a la función [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="8cbb8-142">Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="8cbb8-143">Value</span><span class="sxs-lookup"><span data-stu-id="8cbb8-143">Value</span></span>                                                               | <span data-ttu-id="8cbb8-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cbb8-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbb8-145">**SPLREG \_ permitir el \_ usuario \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="8cbb8-146">Windows XP con Service Pack 2 (SP2) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="8cbb8-147">Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="8cbb8-148">**arquitectura de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-149">**SPLREG \_ beep \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-150">**\_Directorio de \_ cola de impresión predeterminado de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-151">**nombre de la \_ máquina DNS SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-152">**SPLREG \_ DS \_ present**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="8cbb8-153">Si la devolución es correcta, *pdata* contiene 0x0001 si el equipo está en un dominio de DS, de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="8cbb8-154">**SPLREG \_ DS \_ present \_ for \_ User**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="8cbb8-155">Si la devolución es correcta, *pdata* contiene 0x0001 si el usuario ha iniciado sesión en un dominio de DS, de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="8cbb8-156">**\_registro de eventos de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-157">**\_versión principal de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-158">**\_versión secundaria de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-159">**\_ \_ menú emergente de SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="8cbb8-160">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="8cbb8-161">**SPLREG \_ net \_ popup \_ en el \_ equipo**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="8cbb8-162">Si la devolución es correcta, *pdata* contiene 1 si se deben enviar notificaciones de trabajo al equipo cliente, o 0 si las notificaciones de trabajo se van a enviar al usuario.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="8cbb8-163">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="8cbb8-164">**\_versión de SO SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="8cbb8-165">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-166">**SPLREG \_ os \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-167">**\_ \_ \_ valor predeterminado de prioridad de subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-168">**\_prioridad de \_ subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-169">**SPLREG \_ \_ grupos de \_ aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="8cbb8-170">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-171">**SPLREG \_ tiempo de aislamiento de controladores de impresión \_ antes de \_ \_ \_ \_ reciclar**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="8cbb8-172">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-173">**SPLREG de \_ aislamiento de controlador de impresión máximo de \_ \_ \_ \_ objetos antes del \_ \_ reciclaje**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="8cbb8-174">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-175">**\_tiempo de \_ \_ espera de \_ inactividad de controlador de impresión SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="8cbb8-176">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-177">**SPLREG \_ \_ Directiva de \_ ejecución de aislamiento de controladores de \_ impresión \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="8cbb8-178">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-179">**SPLREG \_ \_ Directiva de \_ \_ invalidación de aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="8cbb8-180">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="8cbb8-181">**\_fax remoto \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="8cbb8-182">Si la devolución es correcta, *pdata* contiene 0x0001 si el servicio de fax admite clientes remotos; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="8cbb8-183">**\_elemento emergente de reintento de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="8cbb8-184">Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="8cbb8-185">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="8cbb8-186">**\_prioridad de \_ subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-187">**\_ \_ \_ prioridad predeterminada del subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="8cbb8-188">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="8cbb8-189">Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8cbb8-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="8cbb8-190">Los siguientes valores de *pValueName* indican el comportamiento de impresión del grupo cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="8cbb8-191">Value</span><span class="sxs-lookup"><span data-stu-id="8cbb8-191">Value</span></span>                                       | <span data-ttu-id="8cbb8-192">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cbb8-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbb8-193">**\_ \_ error al reiniciar el trabajo \_ de SPLREG en el \_ grupo \_**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="8cbb8-194">El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="8cbb8-195">Esta configuración se usa con **el \_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="8cbb8-196">**\_ \_ trabajo de reinicio de SPLREG \_ en \_ grupo \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="8cbb8-197">Un valor distinto de cero en *pdata* indica que está habilitado el **\_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_** .</span><span class="sxs-lookup"><span data-stu-id="8cbb8-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="8cbb8-198">La hora especificada en **el \_ trabajo de reinicio de SPLREG \_ en el \_ \_ \_ error de grupo** es un tiempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="8cbb8-199">La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:</span><span class="sxs-lookup"><span data-stu-id="8cbb8-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="8cbb8-200">**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="8cbb8-201">Llame a la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar estos valores.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="8cbb8-202">Configuración del monitor de Puerto</span><span class="sxs-lookup"><span data-stu-id="8cbb8-202">Port monitor setting</span></span>     | <span data-ttu-id="8cbb8-203">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8cbb8-203">Data type</span></span>      | <span data-ttu-id="8cbb8-204">Significado</span><span class="sxs-lookup"><span data-stu-id="8cbb8-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbb8-205">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="8cbb8-206">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-206">**REG\_DWORD**</span></span> | <span data-ttu-id="8cbb8-207">Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="8cbb8-208">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="8cbb8-209">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-209">**REG\_DWORD**</span></span> | <span data-ttu-id="8cbb8-210">Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="8cbb8-211">Si *pKeyName* es una de las claves del servicio de directorio predefinido (DS) (vea [**SetPrinter**](setprinter.md)) y *pValueName* contiene una coma (","), la parte de *pValueName* antes de la coma es el nombre del valor y la parte de *pValueName* situada a la derecha de la coma es el OID de la propiedad de DS.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="8cbb8-212">Se crea una subclave denominada OID y se especifica un nuevo valor compuesto por el nombre de valor y el OID en la clave OID.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="8cbb8-213">[**SetPrinterDataEx**](setprinterdataex.md) también agrega el nombre del valor y los datos en la clave de DS.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="8cbb8-214">En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="8cbb8-215">La configuración de la representación del lado cliente para una impresora se puede leer estableciendo *pKeyName* en "PrinterDriverData" y *pValueName* en el valor de configuración de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="8cbb8-216">Configuración</span><span class="sxs-lookup"><span data-stu-id="8cbb8-216">Setting</span></span>                      | <span data-ttu-id="8cbb8-217">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8cbb8-217">Data type</span></span>      | <span data-ttu-id="8cbb8-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cbb8-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbb8-219">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="8cbb8-220">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-220">**REG\_DWORD**</span></span> | <span data-ttu-id="8cbb8-221">Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="8cbb8-222">Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="8cbb8-223">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="8cbb8-224">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-224">**REG\_DWORD**</span></span> | <span data-ttu-id="8cbb8-225">Un valor de 0, o si este valor no está presente en el registro, hará que los trabajos de impresión se representen en el cliente.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="8cbb8-226">Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="8cbb8-227">Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="8cbb8-228">Un valor de 1 representará los trabajos de impresión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="8cbb8-229">Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8cbb8-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8cbb8-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cbb8-230">Requirements</span></span>



| <span data-ttu-id="8cbb8-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cbb8-231">Requirement</span></span> | <span data-ttu-id="8cbb8-232">Value</span><span class="sxs-lookup"><span data-stu-id="8cbb8-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbb8-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cbb8-233">Minimum supported client</span></span><br/> | <span data-ttu-id="8cbb8-234">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8cbb8-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8cbb8-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cbb8-235">Minimum supported server</span></span><br/> | <span data-ttu-id="8cbb8-236">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cbb8-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8cbb8-237">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cbb8-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cbb8-238"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cbb8-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8cbb8-239">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cbb8-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="8cbb8-240"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cbb8-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8cbb8-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8cbb8-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cbb8-242"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8cbb8-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8cbb8-243">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8cbb8-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8cbb8-244">**GetPrinterDataExW** (Unicode) y **GetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8cbb8-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="8cbb8-245">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cbb8-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbb8-246">Impresión</span><span class="sxs-lookup"><span data-stu-id="8cbb8-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8cbb8-247">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8cbb8-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8cbb8-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="8cbb8-249">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="8cbb8-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

