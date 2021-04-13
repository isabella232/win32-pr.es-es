---
description: La \_ clase de asociación CIM CollectedMSEs representa los miembros del objeto de agrupación, una clase CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496409"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="b8d68-103">CIM_CollectedMSEs (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b8d68-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b8d68-104">La clase de asociación **CIM \_ CollectedMSEs** representa los miembros del objeto de agrupación, una clase [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d68-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8d68-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b8d68-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8d68-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8d68-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8d68-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8d68-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b8d68-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b8d68-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d68-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8d68-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="b8d68-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8d68-110">Members</span></span>

<span data-ttu-id="b8d68-111">La clase **CIM \_ CollectedMSEs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8d68-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="b8d68-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8d68-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8d68-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8d68-113">Properties</span></span>

<span data-ttu-id="b8d68-114">La clase **CIM \_ CollectedMSEs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8d68-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8d68-115">**Colección**</span><span class="sxs-lookup"><span data-stu-id="b8d68-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8d68-116">Tipo de datos: **cm \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="b8d68-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="b8d68-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8d68-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8d68-118">Referencia al objeto de agrupación o de contenedor que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="b8d68-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b8d68-119">**Member**</span><span class="sxs-lookup"><span data-stu-id="b8d68-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8d68-120">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="b8d68-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b8d68-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8d68-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8d68-122">Referencia a un miembro de la colección.</span><span class="sxs-lookup"><span data-stu-id="b8d68-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8d68-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8d68-123">Remarks</span></span>

<span data-ttu-id="b8d68-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8d68-124">WMI does not implement this class.</span></span> <span data-ttu-id="b8d68-125">Para obtener más información sobre las clases WMI derivadas de **CIM \_ CollectedMSEs**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b8d68-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b8d68-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8d68-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8d68-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b8d68-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d68-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d68-128">Requirements</span></span>



| <span data-ttu-id="b8d68-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d68-129">Requirement</span></span> | <span data-ttu-id="b8d68-130">Value</span><span class="sxs-lookup"><span data-stu-id="b8d68-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d68-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8d68-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d68-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8d68-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8d68-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8d68-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d68-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8d68-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8d68-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8d68-135">Namespace</span></span><br/>                | <span data-ttu-id="b8d68-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8d68-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8d68-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b8d68-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8d68-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8d68-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8d68-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8d68-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8d68-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d68-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




