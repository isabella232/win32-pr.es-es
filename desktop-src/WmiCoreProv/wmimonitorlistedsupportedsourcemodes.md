---
description: Enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Clase WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716375"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="165d7-103">Clase WmiMonitorListedSupportedSourceModes</span><span class="sxs-lookup"><span data-stu-id="165d7-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="165d7-104">El **WmiMonitorListedSupportedSourceModes** enumera los modos de origen admitidos para un monitor de vídeo en su descriptor de monitor, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="165d7-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="165d7-105">En el caso de los monitores que no tienen ninguna descripción, esta lista de modos se genera en función del tipo de monitor, tal y como se especifica en el controlador de bus de supervisión.</span><span class="sxs-lookup"><span data-stu-id="165d7-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="165d7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="165d7-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="165d7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="165d7-107">Members</span></span>

<span data-ttu-id="165d7-108">La clase **WmiMonitorListedSupportedSourceModes** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="165d7-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="165d7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="165d7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="165d7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="165d7-110">Properties</span></span>

<span data-ttu-id="165d7-111">La clase **WmiMonitorListedSupportedSourceModes** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="165d7-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="165d7-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="165d7-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="165d7-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="165d7-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="165d7-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="165d7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="165d7-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="165d7-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="165d7-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="165d7-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="165d7-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="165d7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="165d7-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="165d7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="165d7-119">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="165d7-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="165d7-120">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="165d7-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="165d7-121">**MonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="165d7-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="165d7-122">Tipo de datos: matriz **VideoModeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="165d7-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="165d7-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="165d7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="165d7-124">Enumera los modos de origen de monitor que representan las instancias de la clase [**VideoModeDescriptor**](videomodedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="165d7-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="165d7-125">**NumOfMonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="165d7-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="165d7-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="165d7-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="165d7-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="165d7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="165d7-128">Número de modo de origen de monitor compatible.</span><span class="sxs-lookup"><span data-stu-id="165d7-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="165d7-129">**PreferredMonitorSourceModeIndex**</span><span class="sxs-lookup"><span data-stu-id="165d7-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="165d7-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="165d7-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="165d7-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="165d7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="165d7-132">Índice de modo de origen de monitor preferido.</span><span class="sxs-lookup"><span data-stu-id="165d7-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="165d7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="165d7-133">Requirements</span></span>



| <span data-ttu-id="165d7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="165d7-134">Requirement</span></span> | <span data-ttu-id="165d7-135">Value</span><span class="sxs-lookup"><span data-stu-id="165d7-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="165d7-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="165d7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="165d7-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="165d7-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="165d7-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="165d7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="165d7-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="165d7-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="165d7-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="165d7-140">Namespace</span></span><br/>                | <span data-ttu-id="165d7-141">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="165d7-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="165d7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="165d7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="165d7-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="165d7-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="165d7-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="165d7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="165d7-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="165d7-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165d7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="165d7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165d7-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="165d7-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




