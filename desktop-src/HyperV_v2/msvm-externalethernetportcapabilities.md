---
description: Describe las capacidades de la ExternalEthernetPort de MSVM asociada \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Msvm_ExternalEthernetPortCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908138"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="1782a-103">MSVM \_ ExternalEthernetPortCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="1782a-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="1782a-104">Describe las capacidades de la [**\_ ExternalEthernetPort de MSVM**](msvm-externalethernetport.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="1782a-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="1782a-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1782a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1782a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1782a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="1782a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1782a-107">Members</span></span>

<span data-ttu-id="1782a-108">La clase **MSVM \_ ExternalEthernetPortCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1782a-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1782a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1782a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1782a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1782a-110">Properties</span></span>

<span data-ttu-id="1782a-111">La clase **MSVM \_ ExternalEthernetPortCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1782a-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1782a-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1782a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1782a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1782a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1782a-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1782a-115">A short description of the object.</span></span> <span data-ttu-id="1782a-116">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="1782a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="1782a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1782a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1782a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1782a-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1782a-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1782a-120">A description of the object.</span></span> <span data-ttu-id="1782a-121">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "describe las capacidades del puerto Ethernet externo de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="1782a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="1782a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1782a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1782a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1782a-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1782a-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="1782a-125">A display name for the object.</span></span> <span data-ttu-id="1782a-126">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="1782a-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="1782a-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1782a-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1782a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1782a-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1782a-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="1782a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1782a-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="1782a-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1782a-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1782a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1782a-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="1782a-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1782a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1782a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1782a-136">Valor booleano que indica si el adaptador de red admite la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="1782a-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="1782a-137">Si el valor es **true**, el adaptador de red admite IOV y la propiedad **iovsupportreasons incluirán** estará vacía.</span><span class="sxs-lookup"><span data-stu-id="1782a-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="1782a-138">De lo contrario, la propiedad **iovsupportreasons incluirán** tendrá los motivos por los que no se admite IOV.</span><span class="sxs-lookup"><span data-stu-id="1782a-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="1782a-139">**Iovsupportreasons incluirán**</span><span class="sxs-lookup"><span data-stu-id="1782a-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1782a-140">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1782a-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1782a-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1782a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1782a-142">Matriz de cadenas que indica los posibles motivos por los que no se admite IOV.</span><span class="sxs-lookup"><span data-stu-id="1782a-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="1782a-143">Si el valor de **IOVSupport** es **true**, esta matriz estará vacía.</span><span class="sxs-lookup"><span data-stu-id="1782a-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1782a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1782a-144">Requirements</span></span>



| <span data-ttu-id="1782a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1782a-145">Requirement</span></span> | <span data-ttu-id="1782a-146">Value</span><span class="sxs-lookup"><span data-stu-id="1782a-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1782a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1782a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1782a-148">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1782a-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1782a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1782a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1782a-150">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1782a-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1782a-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1782a-151">Namespace</span></span><br/>                | <span data-ttu-id="1782a-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1782a-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1782a-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1782a-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1782a-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1782a-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1782a-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1782a-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1782a-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1782a-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

