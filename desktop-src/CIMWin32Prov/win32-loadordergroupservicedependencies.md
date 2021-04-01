---
description: La \_ clase WMI LoadOrderGroupServiceDependencies Association de Win32 relaciona un servicio base y un grupo de orden de carga del que depende el servicio para empezar a ejecutarse.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceDependencies (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153428"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="194d8-103">\_Clase Win32 LoadOrderGroupServiceDependencies</span><span class="sxs-lookup"><span data-stu-id="194d8-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="194d8-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoadOrderGroupServiceDependencies** Association de Win32 relaciona un servicio base y un grupo de orden de carga del que depende el servicio para empezar a ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="194d8-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="194d8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="194d8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="194d8-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="194d8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="194d8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="194d8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="194d8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="194d8-108">Members</span></span>

<span data-ttu-id="194d8-109">La **clase \_ LoadOrderGroupServiceDependencies de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="194d8-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="194d8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="194d8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="194d8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="194d8-111">Properties</span></span>

<span data-ttu-id="194d8-112">La **clase \_ LoadOrderGroupServiceDependencies de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="194d8-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="194d8-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="194d8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d8-114">Tipo de datos: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="194d8-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="194d8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="194d8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="194d8-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="194d8-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="194d8-117">Referencia a la instancia de que representa las propiedades del grupo de orden de carga que deben iniciarse antes de que se pueda iniciar el servicio base dependiente de esta clase.</span><span class="sxs-lookup"><span data-stu-id="194d8-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="194d8-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="194d8-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d8-119">Tipo de datos: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="194d8-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="194d8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="194d8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="194d8-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="194d8-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="194d8-122">Referencia a la instancia de que representa las propiedades del servicio base que depende del grupo de pedidos de carga para empezar a ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="194d8-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="194d8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="194d8-123">Remarks</span></span>

<span data-ttu-id="194d8-124">La **clase \_ LoadOrderGroupServiceDependencies de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="194d8-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="194d8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="194d8-125">Requirements</span></span>



| <span data-ttu-id="194d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="194d8-126">Requirement</span></span> | <span data-ttu-id="194d8-127">Value</span><span class="sxs-lookup"><span data-stu-id="194d8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="194d8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="194d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="194d8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="194d8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="194d8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="194d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="194d8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="194d8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="194d8-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="194d8-132">Namespace</span></span><br/>                | <span data-ttu-id="194d8-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="194d8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="194d8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="194d8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="194d8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="194d8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="194d8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="194d8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="194d8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="194d8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194d8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="194d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194d8-139">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="194d8-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="194d8-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="194d8-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

