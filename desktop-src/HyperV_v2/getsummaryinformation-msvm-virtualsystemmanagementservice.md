---
description: Devuelve información de Resumen de la máquina virtual.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Método GetSummaryInformation de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360159"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bf09a-103">Método GetSummaryInformation de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="bf09a-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bf09a-104">Devuelve información de Resumen de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf09a-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf09a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf09a-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="bf09a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf09a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf09a-107">*SettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf09a-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf09a-108">Tipo: **CIM \_ VirtualSystemSettingData \[ \]**</span><span class="sxs-lookup"><span data-stu-id="bf09a-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="bf09a-109">Matriz de instancias de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que especifican las máquinas virtuales o las instantáneas para las que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="bf09a-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="bf09a-110">Si este parámetro es **null**, se recupera la información de todas las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="bf09a-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="bf09a-111">*RequestedInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf09a-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf09a-112">Tipo: **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="bf09a-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="bf09a-113">Matriz de valores de enumeración, que corresponden a las propiedades de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , que especifican los datos que se van a recuperar para las máquinas virtuales y las instantáneas especificadas en la matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="bf09a-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="bf09a-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre** (0)</span><span class="sxs-lookup"><span data-stu-id="bf09a-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-115">Esto corresponde a la propiedad **Name** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="bf09a-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nombre del elemento** (1)</span><span class="sxs-lookup"><span data-stu-id="bf09a-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-117">Esto corresponde a la propiedad **ElementName** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="bf09a-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Hora de creación** (2)</span><span class="sxs-lookup"><span data-stu-id="bf09a-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-119">Esto corresponde a la propiedad **CreationTime** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="bf09a-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notas** (3)</span><span class="sxs-lookup"><span data-stu-id="bf09a-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-121">Esto corresponde a la propiedad **notas** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="bf09a-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Número de procesadores** (4)</span><span class="sxs-lookup"><span data-stu-id="bf09a-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-123">Esto corresponde a la propiedad **NumberOfProcessors** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="bf09a-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Imagen en miniatura pequeña (80x60)** (5)</span><span class="sxs-lookup"><span data-stu-id="bf09a-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-125">Esto corresponde a la propiedad **ThumbnailImage** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="bf09a-126">Se recuperará una imagen en miniatura con las dimensiones de 80 60.</span><span class="sxs-lookup"><span data-stu-id="bf09a-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="bf09a-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Imagen en miniatura mediana (160x120)** (6)</span><span class="sxs-lookup"><span data-stu-id="bf09a-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-128">Esto corresponde a la propiedad **ThumbnailImage** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="bf09a-129">Se recuperará una imagen en miniatura con las dimensiones de 160 120.</span><span class="sxs-lookup"><span data-stu-id="bf09a-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="bf09a-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Imagen en miniatura grande (320x240)** (7)</span><span class="sxs-lookup"><span data-stu-id="bf09a-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-131">Esto corresponde a la propiedad **ThumbnailImage** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="bf09a-132">Se recuperará una imagen en miniatura con las dimensiones de 320 240.</span><span class="sxs-lookup"><span data-stu-id="bf09a-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="bf09a-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span><span class="sxs-lookup"><span data-stu-id="bf09a-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-134">Esto corresponde a la propiedad **AllocatedGPU** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="bf09a-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span><span class="sxs-lookup"><span data-stu-id="bf09a-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="bf09a-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión** (10)</span><span class="sxs-lookup"><span data-stu-id="bf09a-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="bf09a-137">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="bf09a-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="bf09a-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindado** (11)</span><span class="sxs-lookup"><span data-stu-id="bf09a-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="bf09a-139">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="bf09a-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="bf09a-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span><span class="sxs-lookup"><span data-stu-id="bf09a-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-141">Esto corresponde a la propiedad **EnabledState** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="bf09a-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span><span class="sxs-lookup"><span data-stu-id="bf09a-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-143">Esto corresponde a la propiedad **ProcessorLoad** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="bf09a-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span><span class="sxs-lookup"><span data-stu-id="bf09a-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-145">Esto corresponde a la propiedad **ProcessorLoadHistory** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="bf09a-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span><span class="sxs-lookup"><span data-stu-id="bf09a-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-147">Esto corresponde a la propiedad **MemoryUsage** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="bf09a-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Latido** (104)</span><span class="sxs-lookup"><span data-stu-id="bf09a-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-149">Esto corresponde a la propiedad **Heartbeat** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="bf09a-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tiempo de actividad** (105)</span><span class="sxs-lookup"><span data-stu-id="bf09a-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-151">Esto corresponde a la propiedad de **tiempo de actividad** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="bf09a-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span><span class="sxs-lookup"><span data-stu-id="bf09a-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-153">Esto corresponde a la propiedad **GuestOperatingSystem** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="bf09a-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantáneas** (107)</span><span class="sxs-lookup"><span data-stu-id="bf09a-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-155">Esto corresponde a la propiedad **snapshots** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="bf09a-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span><span class="sxs-lookup"><span data-stu-id="bf09a-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-157">Esto corresponde a la propiedad **AsynchronousTasks** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="bf09a-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span><span class="sxs-lookup"><span data-stu-id="bf09a-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-159">Esto corresponde a la propiedad **HealthState** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="bf09a-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="bf09a-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-161">Esto corresponde a la propiedad **OperationalStatus** de la clase [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="bf09a-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span><span class="sxs-lookup"><span data-stu-id="bf09a-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-163">Esto corresponde a la propiedad **StatusDescriptions** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="bf09a-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span><span class="sxs-lookup"><span data-stu-id="bf09a-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-165">Esto corresponde a la propiedad **MemoryAvailable** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="bf09a-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span><span class="sxs-lookup"><span data-stu-id="bf09a-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-167">Esto corresponde a la propiedad **AvailableMemoryBuffer** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="bf09a-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modo de replicación** (114)</span><span class="sxs-lookup"><span data-stu-id="bf09a-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-169">Esto corresponde a la propiedad **ReplicationMode** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="bf09a-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Estado de replicación** (115)</span><span class="sxs-lookup"><span data-stu-id="bf09a-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-171">Esto corresponde a la propiedad **ReplicationState** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="bf09a-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Sistema de réplica HealthTest de replicación** (116)</span><span class="sxs-lookup"><span data-stu-id="bf09a-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-173">Esto corresponde a la propiedad **ReplicationHealth** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="bf09a-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Estado** de la aplicación (117)</span><span class="sxs-lookup"><span data-stu-id="bf09a-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="bf09a-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span><span class="sxs-lookup"><span data-stu-id="bf09a-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-176">Esto corresponde a la propiedad **ReplicationState** de la [**clase \_ ReplicationRelationship de MSVM**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="bf09a-177">Esta es una matriz para todos los valores de estado de replicación en la relación principal y la extendida.</span><span class="sxs-lookup"><span data-stu-id="bf09a-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="bf09a-178">0 el valor del índice siempre es para la relación principal y, si la replicación extendida está habilitada, se devuelve en el índice 1.</span><span class="sxs-lookup"><span data-stu-id="bf09a-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="bf09a-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span><span class="sxs-lookup"><span data-stu-id="bf09a-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-180">Esto corresponde a la propiedad **ReplicationHealth** de la [**clase \_ ReplicationRelationship de MSVM**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="bf09a-181">Se trata de una matriz para todos los valores de mantenimiento de la replicación a través de la relación principal y extendida.</span><span class="sxs-lookup"><span data-stu-id="bf09a-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="bf09a-182">0 el valor del índice siempre es para la relación principal y, si la replicación extendida está habilitada, se devuelve en el índice 1.</span><span class="sxs-lookup"><span data-stu-id="bf09a-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="bf09a-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span><span class="sxs-lookup"><span data-stu-id="bf09a-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-184">Esto corresponde a la propiedad **SwapFilesInUse** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="bf09a-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span><span class="sxs-lookup"><span data-stu-id="bf09a-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="bf09a-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span><span class="sxs-lookup"><span data-stu-id="bf09a-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-187">Esto corresponde a la propiedad **Name** de la clase [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="bf09a-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span><span class="sxs-lookup"><span data-stu-id="bf09a-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="bf09a-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span><span class="sxs-lookup"><span data-stu-id="bf09a-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-190">Esto corresponde a la propiedad **IntegrationServicesVersionState** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="bf09a-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span><span class="sxs-lookup"><span data-stu-id="bf09a-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="bf09a-192">Esto corresponde a la propiedad **OtherEnabledState** de la [**clase \_ SummaryInformation de MSVM**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bf09a-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="bf09a-193">(133)</span><span class="sxs-lookup"><span data-stu-id="bf09a-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="bf09a-194">*SummaryInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bf09a-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf09a-195">Tipo: **[ **MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="bf09a-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="bf09a-196">Una matriz de instancias de [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md) que contiene la información solicitada para las máquinas virtuales y/o las instantáneas especificadas en la matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="bf09a-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="bf09a-197">Esta matriz tendrá el mismo número de elementos que la matriz *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="bf09a-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="bf09a-198">Cada una de estas entradas contendrá la propiedad **Name** , aunque no se haya solicitado esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="bf09a-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="bf09a-199">Si no se encuentra la máquina virtual o la instantánea o no está disponible, la propiedad **nombre** de la entrada de información de Resumen correspondiente estará vacía.</span><span class="sxs-lookup"><span data-stu-id="bf09a-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="bf09a-200">Las propiedades no especificadas en el parámetro *RequestedInformation* tendrán un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="bf09a-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="bf09a-201">DataType actualizado desde en Windows 10, versión 1703 de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="bf09a-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf09a-202">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf09a-202">Return value</span></span>

<span data-ttu-id="bf09a-203">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf09a-203">Type: **uint32**</span></span>

<span data-ttu-id="bf09a-204">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf09a-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf09a-205">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bf09a-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-206">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="bf09a-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-207">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="bf09a-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-208">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bf09a-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-209">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="bf09a-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-210">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bf09a-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-211">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="bf09a-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-212">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bf09a-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-213">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bf09a-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-214">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="bf09a-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-215">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bf09a-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-216">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bf09a-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bf09a-217">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bf09a-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf09a-218">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf09a-218">Remarks</span></span>

<span data-ttu-id="bf09a-219">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="bf09a-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bf09a-220">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bf09a-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bf09a-221">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf09a-221">Examples</span></span>

<span data-ttu-id="bf09a-222">En el siguiente ejemplo de C# se muestra información de resumen.</span><span class="sxs-lookup"><span data-stu-id="bf09a-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="bf09a-223">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="bf09a-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf09a-224">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="bf09a-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="bf09a-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf09a-225">Requirements</span></span>



| <span data-ttu-id="bf09a-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf09a-226">Requirement</span></span> | <span data-ttu-id="bf09a-227">Value</span><span class="sxs-lookup"><span data-stu-id="bf09a-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf09a-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf09a-228">Minimum supported client</span></span><br/> | <span data-ttu-id="bf09a-229">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf09a-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf09a-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf09a-230">Minimum supported server</span></span><br/> | <span data-ttu-id="bf09a-231">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf09a-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf09a-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf09a-232">Namespace</span></span><br/>                | <span data-ttu-id="bf09a-233">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bf09a-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf09a-234">MOF</span><span class="sxs-lookup"><span data-stu-id="bf09a-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf09a-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf09a-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf09a-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf09a-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf09a-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf09a-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf09a-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf09a-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf09a-239">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bf09a-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="bf09a-240">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf09a-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bf09a-241">**MSVM \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="bf09a-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

