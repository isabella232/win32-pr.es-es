---
description: La función AddPrinterDriverEx instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Función AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677730"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="edeef-103">AddPrinterDriverEx función)</span><span class="sxs-lookup"><span data-stu-id="edeef-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="edeef-104">La función **AddPrinterDriverEx** instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador.</span><span class="sxs-lookup"><span data-stu-id="edeef-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="edeef-105">Además de tener las funcionalidades de [**AddPrinterDriver**](addprinterdriver.md), también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).</span><span class="sxs-lookup"><span data-stu-id="edeef-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="edeef-106">Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="edeef-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="edeef-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="edeef-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="edeef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edeef-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="edeef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edeef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edeef-110">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edeef-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edeef-111">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el controlador.</span><span class="sxs-lookup"><span data-stu-id="edeef-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="edeef-112">Si este parámetro es **null**, la función instala el controlador en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="edeef-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="edeef-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="edeef-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edeef-114">Versión de la estructura a la que apunta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="edeef-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="edeef-115">Este valor puede ser 2, 3, 4, 6 u 8.</span><span class="sxs-lookup"><span data-stu-id="edeef-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="edeef-116">*pDriverInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="edeef-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="edeef-117">Puntero a una estructura que contiene información del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="edeef-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="edeef-118">Puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="edeef-118">It can be one of the following.</span></span>



| <span data-ttu-id="edeef-119">Valor de nivel</span><span class="sxs-lookup"><span data-stu-id="edeef-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="edeef-120">\_Estructura de información del controlador \_ \*</span><span class="sxs-lookup"><span data-stu-id="edeef-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="edeef-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="edeef-122">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="edeef-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="edeef-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="edeef-124">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="edeef-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="edeef-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="edeef-126">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="edeef-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="edeef-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="edeef-128">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="edeef-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="edeef-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="edeef-130">**Información del controlador \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="edeef-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="edeef-131">Si el miembro **pEnvironment** de la estructura a la que apunta *pDriverInfo* es **null**, la función usa el entorno actual del llamador o el cliente, no el entorno del servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="edeef-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="edeef-132">*dwFileCopyFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edeef-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edeef-133">Opciones para copiar los archivos del controlador.</span><span class="sxs-lookup"><span data-stu-id="edeef-133">The options for copying the driver files.</span></span> <span data-ttu-id="edeef-134">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="edeef-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="edeef-135">Valor</span><span class="sxs-lookup"><span data-stu-id="edeef-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="edeef-136">Significado</span><span class="sxs-lookup"><span data-stu-id="edeef-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="edeef-137"><dt>**APD \_ copiar \_ todos \_ los archivos**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="edeef-138">Agregue el controlador de impresora y copie todos los archivos en el directorio Printer-driver.</span><span class="sxs-lookup"><span data-stu-id="edeef-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="edeef-139">Las marcas de tiempo de archivo se omiten con esta opción.</span><span class="sxs-lookup"><span data-stu-id="edeef-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="edeef-140"><dt>**APD \_ copiar \_ desde el \_ directorio**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="edeef-141">Agregue el controlador de impresora con los nombres de archivo completos especificados en la estructura de [**información de controlador \_ \_ 6**](driver-info-6.md) .</span><span class="sxs-lookup"><span data-stu-id="edeef-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="edeef-142">Esta marca es ORed junto con una de las otras marcas de copia.</span><span class="sxs-lookup"><span data-stu-id="edeef-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="edeef-143">Si se establece esta marca, **AddPrinterDriverEx** producirá un error si los archivos no existen donde se especifica que existen en la estructura de **información de controlador \_ \_ 6** .</span><span class="sxs-lookup"><span data-stu-id="edeef-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="edeef-144">No es necesario que los archivos se copien en el directorio del controlador de impresora del sistema.</span><span class="sxs-lookup"><span data-stu-id="edeef-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="edeef-145">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="edeef-145">See the Remarks.</span></span><br/> <span data-ttu-id="edeef-146">**Windows 2000:** Esta marca no se admite.</span><span class="sxs-lookup"><span data-stu-id="edeef-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="edeef-147"><dt>**APD \_ copiar \_ \_ archivos nuevos**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="edeef-148">Agregue el controlador de impresora y copie los archivos en el directorio de controlador de impresora que son más recientes que los archivos correspondientes que se están usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="edeef-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="edeef-149">Esta marca emula el comportamiento de [**AddPrinterDriver**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="edeef-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="edeef-150"><dt>**\_degradación estricta de APD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="edeef-151">Agregue el controlador de impresora sólo si todos los archivos del directorio de controladores de impresora son más antiguos que los archivos correspondientes que se estén usando.</span><span class="sxs-lookup"><span data-stu-id="edeef-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="edeef-152"><dt>**\_actualización estricta de APD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="edeef-153">Agregue el controlador de impresora sólo si todos los archivos del directorio de controladores de impresora son más recientes que los archivos correspondientes actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="edeef-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edeef-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edeef-154">Return value</span></span>

