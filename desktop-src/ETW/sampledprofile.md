---
description: Esta clase es la clase de tipo de evento para eventos de perfil muestreados. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Clase SampledProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985938"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="dbf08-104">Clase SampledProfile</span><span class="sxs-lookup"><span data-stu-id="dbf08-104">SampledProfile class</span></span>

<span data-ttu-id="dbf08-105">Esta clase es la clase de tipo de evento para eventos de perfil muestreados.</span><span class="sxs-lookup"><span data-stu-id="dbf08-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="dbf08-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="dbf08-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf08-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbf08-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="dbf08-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dbf08-108">Members</span></span>

<span data-ttu-id="dbf08-109">La clase **SampledProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dbf08-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="dbf08-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf08-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbf08-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf08-111">Properties</span></span>

<span data-ttu-id="dbf08-112">La clase **SampledProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dbf08-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbf08-113">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="dbf08-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf08-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbf08-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbf08-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="dbf08-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="dbf08-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dbf08-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbf08-118">**InstructionPointer**</span><span class="sxs-lookup"><span data-stu-id="dbf08-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf08-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbf08-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbf08-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-121">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="dbf08-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="dbf08-122">Dirección de la imagen que se estaba ejecutando en el momento en que se muestrea el procesador.</span><span class="sxs-lookup"><span data-stu-id="dbf08-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="dbf08-123">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="dbf08-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbf08-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbf08-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbf08-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbf08-126">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="dbf08-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="dbf08-127">Identificador de subproceso del subproceso que se estaba ejecutando en el momento en que se muestrea el procesador.</span><span class="sxs-lookup"><span data-stu-id="dbf08-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbf08-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbf08-128">Remarks</span></span>

<span data-ttu-id="dbf08-129">Estos eventos proporcionan un perfil de ejecución muestreado.</span><span class="sxs-lookup"><span data-stu-id="dbf08-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="dbf08-130">El evento registra lo que se estaba ejecutando en el procesador.</span><span class="sxs-lookup"><span data-stu-id="dbf08-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="dbf08-131">Puede usar los eventos de imagen para identificar el módulo binario que contiene esa instrucción.</span><span class="sxs-lookup"><span data-stu-id="dbf08-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="dbf08-132">Después, puede usar esta información para generar un perfil de ejecución mientras dure el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="dbf08-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf08-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbf08-133">Requirements</span></span>



| <span data-ttu-id="dbf08-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbf08-134">Requirement</span></span> | <span data-ttu-id="dbf08-135">Value</span><span class="sxs-lookup"><span data-stu-id="dbf08-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dbf08-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbf08-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf08-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dbf08-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dbf08-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbf08-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf08-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbf08-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




