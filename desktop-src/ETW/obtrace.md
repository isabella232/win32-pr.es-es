---
description: Representa la clase primaria de la que se derivan todas las clases de seguimiento de eventos del administrador de objetos.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Clase ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815238"
---
# <a name="obtrace-class"></a><span data-ttu-id="87040-103">Clase ObTrace</span><span class="sxs-lookup"><span data-stu-id="87040-103">ObTrace class</span></span>

<span data-ttu-id="87040-104">Representa la clase primaria de la que se derivan todas las clases de seguimiento de eventos del administrador de objetos.</span><span class="sxs-lookup"><span data-stu-id="87040-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="87040-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="87040-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87040-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87040-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="87040-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="87040-107">Members</span></span>

<span data-ttu-id="87040-108">La clase **ObTrace** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="87040-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="87040-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87040-109">Remarks</span></span>

<span data-ttu-id="87040-110">Para habilitar el seguimiento de eventos del administrador de objetos, llame a la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) con el parámetro *InformationClass* igual al valor de enumeración de la [**clase de \_ información \_ de seguimiento**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** y el miembro **EnableFlags** de la estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) es igual al **identificador de rendimiento \_ OB \_** (0x80000040).</span><span class="sxs-lookup"><span data-stu-id="87040-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="87040-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87040-111">Requirements</span></span>



| <span data-ttu-id="87040-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="87040-112">Requirement</span></span> | <span data-ttu-id="87040-113">Value</span><span class="sxs-lookup"><span data-stu-id="87040-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87040-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87040-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87040-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="87040-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87040-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87040-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87040-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="87040-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87040-118">MOF</span><span class="sxs-lookup"><span data-stu-id="87040-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87040-119"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87040-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
