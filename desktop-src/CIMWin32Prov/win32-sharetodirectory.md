---
description: La \_ clase WMI ShareToDirectory Association de Win32 relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Win32_ShareToDirectory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807016"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="23127-103">\_Clase Win32 ShareToDirectory</span><span class="sxs-lookup"><span data-stu-id="23127-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="23127-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ShareToDirectory** Association de Win32 relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.</span><span class="sxs-lookup"><span data-stu-id="23127-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="23127-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="23127-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="23127-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="23127-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="23127-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23127-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="23127-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="23127-108">Members</span></span>

<span data-ttu-id="23127-109">La **clase \_ ShareToDirectory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23127-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="23127-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23127-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23127-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23127-111">Properties</span></span>

<span data-ttu-id="23127-112">La **clase \_ ShareToDirectory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23127-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23127-113">**Compartir**</span><span class="sxs-lookup"><span data-stu-id="23127-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23127-114">Tipo de datos **: \_ recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="23127-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="23127-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23127-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23127-116">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ share")</span><span class="sxs-lookup"><span data-stu-id="23127-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="23127-117">Referencia a la instancia de que representa las propiedades de un recurso compartido disponible a través del directorio.</span><span class="sxs-lookup"><span data-stu-id="23127-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="23127-118">**SharedElement**</span><span class="sxs-lookup"><span data-stu-id="23127-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23127-119">Tipo de datos **: \_ directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="23127-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="23127-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23127-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23127-121">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directorio CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="23127-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="23127-122">Referencia a la instancia de que representa las propiedades del directorio que se ha asignado a un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="23127-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23127-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23127-123">Requirements</span></span>



| <span data-ttu-id="23127-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="23127-124">Requirement</span></span> | <span data-ttu-id="23127-125">Value</span><span class="sxs-lookup"><span data-stu-id="23127-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23127-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23127-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23127-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23127-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23127-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23127-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23127-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23127-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23127-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23127-130">Namespace</span></span><br/>                | <span data-ttu-id="23127-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="23127-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23127-132">MOF</span><span class="sxs-lookup"><span data-stu-id="23127-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23127-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23127-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23127-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23127-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23127-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23127-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23127-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="23127-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23127-137">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="23127-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