<span data-ttu-id="edeef-155">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="edeef-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="edeef-156">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="edeef-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="edeef-157">Si se sabe que el controlador de impresora tiene problemas para trabajar con el sistema operativo, **AddPrinterDriverEx** producirá un error con uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="edeef-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="edeef-158">Código de error</span><span class="sxs-lookup"><span data-stu-id="edeef-158">Error Code</span></span>                      | <span data-ttu-id="edeef-159">Significado</span><span class="sxs-lookup"><span data-stu-id="edeef-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edeef-160">controlador de impresora de ERROR \_ \_ \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="edeef-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="edeef-161">El controlador no funciona en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="edeef-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="edeef-162">\_Advertencia de \_ controlador de impresora de error \_</span><span class="sxs-lookup"><span data-stu-id="edeef-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="edeef-163">El controlador no es confiable en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="edeef-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="edeef-164">Sin embargo, si \_ \_ \_ se especifica APD instalar el controlador de advertencias, el controlador está instalado y no se proporciona ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="edeef-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="edeef-165">Para obtener más información, vea la sección Notas.</span><span class="sxs-lookup"><span data-stu-id="edeef-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="edeef-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edeef-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="edeef-167">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="edeef-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="edeef-168">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="edeef-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="edeef-169">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="edeef-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="edeef-170">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="edeef-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="edeef-171">Antes de llamar a la función **AddPrinterDriverEx** , todos los archivos requeridos por el controlador se deben copiar en el directorio de controladores de impresora del sistema.</span><span class="sxs-lookup"><span data-stu-id="edeef-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="edeef-172">Para recuperar el nombre de este directorio, llame a la función [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="edeef-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="edeef-173">Para determinar qué controladores de impresora están instalados actualmente, llame a la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="edeef-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="edeef-174">Si el controlador de impresora se ha agregado correctamente, la función llama a la función DrvDriverEvent (controlador de \_ eventos \_ inicializados, nivel, información de controlador \_ \_ \* , lParam) para permitir que el controlador realice las inicializaciones necesarias durante la instalación de un controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="edeef-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="edeef-175">Para obtener más información acerca de **DrvDriverEvent**, consulte el kit de desarrollo de controladores de Microsoft Windows (DDK)</span><span class="sxs-lookup"><span data-stu-id="edeef-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="edeef-176">El controlador no debe usar una llamada de interfaz de usuario durante la llamada a **DrvDriverEvent**.</span><span class="sxs-lookup"><span data-stu-id="edeef-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="edeef-177">Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada VendorSetup en el archivo. inf de la impresora o, para Plug and Play dispositivos, el instalador puede usar un Coinstalador específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edeef-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="edeef-178">Para obtener más información sobre VendorSetup, consulte el DDK.</span><span class="sxs-lookup"><span data-stu-id="edeef-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="edeef-179">Los archivos a los que se hace referencia en la estructura de la [**información de controlador \_ \_ 6**](driver-info-6.md) deben ser locales en la máquina desde la que se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="edeef-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="edeef-180">Un nombre de archivo puede ser un nombre UNC siempre que el nombre UNC sea el equipo local.</span><span class="sxs-lookup"><span data-stu-id="edeef-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="edeef-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edeef-181">Requirements</span></span>



| <span data-ttu-id="edeef-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="edeef-182">Requirement</span></span> | <span data-ttu-id="edeef-183">Value</span><span class="sxs-lookup"><span data-stu-id="edeef-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edeef-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edeef-184">Minimum supported client</span></span><br/> | <span data-ttu-id="edeef-185">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="edeef-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="edeef-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edeef-186">Minimum supported server</span></span><br/> | <span data-ttu-id="edeef-187">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edeef-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="edeef-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edeef-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="edeef-189"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="edeef-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edeef-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="edeef-191"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="edeef-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edeef-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edeef-193"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="edeef-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="edeef-194">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="edeef-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="edeef-195">**AddPrinterDriverExW** (Unicode) y **AddPrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="edeef-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="edeef-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="edeef-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edeef-197">Impresión</span><span class="sxs-lookup"><span data-stu-id="edeef-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="edeef-198">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="edeef-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="edeef-199">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="edeef-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="edeef-200">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="edeef-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="edeef-201">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="edeef-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="edeef-202">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="edeef-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="edeef-203">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="edeef-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="edeef-204">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="edeef-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="edeef-205">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="edeef-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="edeef-206">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="edeef-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

