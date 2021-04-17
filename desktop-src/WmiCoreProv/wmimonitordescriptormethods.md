---
description: Contiene métodos que obtienen el contenido sin procesar de la definición de entrada de vídeo de Video Electronics estándar Association (VESA) datos de identificación mejorada de la visualización extendida (E-EDID) v. 1. x 128 bits bloques de datos de bytes.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Clase WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678198"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="3fb59-103">Clase WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="3fb59-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="3fb59-104">La clase WMI **WmiMonitorDescriptorMethods** contiene métodos que obtienen el contenido sin procesar de la definición de entrada de vídeo de Video Electronics estándar Association (VESA) datos de identificación de presentación extendida mejorada (E-EDID) v. 1. x 128 bits bloques de datos de bytes.</span><span class="sxs-lookup"><span data-stu-id="3fb59-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb59-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb59-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="3fb59-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fb59-106">Members</span></span>

<span data-ttu-id="3fb59-107">La clase **WmiMonitorDescriptorMethods** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3fb59-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="3fb59-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fb59-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="3fb59-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fb59-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3fb59-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fb59-110">Methods</span></span>

<span data-ttu-id="3fb59-111">La clase **WmiMonitorDescriptorMethods** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3fb59-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="3fb59-112">Método</span><span class="sxs-lookup"><span data-stu-id="3fb59-112">Method</span></span>                                                                                           | <span data-ttu-id="3fb59-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fb59-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="3fb59-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="3fb59-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="3fb59-115">Obtiene acceso a los datos sin procesar de un bloque de descriptor de EDID v. 1. x especificado.</span><span class="sxs-lookup"><span data-stu-id="3fb59-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3fb59-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fb59-116">Properties</span></span>

<span data-ttu-id="3fb59-117">La clase **WmiMonitorDescriptorMethods** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3fb59-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fb59-118">**Activo**</span><span class="sxs-lookup"><span data-stu-id="3fb59-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fb59-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3fb59-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fb59-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fb59-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fb59-121">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="3fb59-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="3fb59-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="3fb59-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fb59-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3fb59-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fb59-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fb59-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fb59-125">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3fb59-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3fb59-126">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="3fb59-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fb59-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb59-127">Requirements</span></span>



| <span data-ttu-id="3fb59-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb59-128">Requirement</span></span> | <span data-ttu-id="3fb59-129">Value</span><span class="sxs-lookup"><span data-stu-id="3fb59-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb59-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb59-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fb59-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3fb59-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb59-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fb59-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3fb59-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fb59-134">Namespace</span></span><br/>                | <span data-ttu-id="3fb59-135">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="3fb59-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3fb59-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb59-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb59-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fb59-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb59-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fb59-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb59-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb59-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb59-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fb59-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb59-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="3fb59-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




