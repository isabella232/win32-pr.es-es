---
description: La \_ Asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que la sesión proporciona acceso.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Win32_SessionResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807741"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="66680-103">\_Clase Win32 SessionResource</span><span class="sxs-lookup"><span data-stu-id="66680-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="66680-104">La \_ Asociación SessionResource de Win32 representa la relación entre una sesión y los recursos a los que la sesión proporciona acceso.</span><span class="sxs-lookup"><span data-stu-id="66680-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="66680-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="66680-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66680-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66680-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="66680-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="66680-107">Members</span></span>

<span data-ttu-id="66680-108">La **clase \_ SessionResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="66680-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="66680-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66680-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66680-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66680-110">Properties</span></span>

<span data-ttu-id="66680-111">La **clase \_ SessionResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="66680-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66680-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="66680-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66680-113">Tipo de datos: **Win32 \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="66680-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="66680-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66680-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66680-115">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="66680-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="66680-116">La referencia Antecedent representa los recursos usados por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="66680-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="66680-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="66680-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66680-118">Tipo de datos **: \_ sesión Win32**</span><span class="sxs-lookup"><span data-stu-id="66680-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="66680-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66680-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66680-120">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="66680-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="66680-121">La referencia dependiente representa la sesión que utiliza el recurso.</span><span class="sxs-lookup"><span data-stu-id="66680-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66680-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66680-122">Requirements</span></span>



| <span data-ttu-id="66680-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66680-123">Requirement</span></span> | <span data-ttu-id="66680-124">Value</span><span class="sxs-lookup"><span data-stu-id="66680-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66680-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66680-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66680-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66680-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66680-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66680-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66680-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66680-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66680-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66680-129">Namespace</span></span><br/>                | <span data-ttu-id="66680-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="66680-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66680-131">MOF</span><span class="sxs-lookup"><span data-stu-id="66680-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66680-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66680-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66680-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66680-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66680-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66680-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66680-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="66680-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66680-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="66680-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
