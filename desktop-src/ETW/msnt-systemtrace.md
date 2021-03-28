---
description: Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984570"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="1c9d6-104">MSNT \_ SystemTrace (clase)</span><span class="sxs-lookup"><span data-stu-id="1c9d6-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="1c9d6-105">Clase primaria de la que se derivan todas las clases de seguimiento de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="1c9d6-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="1c9d6-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="1c9d6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c9d6-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="1c9d6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c9d6-108">Members</span></span>

<span data-ttu-id="1c9d6-109">La clase **MSNT \_ SystemTrace** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1c9d6-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="1c9d6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c9d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c9d6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c9d6-111">Properties</span></span>

<span data-ttu-id="1c9d6-112">La clase **MSNT \_ SystemTrace** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c9d6-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c9d6-113">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="1c9d6-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c9d6-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c9d6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c9d6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c9d6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c9d6-116">Calificadores: **DefineValues {" \_ \_ \_ proceso de marca de seguimiento de eventos", " \_ \_ \_ subproceso de marca de seguimiento de eventos", " \_ carga de imagen de \_ marca de seguimiento de eventos \_ \_ ", " \_ \_ \_ \_ contadores de proceso de marca de seguimiento de eventos", "marca de seguimiento de eventos \_ \_ \_ CSWITCH", "marca de seguimiento de eventos \_ \_ \_ DPC", " \_ \_ interrupción de la marca \_ de seguimiento marca de seguimiento de \_ \_ \_ eventos \_ \_ \_ \_ e e/s de disco", "marca de seguimiento de eventos \_ \_ \_ \_ \_ e/s de archivo de disco", "marca de seguimiento de eventos \_ \_ \_ \_ de e/s de disco \_ ", " \_ distribuidor de marcas de seguimiento de eventos", "errores de página de la marca de seguimiento de eventos", "error de la memoria de la marca de seguimiento de eventos \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ " \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ registro de marca de seguimiento de eventos "," marca de seguimiento de eventos \_ \_ \_ ALPC "," marca de seguimiento de evento \_ \_ \_ Split \_ IO "," \_ controlador de marca de seguimiento de eventos \_ \_ "," \_ \_ Perfil de marca de seguimiento de eventos \_ "," \_ \_ \_ \_ e/s de archivo de marca de seguimiento de eventos "," seguimiento de eventos \_ marcas de \_ \_ e/s de archivo de marca \_ \_ "}**, **ValueMap {" 0x00000001 "," 0x00000002 "," 0x00000004 "," 0x00000008 "," 0x00000010 "," 0x00000020 "," 0x00000040 "," 0x00000080 "," 0x00000100 " , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span><span class="sxs-lookup"><span data-stu-id="1c9d6-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="1c9d6-117">Habilita la marca que indica los proveedores de kernel habilitados.</span><span class="sxs-lookup"><span data-stu-id="1c9d6-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c9d6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c9d6-118">Requirements</span></span>



| <span data-ttu-id="1c9d6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c9d6-119">Requirement</span></span> | <span data-ttu-id="1c9d6-120">Value</span><span class="sxs-lookup"><span data-stu-id="1c9d6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c9d6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c9d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9d6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1c9d6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c9d6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c9d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9d6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1c9d6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




