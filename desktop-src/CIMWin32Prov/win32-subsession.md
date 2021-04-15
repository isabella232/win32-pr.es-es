---
description: La Asociación de la \_ subsesión de Win32 define las relaciones entre las sesiones en las que una sesión forma parte o utiliza otra sesión, por ejemplo, donde una sesión de terminal utiliza una sesión de inicio de sesión.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Win32_SubSession (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539219"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="a00ca-103">\_Clase de subsesión de Win32</span><span class="sxs-lookup"><span data-stu-id="a00ca-103">Win32\_SubSession class</span></span>

<span data-ttu-id="a00ca-104">La Asociación de la \_ subsesión de Win32 define las relaciones entre las sesiones en las que una sesión forma parte o utiliza otra sesión, por ejemplo, donde una sesión de terminal utiliza una sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a00ca-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="a00ca-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a00ca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a00ca-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a00ca-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a00ca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a00ca-107">Members</span></span>

<span data-ttu-id="a00ca-108">La clase de **\_ subsesión de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a00ca-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="a00ca-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a00ca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a00ca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a00ca-110">Properties</span></span>

<span data-ttu-id="a00ca-111">La clase de **\_ subsesión de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a00ca-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a00ca-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a00ca-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00ca-113">Tipo de datos **: \_ sesión Win32**</span><span class="sxs-lookup"><span data-stu-id="a00ca-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="a00ca-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a00ca-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a00ca-115">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) (antecedente)</span><span class="sxs-lookup"><span data-stu-id="a00ca-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="a00ca-116">Una [**\_ sesión de Win32**](win32-session.md) que describe la sesión que tiene una subsesión.</span><span class="sxs-lookup"><span data-stu-id="a00ca-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="a00ca-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a00ca-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a00ca-118">Tipo de datos **: \_ sesión Win32**</span><span class="sxs-lookup"><span data-stu-id="a00ca-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="a00ca-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a00ca-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a00ca-120">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) (dependiente)</span><span class="sxs-lookup"><span data-stu-id="a00ca-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="a00ca-121">Una [**\_ sesión de Win32**](win32-session.md) que describe la sesión que es la subsesión.</span><span class="sxs-lookup"><span data-stu-id="a00ca-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a00ca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a00ca-122">Requirements</span></span>



| <span data-ttu-id="a00ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a00ca-123">Requirement</span></span> | <span data-ttu-id="a00ca-124">Value</span><span class="sxs-lookup"><span data-stu-id="a00ca-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a00ca-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a00ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a00ca-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a00ca-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a00ca-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a00ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a00ca-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a00ca-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a00ca-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a00ca-129">Namespace</span></span><br/>                | <span data-ttu-id="a00ca-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a00ca-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a00ca-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a00ca-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a00ca-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a00ca-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a00ca-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a00ca-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a00ca-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a00ca-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a00ca-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a00ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00ca-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a00ca-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
