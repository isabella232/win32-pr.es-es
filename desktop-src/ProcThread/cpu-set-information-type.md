---
description: Representa el tipo de información de la estructura de información de conjunto de CPU del sistema \_ \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Enumeración CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677867"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="805d4-103">\_ \_ Enumeración de tipo de información de conjunto de CPU \_</span><span class="sxs-lookup"><span data-stu-id="805d4-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="805d4-104">Representa el tipo de información de la estructura de [**\_ información de \_ conjunto \_ de CPU del sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .</span><span class="sxs-lookup"><span data-stu-id="805d4-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="805d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="805d4-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="805d4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="805d4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="805d4-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span><span class="sxs-lookup"><span data-stu-id="805d4-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="805d4-108">La estructura contiene información de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="805d4-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="805d4-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805d4-109">Requirements</span></span>



| <span data-ttu-id="805d4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="805d4-110">Requirement</span></span> | <span data-ttu-id="805d4-111">Value</span><span class="sxs-lookup"><span data-stu-id="805d4-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805d4-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805d4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="805d4-113">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="805d4-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="805d4-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805d4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="805d4-115">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="805d4-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="805d4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="805d4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="805d4-117"><dt>Processthreadsapi. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="805d4-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




