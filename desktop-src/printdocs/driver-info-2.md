---
description: La estructura de la información de controlador \_ \_ 2 identifica un controlador de impresora, el número de versión del controlador, el entorno para el que se escribió el controlador, el nombre del archivo en el que está almacenado el controlador, etc.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Estructura de DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716028"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="e96e9-103">Estructura de la información de controlador \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="e96e9-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="e96e9-104">La estructura de la **información de controlador \_ \_ 2** identifica un controlador de impresora, el número de versión del controlador, el entorno para el que se escribió el controlador, el nombre del archivo en el que está almacenado el controlador, etc.</span><span class="sxs-lookup"><span data-stu-id="e96e9-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="e96e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e96e9-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="e96e9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e96e9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e96e9-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="e96e9-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-108">Versión del sistema operativo para el que se escribió el controlador.</span><span class="sxs-lookup"><span data-stu-id="e96e9-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="e96e9-109">El valor admitido es 3.</span><span class="sxs-lookup"><span data-stu-id="e96e9-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="e96e9-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="e96e9-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-111">Un puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="e96e9-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="e96e9-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="e96e9-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-113">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e96e9-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="e96e9-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="e96e9-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-115">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, "c: \\ drivers \\pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="e96e9-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="e96e9-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="e96e9-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-117">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, "c: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="e96e9-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="e96e9-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="e96e9-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="e96e9-119">Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para Configuration. dll del controlador de dispositivo (por ejemplo, "c: \\ drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="e96e9-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e96e9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e96e9-120">Requirements</span></span>



| <span data-ttu-id="e96e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96e9-121">Requirement</span></span> | <span data-ttu-id="e96e9-122">Value</span><span class="sxs-lookup"><span data-stu-id="e96e9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e96e9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e96e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e96e9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e96e9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e96e9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e96e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e96e9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e96e9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e96e9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e96e9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96e9-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e96e9-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e96e9-129">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e96e9-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e96e9-130">**\_ Información del controlador \_ \_ 2W** (Unicode) y la **\_ información del controlador \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e96e9-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="e96e9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e96e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96e9-132">Impresión</span><span class="sxs-lookup"><span data-stu-id="e96e9-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e96e9-133">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="e96e9-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e96e9-134">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="e96e9-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="e96e9-135">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="e96e9-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




