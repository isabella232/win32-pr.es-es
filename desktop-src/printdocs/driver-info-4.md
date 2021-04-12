---
description: La estructura de la información de controlador \_ \_ 4 contiene información sobre el controlador de impresora.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Estructura de DRIVER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276662"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="a9610-103">Estructura de la información de controlador \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="a9610-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="a9610-104">La estructura de la **información de controlador \_ \_ 4** contiene información sobre el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="a9610-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9610-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9610-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="a9610-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9610-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9610-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="a9610-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="a9610-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="a9610-109">El valor admitido es 3.</span><span class="sxs-lookup"><span data-stu-id="a9610-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="a9610-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="a9610-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-111">Puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="a9610-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="a9610-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="a9610-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a9610-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="a9610-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="a9610-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-115">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="a9610-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="a9610-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="a9610-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-117">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="a9610-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="a9610-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="a9610-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-119">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="a9610-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="a9610-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="a9610-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-121">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9610-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="a9610-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="a9610-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-123">Un puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="a9610-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="a9610-124">Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador.</span><span class="sxs-lookup"><span data-stu-id="a9610-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="a9610-125">La secuencia de cadenas termina en una cadena vacía de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="a9610-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="a9610-126">Si **pDependentFiles** no es **null** y no contiene ningún nombre de archivo, apuntará a un búfer que contenga dos cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="a9610-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="a9610-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="a9610-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-128">Un puntero a una cadena terminada en null que especifica un monitor de idioma (por ejemplo, el monitor PJL).</span><span class="sxs-lookup"><span data-stu-id="a9610-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="a9610-129">Este miembro puede ser **null** y debe especificarse solo para impresoras capaces de comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="a9610-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="a9610-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="a9610-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-131">Un puntero a una cadena terminada en null que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, EMF).</span><span class="sxs-lookup"><span data-stu-id="a9610-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="a9610-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="a9610-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="a9610-133">Puntero a una cadena terminada en null que especifica los nombres de controladores de impresora anteriores que son compatibles con este controlador.</span><span class="sxs-lookup"><span data-stu-id="a9610-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="a9610-134">Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="a9610-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9610-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9610-135">Requirements</span></span>



| <span data-ttu-id="a9610-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9610-136">Requirement</span></span> | <span data-ttu-id="a9610-137">Value</span><span class="sxs-lookup"><span data-stu-id="a9610-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9610-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9610-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a9610-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9610-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9610-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9610-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a9610-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9610-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9610-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9610-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9610-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9610-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a9610-144">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a9610-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9610-145">**\_ Información del controlador \_ \_ 4W** (Unicode) y la **\_ información del controlador \_ \_ 4A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a9610-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="a9610-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9610-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9610-147">Impresión</span><span class="sxs-lookup"><span data-stu-id="a9610-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a9610-148">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a9610-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a9610-149">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a9610-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="a9610-150">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="a9610-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="a9610-151">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a9610-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




