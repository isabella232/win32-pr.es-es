---
description: Asocia los datos de configuración a un elemento administrado.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: CIM_SettingsDefineState (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687953"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="35407-103">\_Clase SettingsDefineState de CIM</span><span class="sxs-lookup"><span data-stu-id="35407-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="35407-104">Asocia los datos de configuración a un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="35407-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="35407-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35407-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="35407-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="35407-106">Members</span></span>

<span data-ttu-id="35407-107">La clase **CIM \_ SettingsDefineState** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35407-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="35407-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35407-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35407-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35407-109">Properties</span></span>

<span data-ttu-id="35407-110">La clase **CIM \_ SettingsDefineState** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35407-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35407-111">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="35407-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35407-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="35407-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="35407-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35407-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35407-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35407-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35407-115">Elemento administrado en la asociación.</span><span class="sxs-lookup"><span data-stu-id="35407-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="35407-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="35407-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35407-117">Tipo de datos **: \_ SettingData de CIM**</span><span class="sxs-lookup"><span data-stu-id="35407-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="35407-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35407-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35407-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35407-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35407-120">Los datos de configuración de la asociación.</span><span class="sxs-lookup"><span data-stu-id="35407-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35407-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35407-121">Requirements</span></span>



| <span data-ttu-id="35407-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35407-122">Requirement</span></span> | <span data-ttu-id="35407-123">Value</span><span class="sxs-lookup"><span data-stu-id="35407-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35407-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35407-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35407-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="35407-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="35407-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35407-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35407-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="35407-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="35407-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35407-128">Namespace</span></span><br/>                | <span data-ttu-id="35407-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="35407-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35407-130">MOF</span><span class="sxs-lookup"><span data-stu-id="35407-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35407-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35407-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35407-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35407-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35407-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35407-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

