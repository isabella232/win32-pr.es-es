---
title: Win32_SessionBrokerTarget (clase)
description: Define la consulta para un destino del agente de sesión.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTarget clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerTarget de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905609"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="8b9fd-105">\_Clase Win32 SessionBrokerTarget</span><span class="sxs-lookup"><span data-stu-id="8b9fd-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="8b9fd-106">Define la consulta para un destino del agente de sesión.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="8b9fd-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b9fd-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="8b9fd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b9fd-109">Members</span></span>

<span data-ttu-id="8b9fd-110">La **clase \_ SessionBrokerTarget de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8b9fd-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="8b9fd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b9fd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b9fd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b9fd-112">Properties</span></span>

<span data-ttu-id="8b9fd-113">La **clase \_ SessionBrokerTarget de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b9fd-114">**Entorno**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b9fd-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b9fd-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b9fd-117">El nombre del entorno.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-117">The environment name.</span></span> <span data-ttu-id="8b9fd-118">En el caso de un destino de máquina virtual (VM), podría ser el nombre de host de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="8b9fd-119">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b9fd-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b9fd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b9fd-122">El nombre de la granja a la que pertenece el destino.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="8b9fd-123">**Guid**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b9fd-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b9fd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b9fd-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b9fd-127">GUID (si existe) del destino.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="8b9fd-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b9fd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b9fd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b9fd-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b9fd-132">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="8b9fd-133">**NombreDeDestino**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b9fd-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b9fd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b9fd-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b9fd-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b9fd-136">Nombre del destino.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8b9fd-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b9fd-137">Examples</span></span>

<span data-ttu-id="8b9fd-138">La siguiente cadena de consulta muestra cómo \_ se usa la clase SessionBrokerTarget de Win32 en una consulta.</span><span class="sxs-lookup"><span data-stu-id="8b9fd-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="8b9fd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9fd-139">Requirements</span></span>



| <span data-ttu-id="8b9fd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9fd-140">Requirement</span></span> | <span data-ttu-id="8b9fd-141">Value</span><span class="sxs-lookup"><span data-stu-id="8b9fd-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9fd-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9fd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9fd-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8b9fd-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b9fd-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b9fd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9fd-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b9fd-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="8b9fd-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b9fd-146">Namespace</span></span><br/>                | <span data-ttu-id="8b9fd-147">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8b9fd-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="8b9fd-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8b9fd-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b9fd-149"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b9fd-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b9fd-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b9fd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b9fd-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b9fd-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

