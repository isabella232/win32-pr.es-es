---
description: Describe las restricciones de las propiedades de un objeto EnabledLogicalElement de CIM asociado \_ .
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667570"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="79697-103">\_Clase EnabledLogicalElementCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="79697-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="79697-104">Describe las restricciones de las propiedades de un objeto [**\_ EnabledLogicalElement de CIM**](cim-enabledlogicalelement.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="79697-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79697-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79697-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="79697-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="79697-106">Members</span></span>

<span data-ttu-id="79697-107">La clase **CIM \_ EnabledLogicalElementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79697-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="79697-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79697-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79697-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79697-109">Properties</span></span>

<span data-ttu-id="79697-110">La clase **CIM \_ EnabledLogicalElementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79697-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79697-111">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="79697-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79697-112">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79697-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79697-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79697-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79697-114">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCITS-T11 \| swapi \_ unidad \_ config \_ Cap \_ T \| EditName "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md).**ElementName**")</span><span class="sxs-lookup"><span data-stu-id="79697-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="79697-115">**true** si se puede modificar la propiedad **ElementName** del elemento lógico habilitado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="79697-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79697-116">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="79697-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79697-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79697-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79697-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79697-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79697-119">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span><span class="sxs-lookup"><span data-stu-id="79697-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="79697-120">Una expresión regular que indica las restricciones en la propiedad **ElementName** del elemento lógico enable.</span><span class="sxs-lookup"><span data-stu-id="79697-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="79697-121">Consulte *DMTF Standard ABNF con la guía de uso de especificación de Perfil de administración*, Apéndice C para ver la sintaxis permitida.</span><span class="sxs-lookup"><span data-stu-id="79697-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="79697-122">Si esta propiedad y la propiedad **ElementNameMask** del elemento lógico enable describen la longitud máxima de **ElementName**, se usa el valor menor.</span><span class="sxs-lookup"><span data-stu-id="79697-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="79697-123">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="79697-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79697-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79697-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79697-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79697-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79697-126">Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCITS-T11 \| swapi \_ unidad \_ config \_ Cap \_ T \| MaxNameChars "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ FCSwitchCapabilities. ElementNameEditSupported ","**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")</span><span class="sxs-lookup"><span data-stu-id="79697-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="79697-127">Longitud máxima admitida de la propiedad **ElementName** del elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="79697-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="79697-128">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="79697-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79697-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79697-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79697-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79697-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79697-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span><span class="sxs-lookup"><span data-stu-id="79697-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="79697-132">Los Estados posibles que se pueden solicitar en el elemento lógico habilitado mediante el método [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="79697-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79697-133">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="79697-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79697-134">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79697-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="79697-135">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="79697-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="79697-136">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="79697-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="79697-137">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="79697-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="79697-138">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="79697-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="79697-139">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="79697-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="79697-140">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="79697-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="79697-141">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="79697-141">**Reset** (11)</span></span>


<span data-ttu-id="79697-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79697-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="79697-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79697-143">Requirements</span></span>



| <span data-ttu-id="79697-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="79697-144">Requirement</span></span> | <span data-ttu-id="79697-145">Value</span><span class="sxs-lookup"><span data-stu-id="79697-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79697-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79697-146">Minimum supported client</span></span><br/> | <span data-ttu-id="79697-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="79697-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="79697-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79697-148">Minimum supported server</span></span><br/> | <span data-ttu-id="79697-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79697-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="79697-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79697-150">Namespace</span></span><br/>                | <span data-ttu-id="79697-151">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="79697-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79697-152">MOF</span><span class="sxs-lookup"><span data-stu-id="79697-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79697-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79697-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79697-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79697-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79697-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79697-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79697-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="79697-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79697-157">**Capacidades de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="79697-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

