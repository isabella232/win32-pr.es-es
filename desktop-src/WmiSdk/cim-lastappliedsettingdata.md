---
description: Asociación entre un objeto y otro objeto que se le ha aplicado.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: CIM_LastAppliedSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718635"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="fd940-103">\_Clase LastAppliedSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="fd940-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="fd940-104">Asociación entre un objeto y otro objeto que se le ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="fd940-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd940-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd940-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd940-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd940-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd940-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fd940-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd940-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd940-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="fd940-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd940-109">Members</span></span>

<span data-ttu-id="fd940-110">La clase **CIM \_ LastAppliedSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd940-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fd940-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd940-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd940-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd940-112">Properties</span></span>

<span data-ttu-id="fd940-113">La clase **CIM \_ LastAppliedSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd940-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd940-114">**AppliedObject**</span><span class="sxs-lookup"><span data-stu-id="fd940-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd940-115">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fd940-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fd940-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd940-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd940-117">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fd940-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fd940-118">Objeto que se aplicó al objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fd940-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="fd940-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="fd940-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd940-120">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fd940-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fd940-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd940-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd940-122">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fd940-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fd940-123">Objeto que era el destino de la aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd940-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd940-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd940-124">Requirements</span></span>



| <span data-ttu-id="fd940-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd940-125">Requirement</span></span> | <span data-ttu-id="fd940-126">Value</span><span class="sxs-lookup"><span data-stu-id="fd940-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="fd940-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd940-127">Namespace</span></span><br/> | <span data-ttu-id="fd940-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fd940-128">Root\\CIMV2</span></span><br/> |



 

 




