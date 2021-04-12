---
description: La estructura CONFIGUREDEXPERT asocia un experto con sus datos de configuración.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Estructura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277025"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="12840-103">Estructura CONFIGUREDEXPERT</span><span class="sxs-lookup"><span data-stu-id="12840-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="12840-104">La estructura **CONFIGUREDEXPERT** asocia un experto con sus datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="12840-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="12840-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12840-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="12840-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="12840-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12840-107">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="12840-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="12840-108">Identificador de un experto.</span><span class="sxs-lookup"><span data-stu-id="12840-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="12840-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="12840-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="12840-110">Valores de marca de inicio del experto.</span><span class="sxs-lookup"><span data-stu-id="12840-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="12840-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="12840-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="12840-112">Puntero a una estructura [**EXPERTCONFIG**](expertconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="12840-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12840-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12840-113">Requirements</span></span>



| <span data-ttu-id="12840-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12840-114">Requirement</span></span> | <span data-ttu-id="12840-115">Value</span><span class="sxs-lookup"><span data-stu-id="12840-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="12840-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12840-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12840-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12840-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="12840-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12840-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12840-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12840-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="12840-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12840-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12840-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="12840-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




