---
description: Representa las opciones de la impresora.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Estructura de PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697273"
---
# <a name="printer_options-structure"></a><span data-ttu-id="d1fc9-103">Estructura de opciones de impresora \_</span><span class="sxs-lookup"><span data-stu-id="d1fc9-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="d1fc9-104">Representa las opciones de la impresora.</span><span class="sxs-lookup"><span data-stu-id="d1fc9-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fc9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1fc9-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="d1fc9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1fc9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d1fc9-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d1fc9-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d1fc9-108">Tamaño de la estructura **de \_ Opciones de impresora** .</span><span class="sxs-lookup"><span data-stu-id="d1fc9-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1fc9-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d1fc9-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d1fc9-110">Conjunto de [**marcas de \_ opción \_ de impresora**](printer-option-flags.md) que especifica cómo otras funciones utilizarán el identificador de una impresora devuelta por [**OpenPrinter2**](openprinter2.md) .</span><span class="sxs-lookup"><span data-stu-id="d1fc9-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1fc9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1fc9-111">Requirements</span></span>



| <span data-ttu-id="d1fc9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1fc9-112">Requirement</span></span> | <span data-ttu-id="d1fc9-113">Value</span><span class="sxs-lookup"><span data-stu-id="d1fc9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fc9-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1fc9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fc9-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1fc9-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d1fc9-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1fc9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fc9-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1fc9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d1fc9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1fc9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1fc9-119"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1fc9-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fc9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1fc9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fc9-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="d1fc9-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d1fc9-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="d1fc9-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="d1fc9-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="d1fc9-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="d1fc9-124">**\_marcas de opciones de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="d1fc9-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




