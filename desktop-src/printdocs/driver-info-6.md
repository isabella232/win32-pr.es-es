---
description: La estructura de la información del controlador \_ \_ 6 contiene información sobre el controlador de impresora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Estructura de DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697131"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="5757d-103">Estructura de información de controlador \_ \_ 6</span><span class="sxs-lookup"><span data-stu-id="5757d-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="5757d-104">La estructura de la **información del controlador \_ \_ 6** contiene información sobre el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="5757d-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5757d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5757d-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
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
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="5757d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5757d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5757d-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="5757d-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="5757d-109">El valor admitido es 3.</span><span class="sxs-lookup"><span data-stu-id="5757d-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="5757d-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-111">Puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="5757d-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="5757d-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="5757d-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows NT x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="5757d-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="5757d-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-115">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="5757d-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5757d-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="5757d-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-117">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="5757d-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="5757d-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="5757d-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-119">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="5757d-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5757d-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="5757d-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-121">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo (por ejemplo, C: \\ drivers \\ Pscrptui. hlp).</span><span class="sxs-lookup"><span data-stu-id="5757d-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="5757d-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="5757d-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-123">Un puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="5757d-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="5757d-124">Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="5757d-125">La secuencia de cadenas termina en una cadena vacía de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="5757d-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="5757d-126">Si **pDependentFiles** no es **null** y no contiene ningún nombre de archivo, apuntará a un búfer que contenga dos cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="5757d-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="5757d-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-128">Un puntero a una cadena terminada en null que especifica un monitor de idioma (por ejemplo, "monitor PJL").</span><span class="sxs-lookup"><span data-stu-id="5757d-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="5757d-129">Este miembro puede ser **null** y debe especificarse solo para impresoras capaces de comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="5757d-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="5757d-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-131">Un puntero a una cadena terminada en null que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="5757d-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="5757d-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="5757d-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-133">Puntero a una cadena terminada en null que especifica los nombres de controladores de impresora anteriores que son compatibles con este controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="5757d-134">Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="5757d-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="5757d-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-136">La fecha del paquete de controladores, como se codifica en los archivos del controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="5757d-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-138">Número de versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-138">Version number of the driver.</span></span> <span data-ttu-id="5757d-139">Esto sale de la estructura de la versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="5757d-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-141">Puntero a una cadena terminada en null que especifica el nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="5757d-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="5757d-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-143">Puntero a una cadena terminada en null que especifica la dirección URL del fabricante.</span><span class="sxs-lookup"><span data-stu-id="5757d-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="5757d-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-145">Puntero a una cadena terminada en null que especifica el identificador de hardware para el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="5757d-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="5757d-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="5757d-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="5757d-147">Puntero a una cadena terminada en null que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000")</span><span class="sxs-lookup"><span data-stu-id="5757d-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5757d-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5757d-148">Remarks</span></span>

<span data-ttu-id="5757d-149">Las cadenas de estos miembros se encuentran en el archivo. inf que se utiliza para agregar el controlador.</span><span class="sxs-lookup"><span data-stu-id="5757d-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="5757d-150">Si llama a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md) con un *nivel* distinto de 6 y, a continuación, llama a [**GetPrinterDriver**](getprinterdriver.md) o [**EnumPrinterDrivers**](enumprinterdrivers.md) con un *nivel* igual a 6, la estructura de la **información del controlador \_ \_ 6** se devuelve con **pszMfgName**, **pszOEMUrl**, **pszHardwareID** y **pszProvider** establecidos en **null**, **dwlDriverVersion** establecido en 0 y **ftDriverDate** establecido en (0,0).</span><span class="sxs-lookup"><span data-stu-id="5757d-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5757d-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5757d-151">Requirements</span></span>



| <span data-ttu-id="5757d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="5757d-152">Requirement</span></span> | <span data-ttu-id="5757d-153">Value</span><span class="sxs-lookup"><span data-stu-id="5757d-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5757d-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5757d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5757d-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5757d-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5757d-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5757d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5757d-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5757d-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5757d-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5757d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="5757d-159"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5757d-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5757d-160">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5757d-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5757d-161">**\_ Información del controlador \_ \_ 6W** (Unicode) y la **\_ información del controlador \_ \_ 6A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5757d-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="5757d-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="5757d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5757d-163">Impresión</span><span class="sxs-lookup"><span data-stu-id="5757d-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5757d-164">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="5757d-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5757d-165">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="5757d-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="5757d-166">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="5757d-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="5757d-167">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="5757d-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="5757d-168">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="5757d-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




