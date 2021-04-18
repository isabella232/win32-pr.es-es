---
description: La función GetPrinter recupera información sobre una impresora especificada.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Función GetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707169"
---
# <a name="getprinter-function"></a><span data-ttu-id="bb490-103">GetPrinter función)</span><span class="sxs-lookup"><span data-stu-id="bb490-103">GetPrinter function</span></span>

<span data-ttu-id="bb490-104">La función **GetPrinter** recupera información sobre una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="bb490-104">The **GetPrinter** function retrieves information about a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb490-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb490-105">Syntax</span></span>


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="bb490-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb490-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb490-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb490-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb490-108">Identificador de la impresora para la que la función recupera información.</span><span class="sxs-lookup"><span data-stu-id="bb490-108">A handle to the printer for which the function retrieves information.</span></span> <span data-ttu-id="bb490-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="bb490-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bb490-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb490-111">Nivel o tipo de estructura que la función almacena en el búfer al que apunta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="bb490-111">The level or type of structure that the function stores into the buffer pointed to by *pPrinter*.</span></span>

<span data-ttu-id="bb490-112">Este valor puede ser 1, 2, 3, 4, 5, 6, 7, 8 o 9.</span><span class="sxs-lookup"><span data-stu-id="bb490-112">This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.</span></span>

</dd> <dt>

<span data-ttu-id="bb490-113">*pPrinter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb490-113">*pPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb490-114">Puntero a un búfer que recibe una estructura que contiene información sobre la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="bb490-114">A pointer to a buffer that receives a structure containing information about the specified printer.</span></span> <span data-ttu-id="bb490-115">El búfer debe ser lo suficientemente grande como para recibir la estructura y las cadenas u otros datos a los que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="bb490-115">The buffer must be large enough to receive the structure and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="bb490-116">Si el búfer es demasiado pequeño, el parámetro *pcbNeeded* devuelve el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="bb490-116">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

<span data-ttu-id="bb490-117">El tipo de estructura viene determinado por el valor de *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="bb490-117">The type of structure is determined by the value of *Level*.</span></span>



| <span data-ttu-id="bb490-118">Nivel</span><span class="sxs-lookup"><span data-stu-id="bb490-118">Level</span></span>                                                                                                | <span data-ttu-id="bb490-119">Estructura</span><span class="sxs-lookup"><span data-stu-id="bb490-119">Structure</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bb490-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-120"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bb490-121">Una estructura de [**información de impresora \_ \_ 1**](printer-info-1.md) que contiene información general de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-121">A [**PRINTER\_INFO\_1**](printer-info-1.md) structure containing general printer information.</span></span><br/>                                                                                                        |
| <span id="2"></span><dl> <span data-ttu-id="bb490-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-122"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bb490-123">Estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información detallada acerca de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-123">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                             |
| <span id="3"></span><dl> <span data-ttu-id="bb490-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bb490-125">Una estructura de [**información de impresora \_ \_ 3**](printer-info-3.md) que contiene la información de seguridad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-125">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                 |
| <span id="4"></span><dl> <span data-ttu-id="bb490-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="bb490-127">Una estructura de [**información de impresora \_ \_ 4**](printer-info-4.md) que contiene la información de impresora mínima, incluido el nombre de la impresora, el nombre del servidor y si la impresora es remota o local.</span><span class="sxs-lookup"><span data-stu-id="bb490-127">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="bb490-128"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-128"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="bb490-129">Una estructura de información de impresora [**\_ \_ 5**](printer-info-5.md) que contiene información de la impresora, como los atributos de impresora y la configuración de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="bb490-129">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                               |
| <span id="6"></span><dl> <span data-ttu-id="bb490-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-130"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="bb490-131">Estructura de la información de la [**impresora \_ \_ 6**](printer-info-6.md) que especifica el valor de estado de una impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-131">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                      |
| <span id="7"></span><dl> <span data-ttu-id="bb490-132"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-132"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="bb490-133">Una estructura de [**información de impresora \_ \_ 7**](printer-info-7.md) que indica si la impresora está publicada en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="bb490-133">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure that indicates whether the printer is published in the directory service.</span></span><br/>                                                                      |
| <span id="8"></span><dl> <span data-ttu-id="bb490-134"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-134"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="bb490-135">Una estructura de la información de la [**impresora \_ \_ 8**](printer-info-8.md) que especifica la configuración de impresora predeterminada global.</span><span class="sxs-lookup"><span data-stu-id="bb490-135">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                |
| <span id="9"></span><dl> <span data-ttu-id="bb490-136"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-136"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="bb490-137">Una estructura de [**información de impresora \_ \_ 9**](printer-info-9.md) que especifica la configuración de impresora predeterminada por usuario.</span><span class="sxs-lookup"><span data-stu-id="bb490-137">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="bb490-138">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb490-138">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb490-139">Tamaño, en bytes, del búfer al que apunta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="bb490-139">The size, in bytes, of the buffer pointed to by *pPrinter*.</span></span>

