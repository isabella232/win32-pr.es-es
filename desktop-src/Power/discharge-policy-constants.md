---
description: En la lista siguiente se describen las constantes de la Directiva de descargas.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de la Directiva de descarga (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667220"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="eccb1-103">Constantes de la Directiva de descarga</span><span class="sxs-lookup"><span data-stu-id="eccb1-103">Discharge Policy Constants</span></span>

<span data-ttu-id="eccb1-104">En la lista siguiente se describen las constantes de la Directiva de descargas.</span><span class="sxs-lookup"><span data-stu-id="eccb1-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="eccb1-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="eccb1-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="eccb1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="eccb1-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="eccb1-107"><dt>**Descarga \_ de DIRECTIVA \_ crítica**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eccb1-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="eccb1-108">La configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) se usa cuando la batería se carga por debajo del umbral crítico.</span><span class="sxs-lookup"><span data-stu-id="eccb1-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="eccb1-109"><dt>**Descarga \_ de DIRECTIVA \_ baja**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eccb1-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="eccb1-110">La configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) se usa cuando la batería se carga por debajo del umbral inferior.</span><span class="sxs-lookup"><span data-stu-id="eccb1-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="eccb1-111"><dt>**Número \_ de \_Directivas de descarga**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eccb1-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="eccb1-112">Número de opciones de configuración de la Directiva de descarga de la batería (estructuras de [**\_ \_ nivel de energía del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) especificadas.</span><span class="sxs-lookup"><span data-stu-id="eccb1-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="eccb1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eccb1-113">Requirements</span></span>



| <span data-ttu-id="eccb1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eccb1-114">Requirement</span></span> | <span data-ttu-id="eccb1-115">Value</span><span class="sxs-lookup"><span data-stu-id="eccb1-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eccb1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccb1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eccb1-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="eccb1-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eccb1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eccb1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eccb1-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eccb1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="eccb1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eccb1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eccb1-121"><dt>Winnt. h (incluye Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eccb1-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




