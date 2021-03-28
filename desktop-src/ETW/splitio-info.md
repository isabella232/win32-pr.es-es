---
description: Esta clase es la clase de tipo de evento para los eventos de e/s divididos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912598"
---
# <a name="splitio_info-class"></a><span data-ttu-id="e2113-104">Clase de información de SplitIo \_</span><span class="sxs-lookup"><span data-stu-id="e2113-104">SplitIo\_Info class</span></span>

<span data-ttu-id="e2113-105">Esta clase es la clase de tipo de evento para los eventos de e/s divididos.</span><span class="sxs-lookup"><span data-stu-id="e2113-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="e2113-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="e2113-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2113-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2113-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="e2113-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2113-108">Members</span></span>

<span data-ttu-id="e2113-109">La clase de **\_ información SplitIo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e2113-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="e2113-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2113-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2113-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2113-111">Properties</span></span>

<span data-ttu-id="e2113-112">La clase de **\_ información SplitIo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2113-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2113-113">**ChildIrp**</span><span class="sxs-lookup"><span data-stu-id="e2113-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2113-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2113-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2113-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2113-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2113-116">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="e2113-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e2113-117">Paquete de solicitud de e/s secundaria.</span><span class="sxs-lookup"><span data-stu-id="e2113-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="e2113-118">**ParentIrp**</span><span class="sxs-lookup"><span data-stu-id="e2113-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2113-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2113-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2113-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2113-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2113-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="e2113-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e2113-122">Paquete de solicitud de e/s primaria.</span><span class="sxs-lookup"><span data-stu-id="e2113-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2113-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2113-123">Remarks</span></span>

<span data-ttu-id="e2113-124">Indica que el administrador de volúmenes dividió el IRP en dos IRP.</span><span class="sxs-lookup"><span data-stu-id="e2113-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2113-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2113-125">Requirements</span></span>



| <span data-ttu-id="e2113-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2113-126">Requirement</span></span> | <span data-ttu-id="e2113-127">Value</span><span class="sxs-lookup"><span data-stu-id="e2113-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2113-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2113-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2113-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2113-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2113-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2113-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2113-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2113-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




