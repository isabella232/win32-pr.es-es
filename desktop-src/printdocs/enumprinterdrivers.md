---
description: La función EnumPrinterDrivers enumera los controladores de impresora instalados en un servidor de impresión especificado.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Función EnumPrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813550"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="4fcbf-103">EnumPrinterDrivers función)</span><span class="sxs-lookup"><span data-stu-id="4fcbf-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="4fcbf-104">La función **EnumPrinterDrivers** enumera los controladores de impresora instalados en un servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcbf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fcbf-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="4fcbf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fcbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fcbf-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se enumeran los controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="4fcbf-109">Si *pName* es **null**, la función enumera los controladores de la impresora local.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="4fcbf-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-111">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64, Windows x64 o Windows NT R4000).</span><span class="sxs-lookup"><span data-stu-id="4fcbf-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="4fcbf-112">Si este parámetro es **null**, la función utiliza el entorno actual del llamador/cliente (no del servidor de destino).</span><span class="sxs-lookup"><span data-stu-id="4fcbf-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="4fcbf-113">Si la cadena *pEnvironment* especifica "All", **EnumPrinterDrivers** enumera los controladores de impresora para todas las plataformas instaladas en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="4fcbf-114">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-115">Tipo de estructura de información devuelto en el búfer de *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="4fcbf-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="4fcbf-116">Puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-116">It can be one of the following.</span></span>



| <span data-ttu-id="4fcbf-117">Value</span><span class="sxs-lookup"><span data-stu-id="4fcbf-117">Value</span></span>                                                                                                | <span data-ttu-id="4fcbf-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4fcbf-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4fcbf-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-120">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="4fcbf-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-122">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="4fcbf-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-124">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="4fcbf-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-126">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="4fcbf-127"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-128">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="4fcbf-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-130">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="4fcbf-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="4fcbf-132">**Información del controlador \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="4fcbf-133">*pDriverInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-134">Un puntero a un búfer que recibe una matriz de estructuras de información del controlador \_ \_ \* , tal como se especifica en *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="4fcbf-135">Cada estructura contiene datos que describen un controlador de impresora disponible.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="4fcbf-136">El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y cualquier cadena u otros datos a los que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="4fcbf-137">Para determinar el tamaño de búfer necesario, llame a **EnumPrinterDrivers** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="4fcbf-138">**EnumPrinterDrivers** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="4fcbf-139">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-140">Tamaño, en bytes, del búfer al que apunta *pDriverInfo*</span><span class="sxs-lookup"><span data-stu-id="4fcbf-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="4fcbf-141">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-142">Un puntero a una variable que recibe el número de bytes copiados en el búfer de *pDriverInfo* si la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="4fcbf-143">Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="4fcbf-144">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fcbf-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fcbf-145">Puntero a una variable que recibe el número de estructuras devueltas en el búfer de *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="4fcbf-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="4fcbf-146">Es el número de controladores de impresora instalados en el servidor de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fcbf-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fcbf-147">Return value</span></span>

<span data-ttu-id="4fcbf-148">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4fcbf-149">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fcbf-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fcbf-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4fcbf-151">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4fcbf-152">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4fcbf-153">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4fcbf-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fcbf-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fcbf-154">Requirements</span></span>



| <span data-ttu-id="4fcbf-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fcbf-155">Requirement</span></span> | <span data-ttu-id="4fcbf-156">Value</span><span class="sxs-lookup"><span data-stu-id="4fcbf-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcbf-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fcbf-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4fcbf-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4fcbf-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4fcbf-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fcbf-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4fcbf-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fcbf-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4fcbf-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fcbf-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fcbf-162"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4fcbf-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fcbf-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fcbf-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4fcbf-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fcbf-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fcbf-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4fcbf-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4fcbf-167">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4fcbf-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4fcbf-168">**EnumPrinterDriversW** (Unicode) y **EnumPrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4fcbf-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4fcbf-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fcbf-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcbf-170">Impresión</span><span class="sxs-lookup"><span data-stu-id="4fcbf-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-171">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4fcbf-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-173">**Información del controlador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-174">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-175">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-176">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-177">**Información del controlador \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-178">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="4fcbf-179">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4fcbf-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

