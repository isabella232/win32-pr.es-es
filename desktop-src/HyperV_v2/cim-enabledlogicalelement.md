---
description: Representa un elemento lógico que se puede habilitar y deshabilitar.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: CIM_EnabledLogicalElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687651"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="8eff1-103">\_Clase EnabledLogicalElement de CIM</span><span class="sxs-lookup"><span data-stu-id="8eff1-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="8eff1-104">Representa un elemento lógico que se puede habilitar y deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="8eff1-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8eff1-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="8eff1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8eff1-106">Members</span></span>

<span data-ttu-id="8eff1-107">La clase **CIM \_ EnabledLogicalElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8eff1-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="8eff1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8eff1-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="8eff1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8eff1-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8eff1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8eff1-110">Methods</span></span>

<span data-ttu-id="8eff1-111">La clase **CIM \_ EnabledLogicalElement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8eff1-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="8eff1-112">Método</span><span class="sxs-lookup"><span data-stu-id="8eff1-112">Method</span></span>                                                                     | <span data-ttu-id="8eff1-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8eff1-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8eff1-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8eff1-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="8eff1-115">Solicita que el estado del elemento se cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8eff1-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8eff1-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8eff1-116">Properties</span></span>

<span data-ttu-id="8eff1-117">La clase **CIM \_ EnabledLogicalElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8eff1-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8eff1-118">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8eff1-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-119">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff1-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-121">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","[**\_ EnabledLogicalElementCapabilities CIM**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span><span class="sxs-lookup"><span data-stu-id="8eff1-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-122">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="8eff1-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="8eff1-123">Los valores de la lista deben ser un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia de **\_ EnabledLogicalElementCapabilities de CIM** asociada.</span><span class="sxs-lookup"><span data-stu-id="8eff1-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="8eff1-124">Esta propiedad es **null** si la implementación no puede determinar el conjunto de valores posibles para el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="8eff1-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8eff1-125">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff1-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8eff1-126">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff1-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8eff1-127">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff1-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8eff1-128">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff1-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8eff1-129">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff1-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8eff1-130">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="8eff1-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8eff1-131">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff1-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8eff1-132">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="8eff1-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8eff1-133">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="8eff1-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8eff1-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8eff1-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8eff1-135">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8eff1-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff1-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8eff1-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-138">Indica la configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8eff1-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8eff1-139">El valor predeterminado **está habilitado** (2).</span><span class="sxs-lookup"><span data-stu-id="8eff1-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8eff1-140">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff1-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8eff1-141">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff1-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8eff1-142">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff1-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="8eff1-143">**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff1-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="8eff1-144">**No tiene valor predeterminado** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff1-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8eff1-145">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff1-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8eff1-146">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8eff1-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8eff1-147">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8eff1-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8eff1-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8eff1-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff1-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-151">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**OtherEnabledState**")</span><span class="sxs-lookup"><span data-stu-id="8eff1-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-152">Indica el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8eff1-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="8eff1-153">Entre los valores posibles se incluyen las transiciones entre Estados.</span><span class="sxs-lookup"><span data-stu-id="8eff1-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="8eff1-154">Por ejemplo, **apagar** (4) e **iniciar** (10) son Estados transitorios entre **habilitado** y **deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="8eff1-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8eff1-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff1-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8eff1-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8eff1-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8eff1-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff1-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-158">El elemento es o puede ejecutar comandos, procesará cualquier comando en cola y pondrá en cola nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="8eff1-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8eff1-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff1-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-160">el elemento no ejecutará comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="8eff1-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="8eff1-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff1-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-162">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8eff1-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8eff1-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff1-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-164">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="8eff1-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="8eff1-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff1-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-166">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="8eff1-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8eff1-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff1-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-168">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="8eff1-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="8eff1-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="8eff1-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-170">Es posible que el elemento esté completando comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="8eff1-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8eff1-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff1-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-172">Que el elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="8eff1-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8eff1-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (10)</span><span class="sxs-lookup"><span data-stu-id="8eff1-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-174">El elemento está en proceso de pasar a un estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="8eff1-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="8eff1-175">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="8eff1-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8eff1-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8eff1-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8eff1-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8eff1-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8eff1-178">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8eff1-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8eff1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-181">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="8eff1-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-182">Describe el estado del elemento cuando el valor de la propiedad **EnabledState** es **otro**.</span><span class="sxs-lookup"><span data-stu-id="8eff1-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="8eff1-183">Esta propiedad debe establecerse en **null** cuando **EnabledState** no es **otro**.</span><span class="sxs-lookup"><span data-stu-id="8eff1-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="8eff1-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8eff1-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff1-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-187">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="8eff1-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-188">Indica el último estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="8eff1-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="8eff1-189">La propiedad **EnabledState** indica el estado actual.</span><span class="sxs-lookup"><span data-stu-id="8eff1-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="8eff1-190">Esta propiedad permite comparar el último estado solicitado y el actual.</span><span class="sxs-lookup"><span data-stu-id="8eff1-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="8eff1-191">Cuando el valor de la propiedad **EnabledState** **no es aplicable**, esta propiedad no tiene ningún significado.</span><span class="sxs-lookup"><span data-stu-id="8eff1-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8eff1-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff1-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-193">Se desconoce el último estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="8eff1-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8eff1-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff1-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8eff1-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff1-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-196">Solicita una deshabilitación inmediata del elemento, de modo que no se ejecute ni acepte ningún comando o procesamiento de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="8eff1-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8eff1-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff1-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-198">Solicita una transición ordenada al Estado deshabilitado y puede implicar la eliminación de energía para borrar completamente cualquier estado existente.</span><span class="sxs-lookup"><span data-stu-id="8eff1-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="8eff1-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Sin cambios** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff1-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-200">Desusado en lugar de indicar que el último estado solicitado es "Unknown" (0).</span><span class="sxs-lookup"><span data-stu-id="8eff1-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="8eff1-201">Si el último estado solicitado o deseado es desconocido, **RequestedState** debe tener el valor "Unknown" (0), pero puede tener el valor "no Change" (5).</span><span class="sxs-lookup"><span data-stu-id="8eff1-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8eff1-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff1-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-203">Se ha solicitado al elemento la transición a los **EnabledState** habilitado pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8eff1-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8eff1-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff1-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="8eff1-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="8eff1-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8eff1-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff1-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8eff1-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="8eff1-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-208">Hace referencia a "apagar" y, a continuación, a un estado "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8eff1-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8eff1-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="8eff1-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8eff1-210">Indica que el elemento está primero "deshabilitado" y, a continuación, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8eff1-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8eff1-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (12)</span><span class="sxs-lookup"><span data-stu-id="8eff1-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8eff1-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8eff1-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8eff1-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8eff1-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8eff1-214">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8eff1-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-215">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8eff1-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-217">Indica que el elemento ha cambiado el estado por última vez.</span><span class="sxs-lookup"><span data-stu-id="8eff1-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="8eff1-218">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo cero.</span><span class="sxs-lookup"><span data-stu-id="8eff1-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="8eff1-219">Si se solicitó un cambio de estado, pero se rechazó o aún no se ha procesado, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="8eff1-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="8eff1-220">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8eff1-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eff1-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eff1-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eff1-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eff1-223">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElement**.**RequestStateChange**","**\_ EnabledLogicalElement CIM**.**RequestedState**","**CIM \_ EnabledLogicalElement**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="8eff1-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="8eff1-224">Indica el estado de destino en el que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="8eff1-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="8eff1-225">Un valor **sin cambios** indica que no hay ninguna transición en curso.</span><span class="sxs-lookup"><span data-stu-id="8eff1-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="8eff1-226">Un valor de **no aplicable** indica que la implementación no informa de las transiciones en curso.</span><span class="sxs-lookup"><span data-stu-id="8eff1-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8eff1-227">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8eff1-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8eff1-228">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8eff1-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8eff1-229">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8eff1-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8eff1-230">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="8eff1-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="8eff1-231">**Sin cambios** (5)</span><span class="sxs-lookup"><span data-stu-id="8eff1-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8eff1-232">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="8eff1-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8eff1-233">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="8eff1-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8eff1-234">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="8eff1-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8eff1-235">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="8eff1-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8eff1-236">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="8eff1-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8eff1-237">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="8eff1-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8eff1-238">**No aplicable** (12)</span><span class="sxs-lookup"><span data-stu-id="8eff1-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8eff1-239">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8eff1-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="8eff1-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8eff1-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8eff1-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eff1-241">Requirements</span></span>



| <span data-ttu-id="8eff1-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eff1-242">Requirement</span></span> | <span data-ttu-id="8eff1-243">Value</span><span class="sxs-lookup"><span data-stu-id="8eff1-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff1-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eff1-244">Minimum supported client</span></span><br/> | <span data-ttu-id="8eff1-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8eff1-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8eff1-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eff1-246">Minimum supported server</span></span><br/> | <span data-ttu-id="8eff1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8eff1-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8eff1-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8eff1-248">Namespace</span></span><br/>                | <span data-ttu-id="8eff1-249">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8eff1-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8eff1-250">MOF</span><span class="sxs-lookup"><span data-stu-id="8eff1-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eff1-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eff1-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eff1-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8eff1-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eff1-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8eff1-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8eff1-254">Vea también</span><span class="sxs-lookup"><span data-stu-id="8eff1-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eff1-255">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8eff1-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

