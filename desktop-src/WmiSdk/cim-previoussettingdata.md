---
description: Asociación entre un sistema virtual y los datos de configuración de la instantánea que es el primario del sistema virtual.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708708"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="60f10-103">\_Clase PreviousSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="60f10-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="60f10-104">Asociación entre un sistema virtual y los datos de configuración de la instantánea que es el primario del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="60f10-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60f10-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="60f10-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60f10-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60f10-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60f10-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="60f10-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60f10-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="60f10-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="60f10-109">Members</span></span>

<span data-ttu-id="60f10-110">La clase **CIM \_ PreviousSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60f10-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="60f10-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60f10-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60f10-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60f10-112">Properties</span></span>

<span data-ttu-id="60f10-113">La clase **CIM \_ PreviousSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60f10-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60f10-114">**PreviousObject**</span><span class="sxs-lookup"><span data-stu-id="60f10-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60f10-115">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="60f10-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="60f10-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60f10-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60f10-117">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="60f10-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="60f10-118">Los datos de configuración de la instantánea que son el principal de este equipo.</span><span class="sxs-lookup"><span data-stu-id="60f10-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="60f10-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="60f10-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60f10-120">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="60f10-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="60f10-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60f10-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60f10-122">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="60f10-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="60f10-123">Sistema del equipo que era el destino de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60f10-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60f10-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60f10-124">Requirements</span></span>



| <span data-ttu-id="60f10-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="60f10-125">Requirement</span></span> | <span data-ttu-id="60f10-126">Value</span><span class="sxs-lookup"><span data-stu-id="60f10-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="60f10-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60f10-127">Namespace</span></span><br/> | <span data-ttu-id="60f10-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="60f10-128">Root\\CIMV2</span></span><br/> |



 

 




