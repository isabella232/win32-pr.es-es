---
description: Esta clase es la clase de tipo de evento para eventos de fin de espera de ALPC. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542766"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="ac03b-104">ALPC ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="ac03b-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="ac03b-105">Esta clase es la clase de tipo de evento para eventos de fin de espera de ALPC.</span><span class="sxs-lookup"><span data-stu-id="ac03b-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="ac03b-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="ac03b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac03b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac03b-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="ac03b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac03b-108">Members</span></span>

<span data-ttu-id="ac03b-109">La clase **ALPC \_ unwait** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ac03b-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="ac03b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac03b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac03b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac03b-111">Properties</span></span>

<span data-ttu-id="ac03b-112">La clase **ALPC \_ unwait** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ac03b-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac03b-113">**Estado**</span><span class="sxs-lookup"><span data-stu-id="ac03b-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac03b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac03b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac03b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac03b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac03b-116">Estado de la operación de espera.</span><span class="sxs-lookup"><span data-stu-id="ac03b-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac03b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac03b-117">Requirements</span></span>



| <span data-ttu-id="ac03b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac03b-118">Requirement</span></span> | <span data-ttu-id="ac03b-119">Value</span><span class="sxs-lookup"><span data-stu-id="ac03b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac03b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac03b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac03b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac03b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac03b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac03b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac03b-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac03b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




