---
description: El proveedor de clases WDM define la clase WMIBinaryMofResource en \\ el \\ espacio de nombres root WMI para admitir la tarea de realizar un seguimiento del estado de los datos en el repositorio WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Clase WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908331"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="c6d98-103">Clase WMIBinaryMofResource</span><span class="sxs-lookup"><span data-stu-id="c6d98-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="c6d98-104">El proveedor de clases WDM define la clase **WMIBinaryMofResource** en \\ el \\ espacio de nombres root WMI para admitir la tarea de realizar un seguimiento del estado de los datos en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="c6d98-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6d98-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="c6d98-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6d98-106">Members</span></span>

<span data-ttu-id="c6d98-107">La clase **WMIBinaryMofResource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6d98-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="c6d98-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6d98-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6d98-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6d98-109">Properties</span></span>

<span data-ttu-id="c6d98-110">La clase **WMIBinaryMofResource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6d98-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6d98-111">**HighDateTime**</span><span class="sxs-lookup"><span data-stu-id="c6d98-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d98-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6d98-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6d98-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6d98-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6d98-115">Mitad superior de la marca de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="c6d98-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="c6d98-116">**LowDateTime**</span><span class="sxs-lookup"><span data-stu-id="c6d98-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d98-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6d98-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6d98-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6d98-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6d98-120">Mitad inferior de la marca de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="c6d98-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="c6d98-121">**MofProcessed**</span><span class="sxs-lookup"><span data-stu-id="c6d98-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d98-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c6d98-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c6d98-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c6d98-124">Marca que indica si el archivo. mof se ha procesado por completo.</span><span class="sxs-lookup"><span data-stu-id="c6d98-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="c6d98-125">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c6d98-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d98-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c6d98-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6d98-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d98-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6d98-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6d98-129">Nombre del controlador habilitado para WDM que tiene un archivo MOF binario compilado correctamente en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="c6d98-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6d98-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6d98-130">Remarks</span></span>

<span data-ttu-id="c6d98-131">El proveedor de clases WDM crea una instancia de **WMIBinaryMofResource** para cada controlador WDM que proporciona un archivo MOF binario.</span><span class="sxs-lookup"><span data-stu-id="c6d98-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="c6d98-132">Siempre que WMI inicializa el proveedor, el proveedor compara la marca de tiempo con la marca de tiempo del archivo de imagen del controlador.</span><span class="sxs-lookup"><span data-stu-id="c6d98-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="c6d98-133">Si las marcas de tiempo difieren, WMI vuelve a compilar el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="c6d98-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d98-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6d98-134">Requirements</span></span>



| <span data-ttu-id="c6d98-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d98-135">Requirement</span></span> | <span data-ttu-id="c6d98-136">Value</span><span class="sxs-lookup"><span data-stu-id="c6d98-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d98-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6d98-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d98-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6d98-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="c6d98-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6d98-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d98-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6d98-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c6d98-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6d98-141">Namespace</span></span><br/>                | <span data-ttu-id="c6d98-142">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="c6d98-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="c6d98-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c6d98-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6d98-144"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6d98-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d98-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6d98-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d98-146">Proveedor de WDM</span><span class="sxs-lookup"><span data-stu-id="c6d98-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

