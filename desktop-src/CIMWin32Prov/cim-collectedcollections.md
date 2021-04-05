---
description: La \_ clase CollectedCollections de CIM es una asociación de agregación que representa una colección de elementos del sistema administrados (MSE) contenidos en una colección de MSEs.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000667"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="73518-103">\_Clase CollectedCollections de CIM</span><span class="sxs-lookup"><span data-stu-id="73518-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="73518-104">La **clase \_ CollectedCollections de CIM** es una asociación de agregación que representa una colección de elementos del sistema administrados (MSE) contenidos en una colección de MSEs.</span><span class="sxs-lookup"><span data-stu-id="73518-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73518-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="73518-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="73518-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="73518-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="73518-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="73518-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="73518-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="73518-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73518-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73518-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="73518-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="73518-110">Members</span></span>

<span data-ttu-id="73518-111">La clase **CIM \_ CollectedCollections** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="73518-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="73518-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73518-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73518-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73518-113">Properties</span></span>

<span data-ttu-id="73518-114">La clase **CIM \_ CollectedCollections** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="73518-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73518-115">**Colección**</span><span class="sxs-lookup"><span data-stu-id="73518-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73518-116">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="73518-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="73518-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73518-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73518-118">Referencia al elemento primario o al "nivel superior" de la agregación.</span><span class="sxs-lookup"><span data-stu-id="73518-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="73518-119">**CollectionInCollection**</span><span class="sxs-lookup"><span data-stu-id="73518-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73518-120">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="73518-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="73518-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="73518-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73518-122">Referencia a la **colección**"recopilada".</span><span class="sxs-lookup"><span data-stu-id="73518-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73518-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73518-123">Remarks</span></span>

<span data-ttu-id="73518-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="73518-124">WMI does not implement this class.</span></span>

<span data-ttu-id="73518-125">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="73518-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="73518-126">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="73518-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="73518-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73518-127">Requirements</span></span>



| <span data-ttu-id="73518-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="73518-128">Requirement</span></span> | <span data-ttu-id="73518-129">Value</span><span class="sxs-lookup"><span data-stu-id="73518-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73518-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73518-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73518-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73518-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73518-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73518-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73518-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73518-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73518-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73518-134">Namespace</span></span><br/>                | <span data-ttu-id="73518-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="73518-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73518-136">MOF</span><span class="sxs-lookup"><span data-stu-id="73518-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73518-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73518-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73518-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73518-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73518-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73518-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




