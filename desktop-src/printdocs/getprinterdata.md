---
description: La función GetPrinterData recupera los datos de configuración para la impresora o el servidor de impresión especificado.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Función GetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706705"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="f8949-103">GetPrinterData función)</span><span class="sxs-lookup"><span data-stu-id="f8949-103">GetPrinterData function</span></span>

<span data-ttu-id="f8949-104">La función **GetPrinterData** recupera los datos de configuración para la impresora o el servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="f8949-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="f8949-105">En Windows 2000 y versiones posteriores de Windows, llamar a **GetPrinterData** es equivalente a llamar a [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con el parámetro *pKeyName* establecido en "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="f8949-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="f8949-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8949-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="f8949-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8949-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8949-108">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8949-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-109">Identificador de la impresora o del servidor de impresión para el que la función recupera datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="f8949-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="f8949-110">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f8949-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f8949-111">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8949-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-112">Puntero a una cadena terminada en null que identifica los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f8949-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="f8949-113">En el caso de las impresoras, esta cadena es el nombre de un valor del registro en la clave "PrinterDriverData" de la impresora del registro.</span><span class="sxs-lookup"><span data-stu-id="f8949-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="f8949-114">En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="f8949-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="f8949-115">*pType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8949-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-116">Puntero a una variable que recibe un valor que indica el tipo de datos recuperados en *pdata*.</span><span class="sxs-lookup"><span data-stu-id="f8949-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="f8949-117">La función devuelve el tipo especificado en la llamada a [**SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) que almacena los datos.</span><span class="sxs-lookup"><span data-stu-id="f8949-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="f8949-118">Establezca este parámetro en **null** si no necesita el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f8949-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="f8949-119">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8949-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-120">Un puntero a un búfer que recibe los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="f8949-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="f8949-121">*nSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8949-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-122">Tamaño, en bytes, del búfer al que apunta *pdata* .</span><span class="sxs-lookup"><span data-stu-id="f8949-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="f8949-123">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8949-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8949-124">Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="f8949-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="f8949-125">Si el tamaño de búfer especificado por *nSize* es demasiado pequeño, la función devuelve un **error \_ más \_ datos** y *pcbNeeded* indica el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="f8949-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8949-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8949-126">Return value</span></span>