</dd> <dt>

<span data-ttu-id="bb490-140">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bb490-140">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb490-141">Puntero a una variable que la función establece en el tamaño, en bytes, de la información de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-141">A pointer to a variable that the function sets to the size, in bytes, of the printer information.</span></span> <span data-ttu-id="bb490-142">Si *cbBuf* es menor que este valor, **GetPrinter** produce un error y el valor representa el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="bb490-142">If *cbBuf* is smaller than this value, **GetPrinter** fails, and the value represents the required buffer size.</span></span> <span data-ttu-id="bb490-143">Si *cbBuf* es igual o mayor que este valor, **GetPrinter** se realiza correctamente y el valor representa el número de bytes almacenados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="bb490-143">If *cbBuf* is equal to or greater than this value, **GetPrinter** succeeds, and the value represents the number of bytes stored in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb490-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb490-144">Return value</span></span>

<span data-ttu-id="bb490-145">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bb490-145">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bb490-146">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="bb490-146">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb490-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb490-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb490-148">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bb490-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bb490-149">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb490-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bb490-150">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="bb490-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bb490-151">El miembro **pDevMode** de las estructuras [**Printer info \_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)y [**Printer \_ info \_ 9**](printer-info-9.md) puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bb490-151">The **pDevMode** member in the [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_8**](printer-info-8.md), and [**PRINTER\_INFO\_9**](printer-info-9.md) structures can be **NULL**.</span></span> <span data-ttu-id="bb490-152">Cuando esto sucede, la impresora no se puede usar hasta que el controlador se vuelve a instalar correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb490-152">When this happens, the printer is unusable until the driver is reinstalled successfully.</span></span>

<span data-ttu-id="bb490-153">En el caso de las estructuras [**Printer \_ info \_ 2**](printer-info-2.md) y [**Printer \_ info \_ 3**](printer-info-3.md) que contienen un puntero a un descriptor de seguridad, la función solo recupera los componentes del descriptor de seguridad para los que el autor de la llamada tiene permiso de lectura.</span><span class="sxs-lookup"><span data-stu-id="bb490-153">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read.</span></span> <span data-ttu-id="bb490-154">Para recuperar determinados componentes de descriptor de seguridad, debe especificar los derechos de acceso necesarios cuando llame a la función [**OpenPrinter**](openprinter.md) para recuperar un identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-154">To retrieve particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="bb490-155">En la tabla siguiente se muestran los derechos de acceso necesarios para leer los distintos componentes de descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bb490-155">The following table shows the access rights required to read the various security descriptor components.</span></span>



| <span data-ttu-id="bb490-156">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="bb490-156">Access Right</span></span>                        | <span data-ttu-id="bb490-157">Componente de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="bb490-157">Security Descriptor Component</span></span>                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb490-158">CONTROL de lectura \_</span><span class="sxs-lookup"><span data-stu-id="bb490-158">READ\_CONTROL</span></span><br/>            | <span data-ttu-id="bb490-159">Propietario</span><span class="sxs-lookup"><span data-stu-id="bb490-159">Owner</span></span><br/> <span data-ttu-id="bb490-160">Grupo primario</span><span class="sxs-lookup"><span data-stu-id="bb490-160">Primary group</span></span><br/> <span data-ttu-id="bb490-161">Lista de control de acceso discrecional (DACL)</span><span class="sxs-lookup"><span data-stu-id="bb490-161">Discretionary access-control list (DACL)</span></span><br/> |
| <span data-ttu-id="bb490-162">ACCESO a la \_ seguridad del sistema \_</span><span class="sxs-lookup"><span data-stu-id="bb490-162">ACCESS\_SYSTEM\_SECURITY</span></span><br/> | <span data-ttu-id="bb490-163">Lista de control de acceso del sistema (SACL)</span><span class="sxs-lookup"><span data-stu-id="bb490-163">System access-control list (SACL)</span></span><br/>                                                  |



 

<span data-ttu-id="bb490-164">Si especifica el nivel 7, el miembro **dwAction** de la información de la [**impresora \_ \_ 7**](printer-info-7.md) devuelve uno de los siguientes valores para indicar si la impresora está publicada en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="bb490-164">If you specify level 7, the **dwAction** member of [**PRINTER\_INFO\_7**](printer-info-7.md) returns one of the following values to indicate whether the printer is published in the directory service.</span></span>



