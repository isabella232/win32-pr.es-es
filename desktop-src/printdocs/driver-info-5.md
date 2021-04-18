---
description: La estructura de la información del controlador \_ \_ 5 contiene información sobre el controlador de impresora.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: Estructura de DRIVER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697668"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="1d421-103">Estructura de la información de controlador \_ \_ 5</span><span class="sxs-lookup"><span data-stu-id="1d421-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="1d421-104">La estructura de la **información del controlador \_ \_ 5** contiene información sobre el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="1d421-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d421-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d421-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="1d421-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d421-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d421-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="1d421-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="1d421-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="1d421-109">El valor admitido es 3.</span><span class="sxs-lookup"><span data-stu-id="1d421-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="1d421-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="1d421-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-111">Puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="1d421-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="1d421-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="1d421-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="1d421-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="1d421-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="1d421-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-115">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="1d421-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="1d421-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="1d421-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-117">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="1d421-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="1d421-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="1d421-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-119">Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="1d421-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="1d421-120">**dwDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="1d421-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-121">Atributos del controlador, como UMPD/KMPD.</span><span class="sxs-lookup"><span data-stu-id="1d421-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="1d421-122">**dwConfigVersion**</span><span class="sxs-lookup"><span data-stu-id="1d421-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-123">Número de veces que el archivo de configuración de este controlador se ha actualizado o degradado desde el último reinicio del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d421-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="1d421-124">**dwDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="1d421-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1d421-125">Número de veces que el archivo de controlador para este controlador se ha actualizado o degradado desde el último reinicio del administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d421-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d421-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d421-126">Requirements</span></span>



| <span data-ttu-id="1d421-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d421-127">Requirement</span></span> | <span data-ttu-id="1d421-128">Value</span><span class="sxs-lookup"><span data-stu-id="1d421-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d421-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d421-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1d421-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1d421-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1d421-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d421-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1d421-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d421-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1d421-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d421-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d421-134"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d421-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1d421-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1d421-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1d421-136">**\_ Información del controlador \_ \_ 5W** (Unicode) y la **\_ información del controlador \_ \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1d421-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="1d421-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d421-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d421-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="1d421-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1d421-139">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="1d421-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1d421-140">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1d421-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1d421-141">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1d421-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1d421-142">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1d421-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




