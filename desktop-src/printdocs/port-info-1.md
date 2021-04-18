---
description: La estructura de la información de puerto \_ \_ 1 identifica un puerto de impresora compatible.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Estructura de PORT_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706302"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="be2d3-103">Estructura de información de puerto \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="be2d3-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="be2d3-104">La estructura de la **información de puerto \_ \_ 1** identifica un puerto de impresora compatible.</span><span class="sxs-lookup"><span data-stu-id="be2d3-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="be2d3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be2d3-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="be2d3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="be2d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="be2d3-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="be2d3-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="be2d3-108">Puntero a una cadena terminada en null que identifica un puerto de impresora compatible (por ejemplo, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="be2d3-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be2d3-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be2d3-109">Requirements</span></span>



| <span data-ttu-id="be2d3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="be2d3-110">Requirement</span></span> | <span data-ttu-id="be2d3-111">Value</span><span class="sxs-lookup"><span data-stu-id="be2d3-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2d3-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be2d3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="be2d3-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="be2d3-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be2d3-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be2d3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="be2d3-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be2d3-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be2d3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be2d3-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="be2d3-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be2d3-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="be2d3-118">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="be2d3-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="be2d3-119">**\_ Información de puerto \_ \_ 1s** (Unicode) y la **\_ información de puerto \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="be2d3-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="be2d3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="be2d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be2d3-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="be2d3-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="be2d3-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="be2d3-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="be2d3-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="be2d3-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




