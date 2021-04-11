---
description: La función GetPrinterDriver2 recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, GetPrinterDriver2 lo instala y muestra cualquier interfaz de usuario en la ventana especificada.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Función GetPrinterDriver2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279032"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="0e03a-104">GetPrinterDriver2 función)</span><span class="sxs-lookup"><span data-stu-id="0e03a-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="0e03a-105">La función **GetPrinterDriver2** recupera los datos del controlador de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="0e03a-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="0e03a-106">Si el controlador no está instalado en el equipo local, **GetPrinterDriver2** lo instala y muestra cualquier interfaz de usuario en la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="0e03a-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e03a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e03a-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="0e03a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e03a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e03a-109">*hWnd* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-110">Identificador de la ventana que se usará como ventana primaria de cualquier interfaz de usuario, como un cuadro de diálogo, que el controlador muestra durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0e03a-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="0e03a-111">Si el valor de este parámetro es **null**, la interfaz de usuario del controlador seguirá mostrándose al usuario durante la instalación, pero no tendrá una ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="0e03a-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="0e03a-112">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-113">Identificador de la impresora para la que deben recuperarse los datos del controlador.</span><span class="sxs-lookup"><span data-stu-id="0e03a-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="0e03a-114">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="0e03a-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="0e03a-115">*pEnvironment* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-116">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="0e03a-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="0e03a-117">Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="0e03a-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="0e03a-118">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-119">Estructura del controlador de impresora devuelta en el búfer de *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="0e03a-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="0e03a-120">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0e03a-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0e03a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0e03a-121">Value</span></span>                                                                                                | <span data-ttu-id="0e03a-122">Significado</span><span class="sxs-lookup"><span data-stu-id="0e03a-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="0e03a-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-124">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0e03a-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="0e03a-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-126">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0e03a-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="0e03a-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-128">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="0e03a-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="0e03a-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-130">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="0e03a-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="0e03a-131"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-132">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="0e03a-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="0e03a-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-134">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="0e03a-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="0e03a-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="0e03a-136">**Información del controlador \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="0e03a-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="0e03a-137">*pDriverInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-138">Un puntero a un búfer que recibe una estructura que contiene información sobre el controlador, tal como se especifica en *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="0e03a-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="0e03a-139">El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0e03a-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="0e03a-140">Para determinar el tamaño de búfer necesario, llame a **GetPrinterDriver2** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="0e03a-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="0e03a-141">**GetPrinterDriver2** produce un error, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="0e03a-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="0e03a-142">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-143">Tamaño, en bytes, de la matriz en la que apunta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="0e03a-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="0e03a-144">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e03a-145">Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="0e03a-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e03a-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e03a-146">Return value</span></span>

<span data-ttu-id="0e03a-147">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0e03a-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0e03a-148">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="0e03a-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="0e03a-149">Para obtener el estado de retorno, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0e03a-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e03a-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e03a-150">Remarks</span></span>

<span data-ttu-id="0e03a-151">Las [**estructuras \_ información \_**](driver-info-2.md)de controlador 2, información de [**controlador \_ \_ 3**](driver-info-3.md), [**información de controlador \_ \_ 4**](driver-info-4.md), [**información de controlador \_ \_ 5**](driver-info-5.md), [**información de controlador \_ \_ 6**](driver-info-6.md)e [**información de controlador \_ \_ 8**](driver-info-8.md) contienen el nombre de archivo o la ruta de acceso completa y el nombre de archivo del controlador de impresora en el miembro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="0e03a-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="0e03a-152">Una aplicación puede usar la ruta de acceso y el nombre de archivo para cargar un controlador de impresora mediante una llamada a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y proporcionando la ruta de acceso y el nombre de archivo como argumento único.</span><span class="sxs-lookup"><span data-stu-id="0e03a-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="0e03a-153">La versión ANSI de esta función, **GetPrinterDriver2A** no se admite y devuelve un **error \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="0e03a-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e03a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e03a-154">Requirements</span></span>



| <span data-ttu-id="0e03a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e03a-155">Requirement</span></span> | <span data-ttu-id="0e03a-156">Value</span><span class="sxs-lookup"><span data-stu-id="0e03a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e03a-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e03a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0e03a-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0e03a-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e03a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0e03a-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e03a-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e03a-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e03a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e03a-162"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e03a-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e03a-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e03a-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0e03a-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e03a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e03a-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0e03a-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0e03a-167">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0e03a-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e03a-168">**GetPrinterDriver2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="0e03a-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="0e03a-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e03a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e03a-170">Impresión</span><span class="sxs-lookup"><span data-stu-id="0e03a-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0e03a-171">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="0e03a-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0e03a-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="0e03a-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="0e03a-173">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0e03a-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="0e03a-174">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0e03a-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="0e03a-175">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="0e03a-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="0e03a-176">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="0e03a-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="0e03a-177">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="0e03a-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="0e03a-178">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="0e03a-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="0e03a-179">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="0e03a-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="0e03a-180">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="0e03a-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="0e03a-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e03a-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

