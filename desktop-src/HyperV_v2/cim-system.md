---
description: Representa un conjunto de componentes que funcionan como una única entidad de nivel superior.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: CIM_System (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666911"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="973b6-103">CIM_System (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="973b6-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="973b6-104">Representa un conjunto de componentes que funcionan como una única entidad de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="973b6-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="973b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="973b6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="973b6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="973b6-106">Members</span></span>

<span data-ttu-id="973b6-107">La **clase \_ del sistema CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="973b6-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="973b6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="973b6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="973b6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="973b6-109">Properties</span></span>

<span data-ttu-id="973b6-110">La **clase \_ del sistema CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="973b6-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="973b6-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="973b6-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="973b6-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="973b6-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="973b6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="973b6-114">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="973b6-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="973b6-115">Nombre de clase utilizado para crear una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="973b6-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="973b6-116">**CreationClassName** se combina con otras propiedades de clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="973b6-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="973b6-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="973b6-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="973b6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="973b6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="973b6-120">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ Sistema CIM**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="973b6-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="973b6-121">Una matriz que contiene descripciones de los valores de la propiedad **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="973b6-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="973b6-122">Los elementos de la matriz de **IdentifyingDescriptions** se corresponden con los elementos de la propiedad **IdentifyingDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="973b6-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-123">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="973b6-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="973b6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="973b6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="973b6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="973b6-126">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="973b6-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="973b6-127">La clave de esta instancia en un entorno empresarial.</span><span class="sxs-lookup"><span data-stu-id="973b6-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="973b6-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="973b6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="973b6-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="973b6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="973b6-131">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="973b6-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="973b6-132">La Convención de nomenclatura utilizada por la propiedad Name para asegurarse de que los valores de **nombre** son únicos.</span><span class="sxs-lookup"><span data-stu-id="973b6-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="973b6-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-134">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="973b6-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="973b6-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="973b6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="973b6-136">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ Sistema CIM**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="973b6-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="973b6-137">Una matriz que contiene un conjunto de datos adicionales, más allá de la información del nombre del sistema, que se puede usar para identificar un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="973b6-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="973b6-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="973b6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="973b6-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="973b6-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="973b6-141">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="973b6-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="973b6-142">Una cadena que proporciona información sobre cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="973b6-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="973b6-143">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="973b6-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="973b6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="973b6-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="973b6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="973b6-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="973b6-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="973b6-147">Nombre del usuario primario del sistema.</span><span class="sxs-lookup"><span data-stu-id="973b6-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="973b6-148">**Roles**</span><span class="sxs-lookup"><span data-stu-id="973b6-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="973b6-149">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="973b6-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="973b6-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="973b6-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="973b6-151">Una matriz que contiene los roles que realiza el sistema en un entorno empresarial.</span><span class="sxs-lookup"><span data-stu-id="973b6-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="973b6-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="973b6-152">Requirements</span></span>



| <span data-ttu-id="973b6-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="973b6-153">Requirement</span></span> | <span data-ttu-id="973b6-154">Value</span><span class="sxs-lookup"><span data-stu-id="973b6-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="973b6-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="973b6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="973b6-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="973b6-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="973b6-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="973b6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="973b6-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="973b6-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="973b6-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="973b6-159">Namespace</span></span><br/>                | <span data-ttu-id="973b6-160">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="973b6-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="973b6-161">MOF</span><span class="sxs-lookup"><span data-stu-id="973b6-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="973b6-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="973b6-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="973b6-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="973b6-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="973b6-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="973b6-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="973b6-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="973b6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="973b6-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="973b6-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

