---
description: La \_ estructura supervisar información \_ 2 identifica un monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Estructura de MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817899"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="9e6cc-103">Estructura de supervisión de \_ información \_ 2</span><span class="sxs-lookup"><span data-stu-id="9e6cc-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="9e6cc-104">La estructura **supervisar \_ información \_ 2** identifica un monitor.</span><span class="sxs-lookup"><span data-stu-id="9e6cc-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e6cc-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="9e6cc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e6cc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e6cc-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="9e6cc-108">Puntero a una cadena terminada en null que es el nombre del monitor.</span><span class="sxs-lookup"><span data-stu-id="9e6cc-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9e6cc-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="9e6cc-110">Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el monitor (por ejemplo, Windows NT x86, Windows IA64, Windows x64).</span><span class="sxs-lookup"><span data-stu-id="9e6cc-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="9e6cc-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="9e6cc-112">Un puntero a una cadena terminada en null que es el nombre del archivo DLL del monitor.</span><span class="sxs-lookup"><span data-stu-id="9e6cc-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e6cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e6cc-113">Requirements</span></span>



| <span data-ttu-id="9e6cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6cc-114">Requirement</span></span> | <span data-ttu-id="9e6cc-115">Value</span><span class="sxs-lookup"><span data-stu-id="9e6cc-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6cc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e6cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6cc-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9e6cc-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9e6cc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e6cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6cc-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e6cc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9e6cc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e6cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e6cc-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e6cc-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9e6cc-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9e6cc-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9e6cc-123">**\_ Supervisar la \_ información \_ 2W** (Unicode) y la **\_ información de supervisión \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9e6cc-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="9e6cc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e6cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6cc-125">Impresión</span><span class="sxs-lookup"><span data-stu-id="9e6cc-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9e6cc-126">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="9e6cc-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9e6cc-127">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="9e6cc-128">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="9e6cc-129">**Información de supervisión \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9e6cc-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




