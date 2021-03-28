---
description: Esta clase es la clase de tipo de evento para la llamada del sistema Enter Events. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Clase SysCallEnter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985699"
---
# <a name="syscallenter-class"></a><span data-ttu-id="47764-104">Clase SysCallEnter</span><span class="sxs-lookup"><span data-stu-id="47764-104">SysCallEnter class</span></span>

<span data-ttu-id="47764-105">Esta clase es la clase de tipo de evento para la llamada del sistema Enter Events.</span><span class="sxs-lookup"><span data-stu-id="47764-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="47764-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="47764-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47764-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47764-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="47764-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="47764-108">Members</span></span>

<span data-ttu-id="47764-109">La clase **SysCallEnter** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47764-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="47764-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47764-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47764-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47764-111">Properties</span></span>

<span data-ttu-id="47764-112">La clase **SysCallEnter** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47764-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47764-113">**SysCallAddress**</span><span class="sxs-lookup"><span data-stu-id="47764-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47764-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47764-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47764-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47764-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47764-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="47764-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="47764-117">Dirección de la llamada de función NT que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="47764-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47764-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47764-118">Requirements</span></span>



| <span data-ttu-id="47764-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="47764-119">Requirement</span></span> | <span data-ttu-id="47764-120">Value</span><span class="sxs-lookup"><span data-stu-id="47764-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47764-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47764-121">Minimum supported client</span></span><br/> | <span data-ttu-id="47764-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="47764-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47764-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47764-123">Minimum supported server</span></span><br/> | <span data-ttu-id="47764-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="47764-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




