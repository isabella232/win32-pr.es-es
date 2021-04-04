---
description: La \_ clase WMI ProtocolBinding Association de Win32 relaciona un controlador de nivel de sistema, un protocolo de red y un adaptador de red.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Win32_ProtocolBinding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907012"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="2ca24-103">\_Clase Win32 ProtocolBinding</span><span class="sxs-lookup"><span data-stu-id="2ca24-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="2ca24-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ProtocolBinding** Association de Win32 relaciona un controlador de nivel de sistema, un protocolo de red y un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2ca24-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="2ca24-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2ca24-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2ca24-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2ca24-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca24-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ca24-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="2ca24-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ca24-108">Members</span></span>

<span data-ttu-id="2ca24-109">La **clase \_ ProtocolBinding de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2ca24-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="2ca24-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ca24-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ca24-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ca24-111">Properties</span></span>

<span data-ttu-id="2ca24-112">La **clase \_ ProtocolBinding de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2ca24-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ca24-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2ca24-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca24-114">Tipo de datos: **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="2ca24-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2ca24-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-116">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")</span><span class="sxs-lookup"><span data-stu-id="2ca24-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="2ca24-117">Referencia a la instancia de que representa el protocolo que se utiliza con el controlador del sistema y en el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2ca24-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2ca24-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2ca24-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca24-119">Tipo de datos: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="2ca24-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2ca24-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-121">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="2ca24-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="2ca24-122">Referencia a la instancia de que representa el controlador del sistema que usa el adaptador de red a través del Protocolo de red de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2ca24-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="2ca24-123">**Dispositivo**</span><span class="sxs-lookup"><span data-stu-id="2ca24-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ca24-124">Tipo de datos: **Win32 \_ adaptador** de datos</span><span class="sxs-lookup"><span data-stu-id="2ca24-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2ca24-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ca24-126">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ adaptador de la")</span><span class="sxs-lookup"><span data-stu-id="2ca24-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="2ca24-127">Propiedades del adaptador de red que se usa en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2ca24-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ca24-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca24-128">Requirements</span></span>



| <span data-ttu-id="2ca24-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca24-129">Requirement</span></span> | <span data-ttu-id="2ca24-130">Value</span><span class="sxs-lookup"><span data-stu-id="2ca24-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca24-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca24-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca24-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ca24-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ca24-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca24-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca24-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ca24-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ca24-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2ca24-135">Namespace</span></span><br/>                | <span data-ttu-id="2ca24-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2ca24-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ca24-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2ca24-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ca24-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ca24-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ca24-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ca24-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca24-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca24-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca24-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ca24-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca24-142">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2ca24-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