| <span data-ttu-id="bb490-165">valor dwAction</span><span class="sxs-lookup"><span data-stu-id="bb490-165">dwAction value</span></span>     | <span data-ttu-id="bb490-166">Significado</span><span class="sxs-lookup"><span data-stu-id="bb490-166">Meaning</span></span>                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb490-167">publicación de DSPRINT \_</span><span class="sxs-lookup"><span data-stu-id="bb490-167">DSPRINT\_PUBLISH</span></span>   | <span data-ttu-id="bb490-168">La impresora está publicada.</span><span class="sxs-lookup"><span data-stu-id="bb490-168">The printer is published.</span></span> <span data-ttu-id="bb490-169">El miembro **pszObjectGUID** contiene el GUID del objeto cola de impresión de servicios de directorio asociado a la impresora.</span><span class="sxs-lookup"><span data-stu-id="bb490-169">The **pszObjectGUID** member contains the GUID of the directory services print queue object associated with the printer.</span></span>                                                                                                       |
| <span data-ttu-id="bb490-170">DSPRINT \_ Anular publicación</span><span class="sxs-lookup"><span data-stu-id="bb490-170">DSPRINT\_UNPUBLISH</span></span> | <span data-ttu-id="bb490-171">La impresora no está publicada.</span><span class="sxs-lookup"><span data-stu-id="bb490-171">The printer is not published.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="bb490-172">DSPRINT \_ pendiente</span><span class="sxs-lookup"><span data-stu-id="bb490-172">DSPRINT\_PENDING</span></span>   | <span data-ttu-id="bb490-173">Indica que el sistema está intentando completar una operación de publicación o anulación de publicación.</span><span class="sxs-lookup"><span data-stu-id="bb490-173">Indicates that the system is attempting to complete a publish or unpublish operation.</span></span> <span data-ttu-id="bb490-174">Si una llamada a [**SetPrinter**](setprinter.md) no puede publicar o anular la publicación de una impresora, el sistema realiza más intentos para completar la operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bb490-174">If a [**SetPrinter**](setprinter.md) call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</span></span> |



 

<span data-ttu-id="bb490-175">A partir de Windows Vista, los datos de la impresora devueltos por **GetPrinter** se recuperan de una caché local cuando *hPrinter* hace referencia a una impresora hospedada por un servidor de impresión y hay al menos una conexión abierta con el servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="bb490-175">Starting with Windows Vista, the printer data returned by **GetPrinter** is retrieved from a local cache when *hPrinter* refers to a printer hosted by a print server and there is at least one open connection to the print server.</span></span> <span data-ttu-id="bb490-176">En todas las demás configuraciones, los datos de la impresora se consultan desde el servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="bb490-176">In all other configurations, the printer data is queried from the print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb490-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb490-177">Requirements</span></span>



| <span data-ttu-id="bb490-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb490-178">Requirement</span></span> | <span data-ttu-id="bb490-179">Value</span><span class="sxs-lookup"><span data-stu-id="bb490-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb490-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb490-180">Minimum supported client</span></span><br/> | <span data-ttu-id="bb490-181">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb490-181">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb490-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb490-182">Minimum supported server</span></span><br/> | <span data-ttu-id="bb490-183">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb490-183">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb490-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb490-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb490-185"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-185"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb490-186">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb490-186">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb490-187"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-187"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bb490-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb490-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb490-189"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bb490-189"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bb490-190">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bb490-190">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb490-191">**GetPrinterW** (Unicode) y **GetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb490-191">**GetPrinterW** (Unicode) and **GetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="bb490-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb490-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb490-193">Impresión</span><span class="sxs-lookup"><span data-stu-id="bb490-193">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bb490-194">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="bb490-194">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bb490-195">**AbortPrinter**</span><span class="sxs-lookup"><span data-stu-id="bb490-195">**AbortPrinter**</span></span>](abortprinter.md)
</dt> <dt>

[<span data-ttu-id="bb490-196">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="bb490-196">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="bb490-197">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="bb490-197">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="bb490-198">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="bb490-198">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="bb490-199">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="bb490-199">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="bb490-200">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bb490-200">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="bb490-201">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="bb490-201">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="bb490-202">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="bb490-202">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="bb490-203">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="bb490-203">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="bb490-204">**Información de la impresora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="bb490-204">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="bb490-205">**Información de la impresora \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="bb490-205">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="bb490-206">**Información de la impresora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="bb490-206">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="bb490-207">**Información de la impresora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="bb490-207">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="bb490-208">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bb490-208">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="bb490-209">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="bb490-209">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




