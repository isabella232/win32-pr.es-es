---
description: La estructura de la información de controlador \_ \_ 3 contiene información sobre el controlador de impresora.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Estructura de DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716797"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="e3736-103">Estructura de información de controladores \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="e3736-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="e3736-104">La estructura de la **información de controlador \_ \_ 3** contiene información sobre el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="e3736-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3736-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3736-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
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
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="e3736-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3736-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3736-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="e3736-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="e3736-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="e3736-109">Los valores admitidos son 3 y 4, que representan los controladores V3 y V4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e3736-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="e3736-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="e3736-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-111">Un puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="e3736-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="e3736-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="e3736-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e3736-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="e3736-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="e3736-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-115">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, "C: \\ DRIVERS \\Pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="e3736-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="e3736-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="e3736-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-117">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, "C: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="e3736-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="e3736-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="e3736-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-119">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, "C: \\ DRIVERS \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="e3736-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="e3736-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="e3736-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-121">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3736-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="e3736-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="e3736-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-123">Un puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="e3736-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="e3736-124">Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador.</span><span class="sxs-lookup"><span data-stu-id="e3736-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="e3736-125">La secuencia de cadenas termina en una cadena vacía de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="e3736-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="e3736-126">Si **pDependentFiles** no es **null** y no contiene ningún nombre de archivo, apuntará a un búfer que contenga dos cadenas vacías.</span><span class="sxs-lookup"><span data-stu-id="e3736-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="e3736-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="e3736-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-128">Un puntero a una cadena terminada en null que especifica un monitor de idioma (por ejemplo, "monitor PJL").</span><span class="sxs-lookup"><span data-stu-id="e3736-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="e3736-129">Este miembro puede ser **null** y debe especificarse solo para impresoras capaces de comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="e3736-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="e3736-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="e3736-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="e3736-131">Un puntero a una cadena terminada en null que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="e3736-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3736-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3736-132">Requirements</span></span>



| <span data-ttu-id="e3736-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3736-133">Requirement</span></span> | <span data-ttu-id="e3736-134">Value</span><span class="sxs-lookup"><span data-stu-id="e3736-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3736-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3736-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3736-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3736-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3736-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3736-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3736-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3736-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3736-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3736-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3736-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3736-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e3736-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e3736-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e3736-142">**\_ Información del controlador \_ \_ 3W** (Unicode) y la **\_ información del controlador \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e3736-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e3736-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3736-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3736-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="e3736-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e3736-145">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="e3736-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e3736-146">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="e3736-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="e3736-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="e3736-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="e3736-148">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="e3736-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




