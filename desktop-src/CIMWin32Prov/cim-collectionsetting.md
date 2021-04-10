---
description: La \_ clase CIM CollectionSetting representa la asociación entre un CIM \_ CollectionOfMSEs y la clase de configuración definida para ellos.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: CIM_CollectionSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907336"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="ab572-103">\_Clase CollectionSetting de CIM</span><span class="sxs-lookup"><span data-stu-id="ab572-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="ab572-104">La clase **CIM \_ CollectionSetting** representa la asociación entre un [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="ab572-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab572-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ab572-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab572-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ab572-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab572-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ab572-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab572-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ab572-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab572-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab572-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="ab572-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab572-110">Members</span></span>

<span data-ttu-id="ab572-111">La clase **CIM \_ CollectionSetting** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab572-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ab572-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab572-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab572-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab572-113">Properties</span></span>

<span data-ttu-id="ab572-114">La clase **CIM \_ CollectionSetting** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab572-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab572-115">**Colección**</span><span class="sxs-lookup"><span data-stu-id="ab572-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab572-116">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="ab572-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="ab572-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab572-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab572-118">Referencia a la clase [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="ab572-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ab572-119">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="ab572-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab572-120">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="ab572-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="ab572-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ab572-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab572-122">Referencia al objeto de **configuración** asociado a la propiedad de **colección** .</span><span class="sxs-lookup"><span data-stu-id="ab572-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab572-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab572-123">Remarks</span></span>

<span data-ttu-id="ab572-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ab572-124">WMI does not implement this class.</span></span> <span data-ttu-id="ab572-125">Para obtener más información sobre las clases WMI derivadas de **CIM \_ CollectionSetting**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ab572-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ab572-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab572-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab572-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ab572-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab572-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab572-128">Requirements</span></span>



| <span data-ttu-id="ab572-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab572-129">Requirement</span></span> | <span data-ttu-id="ab572-130">Value</span><span class="sxs-lookup"><span data-stu-id="ab572-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab572-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab572-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ab572-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab572-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab572-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab572-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ab572-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab572-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab572-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab572-135">Namespace</span></span><br/>                | <span data-ttu-id="ab572-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab572-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab572-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ab572-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab572-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab572-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab572-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab572-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab572-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab572-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




