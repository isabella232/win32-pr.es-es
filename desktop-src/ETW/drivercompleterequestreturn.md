---
description: Esta clase es la clase de tipo de evento para los eventos de devolución de solicitud de finalización de controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Clase DriverCompleteRequestReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540366"
---
# <a name="drivercompleterequestreturn-class"></a><span data-ttu-id="83f56-104">Clase DriverCompleteRequestReturn</span><span class="sxs-lookup"><span data-stu-id="83f56-104">DriverCompleteRequestReturn class</span></span>

<span data-ttu-id="83f56-105">Esta clase es la clase de tipo de evento para los eventos de devolución de solicitud de finalización de controlador.</span><span class="sxs-lookup"><span data-stu-id="83f56-105">This class is the event type class for driver complete request return events.</span></span>

<span data-ttu-id="83f56-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="83f56-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83f56-107">Syntax</span></span>

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="83f56-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="83f56-108">Members</span></span>

<span data-ttu-id="83f56-109">La clase **DriverCompleteRequestReturn** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="83f56-109">The **DriverCompleteRequestReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="83f56-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83f56-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83f56-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83f56-111">Properties</span></span>

<span data-ttu-id="83f56-112">La clase **DriverCompleteRequestReturn** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="83f56-112">The **DriverCompleteRequestReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83f56-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="83f56-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f56-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83f56-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83f56-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83f56-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83f56-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="83f56-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="83f56-117">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="83f56-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="83f56-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="83f56-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f56-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83f56-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83f56-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="83f56-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83f56-121">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="83f56-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="83f56-122">Identificador que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f56-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="83f56-123">Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="83f56-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83f56-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83f56-124">Requirements</span></span>



| <span data-ttu-id="83f56-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83f56-125">Requirement</span></span> | <span data-ttu-id="83f56-126">Value</span><span class="sxs-lookup"><span data-stu-id="83f56-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83f56-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83f56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83f56-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83f56-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83f56-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83f56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83f56-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="83f56-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83f56-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="83f56-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f56-132">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="83f56-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




