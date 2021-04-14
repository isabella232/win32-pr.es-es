---
description: Esta clase es la clase de tipo de evento para los eventos de salida de la llamada del sistema. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Clase SysCallExit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985698"
---
# <a name="syscallexit-class"></a><span data-ttu-id="71c98-104">Clase SysCallExit</span><span class="sxs-lookup"><span data-stu-id="71c98-104">SysCallExit class</span></span>

<span data-ttu-id="71c98-105">Esta clase es la clase de tipo de evento para los eventos de salida de la llamada del sistema.</span><span class="sxs-lookup"><span data-stu-id="71c98-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="71c98-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="71c98-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71c98-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="71c98-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="71c98-108">Members</span></span>

<span data-ttu-id="71c98-109">La clase **SysCallExit** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="71c98-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="71c98-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71c98-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71c98-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71c98-111">Properties</span></span>

<span data-ttu-id="71c98-112">La clase **SysCallExit** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="71c98-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71c98-113">**SysCallNtStatus**</span><span class="sxs-lookup"><span data-stu-id="71c98-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71c98-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71c98-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71c98-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="71c98-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71c98-116">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="71c98-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="71c98-117">Código de estado devuelto por la llamada del sistema NT.</span><span class="sxs-lookup"><span data-stu-id="71c98-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71c98-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71c98-118">Requirements</span></span>



| <span data-ttu-id="71c98-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71c98-119">Requirement</span></span> | <span data-ttu-id="71c98-120">Value</span><span class="sxs-lookup"><span data-stu-id="71c98-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71c98-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71c98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71c98-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71c98-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71c98-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71c98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71c98-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71c98-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




