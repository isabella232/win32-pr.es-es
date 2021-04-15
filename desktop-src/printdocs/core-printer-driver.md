---
description: Representa un controlador de impresora del que dependen otros controladores de impresora.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Estructura de CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648375"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="0070b-103">Estructura del controlador de \_ impresora principal \_</span><span class="sxs-lookup"><span data-stu-id="0070b-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="0070b-104">Representa un controlador de impresora del que dependen otros controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="0070b-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="0070b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0070b-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="0070b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0070b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0070b-107">**CoreDriverGUID**</span><span class="sxs-lookup"><span data-stu-id="0070b-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="0070b-108">GUID del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="0070b-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="0070b-109">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="0070b-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="0070b-110">Fecha y hora de la versión más reciente del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="0070b-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="0070b-111">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="0070b-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0070b-112">El ID. de versión de la versión más reciente del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="0070b-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="0070b-113">**\[ruta de acceso máxima de szPackageID \_\]**</span><span class="sxs-lookup"><span data-stu-id="0070b-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="0070b-114">La ruta de acceso al paquete de controladores que contiene el controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="0070b-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0070b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0070b-115">Remarks</span></span>

<span data-ttu-id="0070b-116">Esta estructura puede representar el controlador base de un fabricante en el que dependen los controladores de varios modelos de impresora.</span><span class="sxs-lookup"><span data-stu-id="0070b-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="0070b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0070b-117">Requirements</span></span>



| <span data-ttu-id="0070b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0070b-118">Requirement</span></span> | <span data-ttu-id="0070b-119">Value</span><span class="sxs-lookup"><span data-stu-id="0070b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0070b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0070b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0070b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0070b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0070b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0070b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0070b-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0070b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0070b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0070b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0070b-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0070b-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0070b-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0070b-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0070b-127">**\_ Core \_ Printer \_ DRIVERW** (Unicode) y **\_ Core \_ Printer \_ drivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0070b-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0070b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0070b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0070b-129">Impresión</span><span class="sxs-lookup"><span data-stu-id="0070b-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0070b-130">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="0070b-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




