---
description: Representa los parámetros de entrada de vídeo analógico de un monitor de equipo.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Clase WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002314"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="6b96f-103">Clase WmiMonitorAnalogVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="6b96f-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="6b96f-104">La clase WMI **WmiMonitorAnalogVideoInputParams** representa los parámetros de entrada de vídeo analógico de un monitor de equipo.</span><span class="sxs-lookup"><span data-stu-id="6b96f-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="6b96f-105">Los datos de esta clase se corresponden con los datos de la definición de entrada de vídeo de vídeo electrónica estándar (VESA) estándar de identificación de la visualización extendida mejorada (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="6b96f-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="6b96f-106">Una instancia de esta clase solo está disponible cuando el valor de la propiedad **VideoInputType** de la clase [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) es "analógico".</span><span class="sxs-lookup"><span data-stu-id="6b96f-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="6b96f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b96f-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="6b96f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b96f-108">Members</span></span>

<span data-ttu-id="6b96f-109">La clase **WmiMonitorAnalogVideoInputParams** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b96f-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="6b96f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b96f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b96f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b96f-111">Properties</span></span>

<span data-ttu-id="6b96f-112">La clase **WmiMonitorAnalogVideoInputParams** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b96f-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b96f-113">**Activo**</span><span class="sxs-lookup"><span data-stu-id="6b96f-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b96f-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-116">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="6b96f-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6b96f-117">**CompositeSyncSupported**</span><span class="sxs-lookup"><span data-stu-id="6b96f-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-118">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-120">Indica si se admite la sincronización compuesta.</span><span class="sxs-lookup"><span data-stu-id="6b96f-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="6b96f-121">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-121">Value</span></span>                                                                              | <span data-ttu-id="6b96f-122">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b96f-123"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-124">Se admite la sincronización compuesta en la línea de sincronización horizontal.</span><span class="sxs-lookup"><span data-stu-id="6b96f-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-126">No se admite la sincronización compuesta en la línea de sincronización horizontal.</span><span class="sxs-lookup"><span data-stu-id="6b96f-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b96f-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="6b96f-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b96f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="6b96f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-131">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="6b96f-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="6b96f-132">**SeparateSyncsSupported**</span><span class="sxs-lookup"><span data-stu-id="6b96f-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-133">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-135">Indica si se admiten sincronizaciones independientes.</span><span class="sxs-lookup"><span data-stu-id="6b96f-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="6b96f-136">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-136">Value</span></span>                                                                              | <span data-ttu-id="6b96f-137">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6b96f-138"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-139">Se admiten sincronizaciones independientes.</span><span class="sxs-lookup"><span data-stu-id="6b96f-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-141">No se admiten sincronizaciones independientes.</span><span class="sxs-lookup"><span data-stu-id="6b96f-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b96f-142">**SerrationOfVsyncRequired**</span><span class="sxs-lookup"><span data-stu-id="6b96f-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-143">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-145">Indica si se requiere serration de impulso de sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="6b96f-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="6b96f-146">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-146">Value</span></span>                                                                              | <span data-ttu-id="6b96f-147">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b96f-148"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-149">Se requiere Serration del impulso de sincronización vertical cuando se usa la sincronización compuesta o el vídeo de sincronización en verde.</span><span class="sxs-lookup"><span data-stu-id="6b96f-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-151">No es necesario Serration del impulso de sincronización vertical cuando se usa la sincronización compuesta o el vídeo de sincronización en verde.</span><span class="sxs-lookup"><span data-stu-id="6b96f-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b96f-152">**SetupExpected**</span><span class="sxs-lookup"><span data-stu-id="6b96f-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-153">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-155">Indica si se espera la instalación.</span><span class="sxs-lookup"><span data-stu-id="6b96f-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="6b96f-156">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-156">Value</span></span>                                                                              | <span data-ttu-id="6b96f-157">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b96f-158"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-159">El monitor espera una instalación en blanco en blanco o en un pedestal según el estándar de nivel de señal adecuado.</span><span class="sxs-lookup"><span data-stu-id="6b96f-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="6b96f-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-161">El monitor no espera una configuración en blanco en blanco ni en el pedestal según el estándar de nivel de señal adecuado.</span><span class="sxs-lookup"><span data-stu-id="6b96f-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6b96f-162">**SignalLevelStandard**</span><span class="sxs-lookup"><span data-stu-id="6b96f-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-163">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-165">Estándar de nivel de señal para conexiones de conector de vídeo mejorado (EVC).</span><span class="sxs-lookup"><span data-stu-id="6b96f-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="6b96f-166">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-166">Value</span></span>                                                                              | <span data-ttu-id="6b96f-167">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="6b96f-168"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-169">0,7, 0,3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6b96f-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-171">0.714, 0,286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6b96f-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="6b96f-172"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="6b96f-173">1,0, 0.4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6b96f-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-174"><dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="6b96f-175">0,7, 0.0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="6b96f-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="6b96f-176">**SyncOnGreenVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="6b96f-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b96f-177">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6b96f-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6b96f-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b96f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b96f-179">Indica si se admite la sincronización en verde.</span><span class="sxs-lookup"><span data-stu-id="6b96f-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="6b96f-180">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-180">Value</span></span>                                                                              | <span data-ttu-id="6b96f-181">Significado</span><span class="sxs-lookup"><span data-stu-id="6b96f-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6b96f-182"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b96f-183">Se admite la sincronización en vídeo verde.</span><span class="sxs-lookup"><span data-stu-id="6b96f-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="6b96f-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6b96f-185">No se admite la sincronización en vídeo verde.</span><span class="sxs-lookup"><span data-stu-id="6b96f-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b96f-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b96f-186">Requirements</span></span>



| <span data-ttu-id="6b96f-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b96f-187">Requirement</span></span> | <span data-ttu-id="6b96f-188">Value</span><span class="sxs-lookup"><span data-stu-id="6b96f-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b96f-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b96f-189">Minimum supported client</span></span><br/> | <span data-ttu-id="6b96f-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b96f-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6b96f-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b96f-191">Minimum supported server</span></span><br/> | <span data-ttu-id="6b96f-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b96f-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b96f-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b96f-193">Namespace</span></span><br/>                | <span data-ttu-id="6b96f-194">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="6b96f-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6b96f-195">MOF</span><span class="sxs-lookup"><span data-stu-id="6b96f-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b96f-196"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b96f-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b96f-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b96f-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b96f-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b96f-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b96f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b96f-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6b96f-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




