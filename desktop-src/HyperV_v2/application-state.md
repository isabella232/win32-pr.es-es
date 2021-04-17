---
description: Especifica el estado de mantenimiento de una aplicación.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Enumeración APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667477"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="09a02-103">\_Enumeración de estado de aplicación</span><span class="sxs-lookup"><span data-stu-id="09a02-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="09a02-104">Especifica el estado de mantenimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="09a02-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09a02-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="09a02-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="09a02-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09a02-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span><span class="sxs-lookup"><span data-stu-id="09a02-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="09a02-108">El estado de la aplicación es correcto.</span><span class="sxs-lookup"><span data-stu-id="09a02-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="09a02-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span><span class="sxs-lookup"><span data-stu-id="09a02-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="09a02-110">El estado de la aplicación es crítico.</span><span class="sxs-lookup"><span data-stu-id="09a02-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09a02-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09a02-111">Remarks</span></span>

<span data-ttu-id="09a02-112">Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09a02-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a02-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09a02-113">Requirements</span></span>



| <span data-ttu-id="09a02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a02-114">Requirement</span></span> | <span data-ttu-id="09a02-115">Value</span><span class="sxs-lookup"><span data-stu-id="09a02-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a02-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09a02-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="09a02-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="09a02-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09a02-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="09a02-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09a02-120">Versión</span><span class="sxs-lookup"><span data-stu-id="09a02-120">Version</span></span><br/>                  | <span data-ttu-id="09a02-121">Componentes de integración para Windows 8</span><span class="sxs-lookup"><span data-stu-id="09a02-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="09a02-122">IDL</span><span class="sxs-lookup"><span data-stu-id="09a02-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09a02-123"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09a02-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a02-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="09a02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a02-125">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="09a02-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




