---
description: Muestra los intervalos de frecuencia que admite el monitor.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Clase WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716376"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="be5ca-103">Clase WmiMonitorListedFrequencyRanges</span><span class="sxs-lookup"><span data-stu-id="be5ca-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="be5ca-104">La clase WMI **WmiMonitorListedFrequencyRanges** muestra los intervalos de frecuencia que admite el monitor.</span><span class="sxs-lookup"><span data-stu-id="be5ca-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="be5ca-105">Estos intervalos se encuentran en la definición de entrada de vídeo del bloque de datos de identificación mejorada de la presentación extendida de vídeo (VESA) o en el archivo INF de Windows que contiene los datos del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be5ca-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5ca-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be5ca-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="be5ca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="be5ca-107">Members</span></span>

<span data-ttu-id="be5ca-108">La clase **WmiMonitorListedFrequencyRanges** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="be5ca-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="be5ca-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be5ca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be5ca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be5ca-110">Properties</span></span>

<span data-ttu-id="be5ca-111">La clase **WmiMonitorListedFrequencyRanges** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="be5ca-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be5ca-112">**Activo**</span><span class="sxs-lookup"><span data-stu-id="be5ca-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be5ca-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="be5ca-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be5ca-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be5ca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be5ca-115">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="be5ca-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="be5ca-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="be5ca-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be5ca-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="be5ca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be5ca-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be5ca-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be5ca-119">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="be5ca-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="be5ca-120">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="be5ca-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="be5ca-121">**MonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="be5ca-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be5ca-122">Tipo de datos: matriz **FrequencyRangeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="be5ca-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="be5ca-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be5ca-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be5ca-124">Lista de intervalos de frecuencia de monitor representados por instancias de la clase [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="be5ca-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="be5ca-125">**NumOfMonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="be5ca-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be5ca-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be5ca-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be5ca-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be5ca-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be5ca-128">Número de intervalos de frecuencia de monitor compatibles.</span><span class="sxs-lookup"><span data-stu-id="be5ca-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be5ca-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be5ca-129">Requirements</span></span>



| <span data-ttu-id="be5ca-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5ca-130">Requirement</span></span> | <span data-ttu-id="be5ca-131">Value</span><span class="sxs-lookup"><span data-stu-id="be5ca-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be5ca-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be5ca-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be5ca-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be5ca-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="be5ca-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be5ca-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be5ca-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be5ca-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="be5ca-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be5ca-136">Namespace</span></span><br/>                | <span data-ttu-id="be5ca-137">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="be5ca-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="be5ca-138">MOF</span><span class="sxs-lookup"><span data-stu-id="be5ca-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be5ca-139"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be5ca-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="be5ca-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be5ca-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be5ca-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be5ca-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5ca-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="be5ca-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5ca-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="be5ca-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




