---
description: La \_ estructura valores predeterminados de impresora especifica el tipo de datos, el entorno, los datos de inicialización y los derechos de acceso predeterminados para una impresora.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Estructura de PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678043"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="5c6ea-103">\_Estructura de valores predeterminados de impresora</span><span class="sxs-lookup"><span data-stu-id="5c6ea-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="5c6ea-104">La **estructura \_ valores predeterminados de impresora** especifica el tipo de datos, el entorno, los datos de inicialización y los derechos de acceso predeterminados para una impresora.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c6ea-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="5c6ea-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c6ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c6ea-107">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="5c6ea-108">Puntero a una cadena terminada en null que especifica el tipo de datos predeterminado para una impresora.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="5c6ea-109">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="5c6ea-110">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que identifica el entorno predeterminado y los datos de inicialización de una impresora.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="5c6ea-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="5c6ea-112">Especifica los derechos de acceso deseados para una impresora.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="5c6ea-113">La función [**OpenPrinter**](openprinter.md) usa este miembro para establecer los derechos de acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="5c6ea-114">Estos derechos pueden afectar al funcionamiento de las funciones [**SetPrinter**](setprinter.md) y [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6ea-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="5c6ea-115">Los derechos de acceso pueden ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="5c6ea-116">Value</span><span class="sxs-lookup"><span data-stu-id="5c6ea-116">Value</span></span>                                       | <span data-ttu-id="5c6ea-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5c6ea-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6ea-118">\_administrar el acceso a las impresoras \_</span><span class="sxs-lookup"><span data-stu-id="5c6ea-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="5c6ea-119">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="5c6ea-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="5c6ea-120">\_uso de acceso a impresoras \_</span><span class="sxs-lookup"><span data-stu-id="5c6ea-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="5c6ea-121">Para realizar operaciones de impresión básicas.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="5c6ea-122">\_acceso limitado de administración de acceso a impresoras \_ \_</span><span class="sxs-lookup"><span data-stu-id="5c6ea-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="5c6ea-123">Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="5c6ea-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="5c6ea-124">Este valor está disponible a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="5c6ea-125">\_todo el \_ acceso a la impresora</span><span class="sxs-lookup"><span data-stu-id="5c6ea-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="5c6ea-126">Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto la sincronización (consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="5c6ea-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="5c6ea-127">valores de seguridad genéricos, como WRITE \_ DAC</span><span class="sxs-lookup"><span data-stu-id="5c6ea-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="5c6ea-128">Para permitir derechos de acceso de control específicos.</span><span class="sxs-lookup"><span data-stu-id="5c6ea-128">To allow specific control access rights.</span></span> <span data-ttu-id="5c6ea-129">Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="5c6ea-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c6ea-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c6ea-130">Requirements</span></span>



| <span data-ttu-id="5c6ea-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6ea-131">Requirement</span></span> | <span data-ttu-id="5c6ea-132">Value</span><span class="sxs-lookup"><span data-stu-id="5c6ea-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6ea-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c6ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c6ea-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5c6ea-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c6ea-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c6ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c6ea-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c6ea-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c6ea-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c6ea-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c6ea-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c6ea-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5c6ea-139">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5c6ea-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c6ea-140">**\_ Impresora \_ DEFAULTSW** (Unicode) y **\_ \_ DEFAULTSA de impresora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5c6ea-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5c6ea-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c6ea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6ea-142">Impresión</span><span class="sxs-lookup"><span data-stu-id="5c6ea-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5c6ea-143">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="5c6ea-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5c6ea-144">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="5c6ea-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="5c6ea-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="5c6ea-147">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="5c6ea-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

