---
description: La función GetPrinterDriver recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, GetPrinterDriver lo instala.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Función GetPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707231"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="a38a3-104">GetPrinterDriver función)</span><span class="sxs-lookup"><span data-stu-id="a38a3-104">GetPrinterDriver function</span></span>

<span data-ttu-id="a38a3-105">La función **GetPrinterDriver** recupera los datos del controlador de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="a38a3-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="a38a3-106">Si el controlador no está instalado en el equipo local, **GetPrinterDriver** lo instala.</span><span class="sxs-lookup"><span data-stu-id="a38a3-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a38a3-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a38a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a38a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38a3-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-110">Identificador de la impresora para la que deben recuperarse los datos del controlador.</span><span class="sxs-lookup"><span data-stu-id="a38a3-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="a38a3-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="a38a3-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a38a3-112">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-113">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a38a3-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a38a3-114">Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="a38a3-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a38a3-115">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-116">Estructura del controlador de impresora devuelta en el búfer de *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="a38a3-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="a38a3-117">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a38a3-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a38a3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a38a3-118">Value</span></span>                                                                                                | <span data-ttu-id="a38a3-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a38a3-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a38a3-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-121">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a38a3-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="a38a3-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-123">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a38a3-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="a38a3-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-125">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="a38a3-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="a38a3-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-127">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="a38a3-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="a38a3-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-129">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="a38a3-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="a38a3-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-131">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="a38a3-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="a38a3-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="a38a3-133">**Información del controlador \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="a38a3-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="a38a3-134">*pDriverInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-135">Un puntero a un búfer que recibe una estructura que contiene información sobre el controlador, tal como se especifica en Level.</span><span class="sxs-lookup"><span data-stu-id="a38a3-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="a38a3-136">El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="a38a3-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="a38a3-137">Para determinar el tamaño de búfer necesario, llame a **GetPrinterDriver** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="a38a3-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="a38a3-138">**GetPrinterDriver** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="a38a3-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="a38a3-139">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-140">Tamaño, en bytes, de la matriz en la que apunta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="a38a3-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="a38a3-141">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-142">Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="a38a3-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38a3-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a38a3-143">Return value</span></span>

<span data-ttu-id="a38a3-144">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a38a3-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a38a3-145">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a38a3-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="a38a3-146">Para un controlador no existente, la función devuelve el ERROR \_ \_ controlador de impresora desconocido \_ .</span><span class="sxs-lookup"><span data-stu-id="a38a3-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38a3-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a38a3-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a38a3-148">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a38a3-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a38a3-149">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a38a3-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a38a3-150">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="a38a3-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a38a3-151">Las estructuras [**driver \_ info \_ 2**](driver-info-2.md), info. de controlador [**\_ \_ 3**](driver-info-3.md), info. de controlador [**\_ \_ 4**](driver-info-4.md), info. de controlador [**\_ \_ 5**](driver-info-5.md)y [**driver \_ info \_ 6**](driver-info-6.md) contienen el nombre de archivo o la ruta de acceso completa y el nombre de archivo del controlador de impresora en el miembro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="a38a3-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="a38a3-152">Una aplicación puede usar la ruta de acceso y el nombre de archivo para cargar un controlador de impresora mediante una llamada a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y proporcionando la ruta de acceso y el nombre de archivo como argumento único.</span><span class="sxs-lookup"><span data-stu-id="a38a3-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38a3-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a38a3-153">Requirements</span></span>



| <span data-ttu-id="a38a3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="a38a3-154">Requirement</span></span> | <span data-ttu-id="a38a3-155">Value</span><span class="sxs-lookup"><span data-stu-id="a38a3-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38a3-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a38a3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a38a3-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a38a3-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a38a3-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a38a3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a38a3-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a38a3-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a38a3-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a38a3-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="a38a3-161"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a38a3-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a38a3-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="a38a3-163"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a38a3-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a38a3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a38a3-165"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a38a3-166">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a38a3-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a38a3-167">**GetPrinterDriverW** (Unicode) y **GetPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a38a3-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="a38a3-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="a38a3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38a3-169">Impresión</span><span class="sxs-lookup"><span data-stu-id="a38a3-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a38a3-170">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a38a3-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a38a3-171">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a38a3-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="a38a3-172">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a38a3-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="a38a3-173">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a38a3-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="a38a3-174">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="a38a3-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="a38a3-175">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="a38a3-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="a38a3-176">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="a38a3-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="a38a3-177">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="a38a3-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="a38a3-178">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="a38a3-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="a38a3-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a38a3-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

