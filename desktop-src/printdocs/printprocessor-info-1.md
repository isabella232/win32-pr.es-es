---
description: La \_ estructura PRINTPROCESSOR info \_ 1 especifica el nombre de un procesador de impresión instalado.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Estructura de PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697496"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="c5188-103">PRINTPROCESSOR \_ estructura de información \_ 1</span><span class="sxs-lookup"><span data-stu-id="c5188-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="c5188-104">La estructura **PRINTPROCESSOR \_ info \_ 1** especifica el nombre de un procesador de impresión instalado.</span><span class="sxs-lookup"><span data-stu-id="c5188-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5188-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5188-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="c5188-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5188-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5188-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="c5188-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="c5188-108">Puntero a una cadena terminada en null que especifica el nombre de un procesador de impresión instalado.</span><span class="sxs-lookup"><span data-stu-id="c5188-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5188-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5188-109">Requirements</span></span>



| <span data-ttu-id="c5188-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5188-110">Requirement</span></span> | <span data-ttu-id="c5188-111">Value</span><span class="sxs-lookup"><span data-stu-id="c5188-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5188-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5188-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c5188-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5188-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5188-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5188-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c5188-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5188-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5188-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5188-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5188-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5188-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c5188-118">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c5188-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c5188-119">**\_ PRINTPROCESSOR \_ info \_ 1W** (Unicode) y **\_ PRINTPROCESSOR \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c5188-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c5188-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5188-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5188-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="c5188-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c5188-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="c5188-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c5188-123">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="c5188-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




