---
description: Esta clase es la clase de tipo de evento para los eventos de devolución de llamada de función principal del controlador. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Clase DriverMajorFunctionReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540358"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="cb87d-104">Clase DriverMajorFunctionReturn</span><span class="sxs-lookup"><span data-stu-id="cb87d-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="cb87d-105">Esta clase es la clase de tipo de evento para los eventos de devolución de llamada de función principal del controlador.</span><span class="sxs-lookup"><span data-stu-id="cb87d-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="cb87d-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="cb87d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb87d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb87d-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="cb87d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb87d-108">Members</span></span>

<span data-ttu-id="cb87d-109">La clase **DriverMajorFunctionReturn** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb87d-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="cb87d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb87d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb87d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb87d-111">Properties</span></span>

<span data-ttu-id="cb87d-112">La clase **DriverMajorFunctionReturn** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb87d-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb87d-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="cb87d-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb87d-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb87d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb87d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb87d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb87d-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="cb87d-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cb87d-117">Paquete de solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="cb87d-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="cb87d-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="cb87d-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb87d-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb87d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb87d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb87d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb87d-121">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="cb87d-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cb87d-122">Identificador que identifica de forma única la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb87d-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="cb87d-123">Use este identificador para correlacionar con los otros eventos del controlador, por ejemplo, el evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="cb87d-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb87d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb87d-124">Requirements</span></span>



| <span data-ttu-id="cb87d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb87d-125">Requirement</span></span> | <span data-ttu-id="cb87d-126">Value</span><span class="sxs-lookup"><span data-stu-id="cb87d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb87d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb87d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb87d-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb87d-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb87d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb87d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb87d-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb87d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb87d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb87d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb87d-132">**Desmontaje**</span><span class="sxs-lookup"><span data-stu-id="cb87d-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




