---
description: Contiene información del controlador de impresora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Estructura de DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361417"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="ecac0-103">Estructura de información de controlador \_ \_ 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="ecac0-104">Contiene información del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ecac0-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecac0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecac0-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="ecac0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ecac0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecac0-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="ecac0-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="ecac0-109">El valor admitido es 3.</span><span class="sxs-lookup"><span data-stu-id="ecac0-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="ecac0-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-111">Un puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="ecac0-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ecac0-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="ecac0-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="ecac0-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-115">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="ecac0-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="ecac0-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-117">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="ecac0-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="ecac0-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-119">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="ecac0-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="ecac0-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-121">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo (por ejemplo, C: \\ drivers \\ Pscrptui. hlp).</span><span class="sxs-lookup"><span data-stu-id="ecac0-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="ecac0-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-123">Un puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="ecac0-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="ecac0-124">Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="ecac0-125">La secuencia de cadenas termina en una cadena vacía de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="ecac0-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="ecac0-126">Si **pDependentFiles** no es **null** y no contiene ningún nombre de archivo, apuntará a un búfer que contenga dos cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="ecac0-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="ecac0-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-128">Un puntero a una cadena terminada en null que especifica un monitor de idioma (por ejemplo, "monitor PJL").</span><span class="sxs-lookup"><span data-stu-id="ecac0-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="ecac0-129">Este miembro puede ser **null** y debe especificarse solo para impresoras capaces de comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="ecac0-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="ecac0-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-131">Un puntero a una cadena terminada en null que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="ecac0-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="ecac0-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-133">Puntero a una cadena terminada en null que especifica los nombres de controladores de impresora anteriores que son compatibles con este controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="ecac0-134">Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="ecac0-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="ecac0-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-136">La fecha del paquete de controladores, como se codifica en los archivos del controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="ecac0-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-138">Número de versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-138">The version number of the driver.</span></span> <span data-ttu-id="ecac0-139">Procede de la estructura de la versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="ecac0-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-141">Puntero a una cadena terminada en null que especifica el nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="ecac0-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="ecac0-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-143">Puntero a una cadena terminada en null que especifica la dirección URL del fabricante.</span><span class="sxs-lookup"><span data-stu-id="ecac0-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="ecac0-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-145">Puntero a una cadena terminada en null que especifica el identificador de hardware para el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ecac0-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="ecac0-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-147">Un puntero a una cadena terminada en null que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000").</span><span class="sxs-lookup"><span data-stu-id="ecac0-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-148">**pszPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="ecac0-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-149">Un puntero a una cadena terminada en null que especifica el procesador de impresión (por ejemplo, "WinPrint").</span><span class="sxs-lookup"><span data-stu-id="ecac0-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-150">**pszVendorSetup**</span><span class="sxs-lookup"><span data-stu-id="ecac0-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-151">Un puntero a una cadena terminada en null que especifica el punto de entrada y la DLL de instalación del controlador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ecac0-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-152">**pszzColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="ecac0-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-153">Puntero a una cadena terminada en null que especifica los perfiles de color asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-154">**pszInfPath**</span><span class="sxs-lookup"><span data-stu-id="ecac0-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-155">Puntero a una cadena terminada en null que especifica la ruta de acceso al archivo. inf del controlador en el almacén de controladores.</span><span class="sxs-lookup"><span data-stu-id="ecac0-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="ecac0-156">(Vea la sección comentarios). Debe ser **null** si la información del \_ controlador \_ 8 se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="ecac0-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-157">**dwPrinterDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="ecac0-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-158">Marcas de atributo para controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="ecac0-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="ecac0-159">Debe ser 0 si la información del \_ controlador \_ 8 se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="ecac0-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="ecac0-160">De lo contrario, puede ser cualquier combinación de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ecac0-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="ecac0-161">Nombre/valor de marca</span><span class="sxs-lookup"><span data-stu-id="ecac0-161">Flag name/value</span></span>                                                         | <span data-ttu-id="ecac0-162">Significado</span><span class="sxs-lookup"><span data-stu-id="ecac0-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ecac0-163">SO mínimo</span><span class="sxs-lookup"><span data-stu-id="ecac0-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="ecac0-164">paquete de controlador de impresora \_ \_ \_ compatible</span><span class="sxs-lookup"><span data-stu-id="ecac0-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="ecac0-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ecac0-165">0x00000001</span></span><br/>        | <span data-ttu-id="ecac0-166">El controlador de impresora forma parte de un paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="ecac0-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ecac0-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecac0-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="ecac0-168">controlador de impresora \_ \_ XPS</span><span class="sxs-lookup"><span data-stu-id="ecac0-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="ecac0-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ecac0-169">0x00000002</span></span><br/>                   | <span data-ttu-id="ecac0-170">El controlador de impresora admite el formato XPS de Microsoft que se describe en la [especificación de XML Paper: información general](/previous-versions/windows/hardware/design/dn641615(v=vs.85))y también en el [comportamiento del producto, sección <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="ecac0-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="ecac0-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-171">Windows 8</span></span><br/> <span data-ttu-id="ecac0-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-173">\_ \_ espacio aislado habilitado del controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="ecac0-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ecac0-174">0x00000004</span></span><br/>      | <span data-ttu-id="ecac0-175">El controlador de impresora es compatible con el [aislamiento de controladores de impresora](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="ecac0-176">Para obtener más información, vea el tema sobre el [comportamiento del producto, la sección <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="ecac0-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="ecac0-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ecac0-177">Windows 7</span></span><br/> <span data-ttu-id="ecac0-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ecac0-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="ecac0-179">\_clase de controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="ecac0-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ecac0-180">0x00000008</span></span><br/>                 | <span data-ttu-id="ecac0-181">El controlador de impresora es un [controlador de impresora de clase](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="ecac0-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-182">Windows 8</span></span><br/> <span data-ttu-id="ecac0-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-184">controlador de impresora \_ \_ derivado</span><span class="sxs-lookup"><span data-stu-id="ecac0-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="ecac0-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecac0-185">0x00000010</span></span><br/>               | <span data-ttu-id="ecac0-186">El controlador de impresora es un [controlador de impresora derivado](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="ecac0-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-187">Windows 8</span></span><br/> <span data-ttu-id="ecac0-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-189">controlador de impresora \_ \_ no \_ compartible</span><span class="sxs-lookup"><span data-stu-id="ecac0-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="ecac0-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ecac0-190">0x00000020</span></span><br/>        | <span data-ttu-id="ecac0-191">Las impresoras que usan este controlador de impresora no se pueden compartir.</span><span class="sxs-lookup"><span data-stu-id="ecac0-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="ecac0-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-192">Windows 8</span></span><br/> <span data-ttu-id="ecac0-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-194">\_fax de \_ categoría de controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="ecac0-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ecac0-195">0x00000040</span></span><br/>         | <span data-ttu-id="ecac0-196">El controlador de impresora está diseñado para su uso con [impresoras de fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="ecac0-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-197">Windows 8</span></span><br/> <span data-ttu-id="ecac0-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-199">\_archivo de \_ categoría del controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="ecac0-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ecac0-200">0x00000080</span></span><br/>        | <span data-ttu-id="ecac0-201">El controlador de impresora está pensado para su uso con [impresoras de archivos](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="ecac0-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-202">Windows 8</span></span><br/> <span data-ttu-id="ecac0-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-204">Categoría de controlador de impresora \_ \_ \_ virtual</span><span class="sxs-lookup"><span data-stu-id="ecac0-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="ecac0-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ecac0-205">0x00000100</span></span><br/>     | <span data-ttu-id="ecac0-206">El controlador de impresora está pensado para su uso con [impresoras virtuales](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="ecac0-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-207">Windows 8</span></span><br/> <span data-ttu-id="ecac0-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-209">\_servicio de \_ categoría de controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="ecac0-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ecac0-210">0x00000200</span></span><br/>     | <span data-ttu-id="ecac0-211">El controlador de impresora está pensado para su uso con [impresoras de servicio](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="ecac0-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="ecac0-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-212">Windows 8</span></span><br/> <span data-ttu-id="ecac0-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="ecac0-214">se \_ \_ \_ requiere restablecimiento parcial del controlador de impresora \_</span><span class="sxs-lookup"><span data-stu-id="ecac0-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="ecac0-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ecac0-215">0x00000400</span></span><br/> | <span data-ttu-id="ecac0-216">Las impresoras que usan este controlador de impresora deben seguir las instrucciones descritas en la definición de clase de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="ecac0-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="ecac0-217">Para obtener más información, vea el tema sobre el [comportamiento del producto, la sección <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="ecac0-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="ecac0-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ecac0-218">Windows 8</span></span><br/> <span data-ttu-id="ecac0-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ecac0-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="ecac0-220">**pszzCoreDriverDependencies**</span><span class="sxs-lookup"><span data-stu-id="ecac0-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-221">Puntero a una cadena múltiple terminada en null que especifica todos los controladores de impresora principales de los que depende el controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="ecac0-222">Debe ser **null** si la **información del \_ controlador \_ 8** se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="ecac0-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-223">**ftMinInboxDriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="ecac0-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-224">La fecha más temprana permitida de los controladores incluidos en Windows y de los que depende este controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="ecac0-225">**dwlMinInboxDriverVerVersion**</span><span class="sxs-lookup"><span data-stu-id="ecac0-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ecac0-226">La versión más temprana permitida de los controladores que se incluyen con Windows y de los que depende este controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecac0-227">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecac0-227">Remarks</span></span>

<span data-ttu-id="ecac0-228">Las cadenas de estos miembros se encuentran en el archivo. inf que se utiliza para agregar el controlador.</span><span class="sxs-lookup"><span data-stu-id="ecac0-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecac0-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecac0-229">Requirements</span></span>



| <span data-ttu-id="ecac0-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecac0-230">Requirement</span></span> | <span data-ttu-id="ecac0-231">Value</span><span class="sxs-lookup"><span data-stu-id="ecac0-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecac0-232">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecac0-232">Minimum supported client</span></span><br/> | <span data-ttu-id="ecac0-233">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecac0-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ecac0-234">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecac0-234">Minimum supported server</span></span><br/> | <span data-ttu-id="ecac0-235">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecac0-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ecac0-236">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecac0-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecac0-237"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecac0-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ecac0-238">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ecac0-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ecac0-239">**\_ Información del controlador \_ \_ 8W** (Unicode) y la **\_ información del controlador \_ \_ 8A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ecac0-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ecac0-240">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecac0-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecac0-241">Impresión</span><span class="sxs-lookup"><span data-stu-id="ecac0-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ecac0-242">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ecac0-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ecac0-243">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ecac0-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ecac0-244">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="ecac0-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

