---
description: Especifica el almacenamiento en caché de un identificador para una impresora abierta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumeración PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278344"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="3a2b8-103">\_Enumeración de marcas de opción de impresora \_</span><span class="sxs-lookup"><span data-stu-id="3a2b8-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="3a2b8-104">Especifica el almacenamiento en caché de un identificador para una impresora abierta con [**OpenPrinter2**](openprinter2.md).</span><span class="sxs-lookup"><span data-stu-id="3a2b8-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a2b8-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="3a2b8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3a2b8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3a2b8-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**opción de impresora \_ \_ sin \_ caché**</span><span class="sxs-lookup"><span data-stu-id="3a2b8-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="3a2b8-108">El identificador no está almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="3a2b8-108">The handle is not cached.</span></span> <span data-ttu-id="3a2b8-109">Todas las funciones que se aplican a un identificador devuelto por [**OpenPrinter2**](openprinter2.md) Irán al equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="3a2b8-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="3a2b8-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_caché de opciones de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="3a2b8-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="3a2b8-111">El identificador está almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="3a2b8-111">The handle is cached.</span></span> <span data-ttu-id="3a2b8-112">Todas las funciones que se aplican a un identificador devuelto por [**OpenPrinter2**](openprinter2.md) Irán a la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="3a2b8-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="3a2b8-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_cambio de \_ cliente de opción de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="3a2b8-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="3a2b8-114">[**SetPrinter**](setprinter.md) puede usar el identificador devuelto por [**OpenPrinter2**](openprinter2.md) para cambiar el nombre de la conexión de impresora.</span><span class="sxs-lookup"><span data-stu-id="3a2b8-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a2b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2b8-115">Requirements</span></span>



| <span data-ttu-id="3a2b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2b8-116">Requirement</span></span> | <span data-ttu-id="3a2b8-117">Value</span><span class="sxs-lookup"><span data-stu-id="3a2b8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2b8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a2b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2b8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a2b8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3a2b8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a2b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2b8-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a2b8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a2b8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a2b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2b8-123"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2b8-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2b8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a2b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2b8-125">Impresión</span><span class="sxs-lookup"><span data-stu-id="3a2b8-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3a2b8-126">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="3a2b8-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3a2b8-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="3a2b8-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="3a2b8-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="3a2b8-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




