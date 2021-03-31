---
title: Win32_SessionBrokerFarm (clase)
description: Define la consulta para una granja de agentes de sesiones.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarm clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerFarm de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490588"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="b9177-105">\_Clase Win32 SessionBrokerFarm</span><span class="sxs-lookup"><span data-stu-id="b9177-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="b9177-106">Define la consulta para una granja de agentes de sesiones.</span><span class="sxs-lookup"><span data-stu-id="b9177-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="b9177-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b9177-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9177-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9177-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="b9177-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9177-109">Members</span></span>

<span data-ttu-id="b9177-110">La **clase \_ SessionBrokerFarm de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b9177-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="b9177-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9177-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9177-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9177-112">Properties</span></span>

<span data-ttu-id="b9177-113">La **clase \_ SessionBrokerFarm de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9177-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9177-114">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="b9177-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9177-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9177-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9177-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9177-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9177-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9177-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9177-118">El nombre de la granja de agentes de sesiones que debe consultarse.</span><span class="sxs-lookup"><span data-stu-id="b9177-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="b9177-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="b9177-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9177-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9177-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9177-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9177-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9177-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9177-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9177-123">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="b9177-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b9177-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9177-124">Examples</span></span>

<span data-ttu-id="b9177-125">La siguiente cadena de consulta muestra cómo se usa la clase **\_ SessionBrokerFarm de Win32** en una consulta.</span><span class="sxs-lookup"><span data-stu-id="b9177-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="b9177-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9177-126">Requirements</span></span>



| <span data-ttu-id="b9177-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9177-127">Requirement</span></span> | <span data-ttu-id="b9177-128">Value</span><span class="sxs-lookup"><span data-stu-id="b9177-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9177-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9177-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9177-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9177-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b9177-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9177-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9177-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9177-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b9177-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9177-133">Namespace</span></span><br/>                | <span data-ttu-id="b9177-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b9177-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b9177-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b9177-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9177-136"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9177-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9177-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9177-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9177-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9177-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

