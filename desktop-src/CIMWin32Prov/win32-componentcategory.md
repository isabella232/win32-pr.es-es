---
description: La \_ clase WMI ComponentCategory de Win32 representa una categoría de componente.
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Win32_ComponentCategory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000728"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="9a8d6-103">\_Clase Win32 ComponentCategory</span><span class="sxs-lookup"><span data-stu-id="9a8d6-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="9a8d6-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComponentCategory de Win32** representa una categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="9a8d6-105">Las categorías de componentes son grupos de clases del modelo de objetos componentes (COM) con un conjunto de funcionalidades definido compartido entre ellas.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="9a8d6-106">Un cliente que usa estas interfaces consulta el registro para el título de categoría y el identificador único denominado **CategoryID**, que se crea a partir de un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="9a8d6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9a8d6-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8d6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a8d6-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="9a8d6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a8d6-110">Members</span></span>

<span data-ttu-id="9a8d6-111">La **clase \_ ComponentCategory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a8d6-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="9a8d6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a8d6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a8d6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a8d6-113">Properties</span></span>

<span data-ttu-id="9a8d6-114">La **clase \_ ComponentCategory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a8d6-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-119">A short textual description of the object.</span></span>

<span data-ttu-id="9a8d6-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a8d6-121">**CategoryId**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-124">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Component Categories \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-125">GUID para esta categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="9a8d6-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-129">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-130">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-130">A textual description of the object.</span></span>

<span data-ttu-id="9a8d6-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a8d6-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-135">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-136">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-136">Indicates when the object was installed.</span></span> <span data-ttu-id="9a8d6-137">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9a8d6-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a8d6-139">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-142">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Component Categories \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-143">La propiedad nombre indica un nombre descriptivo de esta categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="9a8d6-144">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a8d6-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a8d6-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a8d6-147">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9a8d6-148">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="9a8d6-149">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9a8d6-150">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="9a8d6-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9a8d6-151">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9a8d6-152">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="9a8d6-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9a8d6-153">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9a8d6-154">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="9a8d6-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9a8d6-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9a8d6-156">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9a8d6-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9a8d6-157">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9a8d6-158">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9a8d6-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9a8d6-160">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9a8d6-161">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9a8d6-162">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9a8d6-163">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9a8d6-164">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9a8d6-165">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9a8d6-166">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9a8d6-167">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9a8d6-168">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9a8d6-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9a8d6-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9a8d6-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9a8d6-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a8d6-170">Remarks</span></span>

<span data-ttu-id="9a8d6-171">La **clase \_ ComponentCategory de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a8d6-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a8d6-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a8d6-172">Requirements</span></span>



| <span data-ttu-id="9a8d6-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a8d6-173">Requirement</span></span> | <span data-ttu-id="9a8d6-174">Value</span><span class="sxs-lookup"><span data-stu-id="9a8d6-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8d6-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a8d6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="9a8d6-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a8d6-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a8d6-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a8d6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="9a8d6-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a8d6-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a8d6-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a8d6-179">Namespace</span></span><br/>                | <span data-ttu-id="9a8d6-180">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9a8d6-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a8d6-181">MOF</span><span class="sxs-lookup"><span data-stu-id="9a8d6-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a8d6-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a8d6-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a8d6-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a8d6-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a8d6-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a8d6-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a8d6-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a8d6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8d6-186">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9a8d6-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="9a8d6-187">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8d6-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

