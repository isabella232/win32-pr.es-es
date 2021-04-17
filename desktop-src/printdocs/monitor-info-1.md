---
description: La estructura de supervisión de la \_ información \_ 1 identifica un monitor instalado.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Estructura de MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697154"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="cbe8d-103">Estructura de supervisión de la \_ información \_ 1</span><span class="sxs-lookup"><span data-stu-id="cbe8d-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="cbe8d-104">La estructura de supervisión de la **\_ información \_ 1** identifica un monitor instalado.</span><span class="sxs-lookup"><span data-stu-id="cbe8d-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbe8d-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="cbe8d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cbe8d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cbe8d-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="cbe8d-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="cbe8d-108">Un puntero a una cadena terminada en null que identifica un monitor instalado.</span><span class="sxs-lookup"><span data-stu-id="cbe8d-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbe8d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbe8d-109">Requirements</span></span>



| <span data-ttu-id="cbe8d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe8d-110">Requirement</span></span> | <span data-ttu-id="cbe8d-111">Value</span><span class="sxs-lookup"><span data-stu-id="cbe8d-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe8d-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbe8d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe8d-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cbe8d-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cbe8d-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbe8d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe8d-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbe8d-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cbe8d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbe8d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbe8d-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbe8d-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cbe8d-118">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cbe8d-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cbe8d-119">Supervisión de la **\_ \_ información \_ 1W** (Unicode) y supervisión de la **\_ \_ información \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cbe8d-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="cbe8d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbe8d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe8d-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="cbe8d-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cbe8d-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="cbe8d-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="cbe8d-123">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="cbe8d-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="cbe8d-124">**Información de supervisión \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="cbe8d-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