<span data-ttu-id="f8949-127">Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="f8949-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="f8949-128">Si se produce un error en la función, el valor devuelto es un valor de error.</span><span class="sxs-lookup"><span data-stu-id="f8949-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8949-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8949-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8949-130">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f8949-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f8949-131">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8949-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f8949-132">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f8949-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f8949-133">**GetPrinterData** recupera los datos de configuración de la impresora que se establecieron con la función [**SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f8949-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="f8949-134">**GetPrinterData** puede desencadenar una llamada de Windows a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), que puede escribir en el registro.</span><span class="sxs-lookup"><span data-stu-id="f8949-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="f8949-135">Si lo hace, pueden producirse efectos secundarios, como desencadenar una actualización o actualizar el ID. de evento 20 de la impresora en el cliente, si la impresora se comparte en una red.</span><span class="sxs-lookup"><span data-stu-id="f8949-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="f8949-136">Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="f8949-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="f8949-137">Value</span><span class="sxs-lookup"><span data-stu-id="f8949-137">Value</span></span>                                                               | <span data-ttu-id="f8949-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8949-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8949-139">**SPLREG \_ permitir el \_ usuario \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="f8949-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="f8949-140">Windows XP con Service Pack 2 (SP2) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="f8949-141">Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="f8949-142">**arquitectura de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-143">**SPLREG \_ beep \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="f8949-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-144">**\_Directorio de \_ cola de impresión predeterminado de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-145">**nombre de la \_ máquina DNS SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-146">**SPLREG \_ DS \_ present**</span><span class="sxs-lookup"><span data-stu-id="f8949-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="f8949-147">Si la devolución es correcta, *pdata* contiene 0x0001 si el equipo está en un dominio de DS, de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f8949-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="f8949-148">**SPLREG \_ DS \_ present \_ for \_ User**</span><span class="sxs-lookup"><span data-stu-id="f8949-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="f8949-149">Si la devolución es correcta, *pdata* contiene 0x0001 si el usuario ha iniciado sesión en un dominio de DS, de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f8949-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="f8949-150">**\_registro de eventos de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-151">**\_versión principal de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-152">**\_versión secundaria de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-153">**\_ \_ menú emergente de SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="f8949-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="f8949-154">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="f8949-155">**SPLREG \_ net \_ popup \_ en el \_ equipo**</span><span class="sxs-lookup"><span data-stu-id="f8949-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="f8949-156">Si la devolución es correcta, *pdata* contiene 1 si se deben enviar notificaciones de trabajo al equipo cliente, o 0 si las notificaciones de trabajo se van a enviar al usuario.</span><span class="sxs-lookup"><span data-stu-id="f8949-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="f8949-157">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="f8949-158">**\_versión de SO SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="f8949-159">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-160">**SPLREG \_ os \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="f8949-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-161">**\_ \_ \_ valor predeterminado de prioridad de subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-162">**\_prioridad de \_ subproceso de Puerto SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-163">**SPLREG \_ \_ grupos de \_ aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="f8949-164">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-165">**SPLREG \_ tiempo de aislamiento de controladores de impresión \_ antes de \_ \_ \_ \_ reciclar**</span><span class="sxs-lookup"><span data-stu-id="f8949-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="f8949-166">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-167">**SPLREG de \_ aislamiento de controlador de impresión máximo de \_ \_ \_ \_ objetos antes del \_ \_ reciclaje**</span><span class="sxs-lookup"><span data-stu-id="f8949-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="f8949-168">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-169">**\_tiempo de \_ \_ espera de \_ inactividad de controlador de impresión SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="f8949-170">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-171">**SPLREG \_ \_ Directiva de \_ ejecución de aislamiento de controladores de \_ impresión \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="f8949-172">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-173">**SPLREG \_ \_ Directiva de \_ \_ invalidación de aislamiento de controladores de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="f8949-174">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f8949-175">**\_fax remoto \_ SPLREG**</span><span class="sxs-lookup"><span data-stu-id="f8949-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="f8949-176">Si la devolución es correcta, *pdata* contiene 0x0001 si el servicio de fax admite clientes remotos; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f8949-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="f8949-177">**\_elemento emergente de reintento de SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="f8949-178">Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.</span><span class="sxs-lookup"><span data-stu-id="f8949-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="f8949-179">No se admite en Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="f8949-180">**\_prioridad de \_ subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-181">**\_ \_ \_ prioridad predeterminada del subproceso de SPLREG Scheduler \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f8949-182">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="f8949-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="f8949-183">Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="f8949-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="f8949-184">Los siguientes valores de *pValueName* indican el comportamiento de impresión del grupo cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f8949-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="f8949-185">Value</span><span class="sxs-lookup"><span data-stu-id="f8949-185">Value</span></span>                                       | <span data-ttu-id="f8949-186">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8949-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8949-187">**\_ \_ error al reiniciar el trabajo \_ de SPLREG en el \_ grupo \_**</span><span class="sxs-lookup"><span data-stu-id="f8949-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="f8949-188">El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="f8949-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="f8949-189">Esta configuración se usa con **el \_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="f8949-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="f8949-190">**\_ \_ trabajo de reinicio de SPLREG \_ en \_ grupo \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="f8949-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="f8949-191">Un valor distinto de cero en *pdata* indica que está habilitado el **\_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_** .</span><span class="sxs-lookup"><span data-stu-id="f8949-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="f8949-192">La hora especificada en **el \_ trabajo de reinicio de SPLREG \_ en el \_ \_ \_ error de grupo** es un tiempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="f8949-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="f8949-193">La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:</span><span class="sxs-lookup"><span data-stu-id="f8949-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="f8949-194">**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**</span><span class="sxs-lookup"><span data-stu-id="f8949-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="f8949-195">Llame a la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar estos valores.</span><span class="sxs-lookup"><span data-stu-id="f8949-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="f8949-196">Configuración del monitor de Puerto</span><span class="sxs-lookup"><span data-stu-id="f8949-196">Port monitor setting</span></span>     | <span data-ttu-id="f8949-197">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f8949-197">Data type</span></span>      | <span data-ttu-id="f8949-198">Significado</span><span class="sxs-lookup"><span data-stu-id="f8949-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8949-199">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8949-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="f8949-200">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f8949-200">**REG\_DWORD**</span></span> | <span data-ttu-id="f8949-201">Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="f8949-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="f8949-202">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="f8949-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="f8949-203">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f8949-203">**REG\_DWORD**</span></span> | <span data-ttu-id="f8949-204">Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="f8949-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="f8949-205">En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f8949-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="f8949-206">Los valores siguientes configuran la representación del lado cliente de un trabajo de impresión y se pueden leer si establece los siguientes valores en *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="f8949-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="f8949-207">Configuración</span><span class="sxs-lookup"><span data-stu-id="f8949-207">Setting</span></span>                      | <span data-ttu-id="f8949-208">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f8949-208">Data type</span></span>      | <span data-ttu-id="f8949-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8949-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8949-210">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="f8949-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="f8949-211">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f8949-211">**REG\_DWORD**</span></span> | <span data-ttu-id="f8949-212">Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="f8949-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="f8949-213">Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="f8949-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="f8949-214">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="f8949-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="f8949-215">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f8949-215">**REG\_DWORD**</span></span> | <span data-ttu-id="f8949-216">Un valor de 0, o si este valor no está presente en el registro, hará que los trabajos de impresión se representen en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f8949-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="f8949-217">Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f8949-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="f8949-218">Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f8949-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="f8949-219">Un valor de 1 representará los trabajos de impresión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f8949-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="f8949-220">Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f8949-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f8949-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8949-221">Requirements</span></span>



| <span data-ttu-id="f8949-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8949-222">Requirement</span></span> | <span data-ttu-id="f8949-223">Value</span><span class="sxs-lookup"><span data-stu-id="f8949-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8949-224">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8949-224">Minimum supported client</span></span><br/> | <span data-ttu-id="f8949-225">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f8949-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8949-226">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8949-226">Minimum supported server</span></span><br/> | <span data-ttu-id="f8949-227">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8949-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8949-228">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8949-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8949-229"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8949-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8949-230">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8949-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8949-231"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8949-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f8949-232">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8949-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8949-233"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f8949-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f8949-234">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f8949-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8949-235">**GetPrinterDataW** (Unicode) y **GetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8949-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="f8949-236">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8949-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8949-237">Impresión</span><span class="sxs-lookup"><span data-stu-id="f8949-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8949-238">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f8949-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f8949-239">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f8949-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f8949-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f8949-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f8949-241">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f8949-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f8949-242">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="f8949-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="f8949-243">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f8949-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f8949-244">**PRINTPROCESSOR \_ Cap \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f8949-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

