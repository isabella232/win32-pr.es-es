---
description: La \_ clase CIM ProductFRU representa una asociación entre el producto y una unidad reemplazable en campo (FRU), que proporciona información acerca de los componentes de producto que se han reemplazado o se han sustituido.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: CIM_ProductFRU (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152931"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="6dd74-103">\_Clase ProductFRU de CIM</span><span class="sxs-lookup"><span data-stu-id="6dd74-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="6dd74-104">La clase **CIM \_ ProductFRU** representa una asociación entre el producto y una unidad reemplazable en campo (FRU), que proporciona información acerca de los componentes de producto que se han reemplazado o se han sustituido.</span><span class="sxs-lookup"><span data-stu-id="6dd74-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6dd74-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6dd74-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6dd74-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6dd74-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6dd74-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6dd74-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6dd74-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6dd74-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd74-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dd74-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="6dd74-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6dd74-110">Members</span></span>

<span data-ttu-id="6dd74-111">La clase **CIM \_ ProductFRU** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6dd74-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="6dd74-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6dd74-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dd74-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6dd74-113">Properties</span></span>

<span data-ttu-id="6dd74-114">La clase **CIM \_ ProductFRU** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6dd74-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dd74-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="6dd74-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd74-116">Tipo de datos **: \_ FRU de CIM**</span><span class="sxs-lookup"><span data-stu-id="6dd74-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="6dd74-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6dd74-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6dd74-118">Referencia a la FRU.</span><span class="sxs-lookup"><span data-stu-id="6dd74-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="6dd74-119">**Producto**</span><span class="sxs-lookup"><span data-stu-id="6dd74-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dd74-120">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="6dd74-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="6dd74-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6dd74-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dd74-122">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6dd74-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6dd74-123">Referencia al producto al que se aplica la FRU.</span><span class="sxs-lookup"><span data-stu-id="6dd74-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6dd74-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6dd74-124">Remarks</span></span>

<span data-ttu-id="6dd74-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6dd74-125">WMI does not implement this class.</span></span>

<span data-ttu-id="6dd74-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6dd74-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6dd74-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6dd74-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd74-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dd74-128">Requirements</span></span>



| <span data-ttu-id="6dd74-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd74-129">Requirement</span></span> | <span data-ttu-id="6dd74-130">Value</span><span class="sxs-lookup"><span data-stu-id="6dd74-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd74-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dd74-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd74-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dd74-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6dd74-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dd74-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd74-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dd74-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6dd74-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6dd74-135">Namespace</span></span><br/>                | <span data-ttu-id="6dd74-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6dd74-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6dd74-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6dd74-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dd74-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dd74-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dd74-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6dd74-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd74-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd74-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

