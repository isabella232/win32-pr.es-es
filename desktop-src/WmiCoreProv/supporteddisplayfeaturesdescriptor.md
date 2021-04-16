---
description: Representa las características de presentación admitidas del monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Clase SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705883"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="4f670-103">Clase SupportedDisplayFeaturesDescriptor</span><span class="sxs-lookup"><span data-stu-id="4f670-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="4f670-104">**SupportedDisplayFeaturesDescriptor** representa las características de presentación admitidas del monitor.</span><span class="sxs-lookup"><span data-stu-id="4f670-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="4f670-105">La información de esta clase se corresponde con los datos de la definición de entrada de vídeo de la estándar de identificación de vídeo electrónica (VESA) de la asociación mejorada de visualización de datos (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="4f670-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f670-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f670-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="4f670-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f670-107">Members</span></span>

<span data-ttu-id="4f670-108">La clase **SupportedDisplayFeaturesDescriptor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f670-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="4f670-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f670-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f670-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f670-110">Properties</span></span>

<span data-ttu-id="4f670-111">La clase **SupportedDisplayFeaturesDescriptor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4f670-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f670-112">**ActiveOffSupported**</span><span class="sxs-lookup"><span data-stu-id="4f670-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-115">Compatibilidad con la energía activa y muy baja.</span><span class="sxs-lookup"><span data-stu-id="4f670-115">Support for active off and very low power.</span></span> <span data-ttu-id="4f670-116">La pantalla consume menos energía cuando recibe una señal de tiempo que está fuera del intervalo operativo activo declarado.</span><span class="sxs-lookup"><span data-stu-id="4f670-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="4f670-117">La pantalla volverá al funcionamiento normal si la señal de temporización vuelve al intervalo operativo normal.</span><span class="sxs-lookup"><span data-stu-id="4f670-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="4f670-118">Algunos ejemplos de señales de control de tiempo fuera del intervalo operativo normal son las señales de sincronización o la ausencia DE señal.</span><span class="sxs-lookup"><span data-stu-id="4f670-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="4f670-119">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="4f670-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-120">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4f670-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-122">Tipo de pantalla para el monitor.</span><span class="sxs-lookup"><span data-stu-id="4f670-122">Type of display for the monitor.</span></span> <span data-ttu-id="4f670-123">En la tabla siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4f670-123">The following table lists possible values.</span></span>



| <span data-ttu-id="4f670-124">Value</span><span class="sxs-lookup"><span data-stu-id="4f670-124">Value</span></span>                                                                              | <span data-ttu-id="4f670-125">Significado</span><span class="sxs-lookup"><span data-stu-id="4f670-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="4f670-126"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="4f670-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4f670-127">Pantalla monocroma/escala de grises</span><span class="sxs-lookup"><span data-stu-id="4f670-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="4f670-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4f670-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="4f670-129">Presentación de color RGB</span><span class="sxs-lookup"><span data-stu-id="4f670-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="4f670-130"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="4f670-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="4f670-131">Pantalla multicolor no RGB</span><span class="sxs-lookup"><span data-stu-id="4f670-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4f670-132">**GTFSupported**</span><span class="sxs-lookup"><span data-stu-id="4f670-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-135">Indica si la pantalla tiene compatibilidad con GTF.</span><span class="sxs-lookup"><span data-stu-id="4f670-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="4f670-136">Si **es true**, la pantalla admite los tiempos basados en el estándar GTF con los valores de parámetro GTF predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4f670-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="4f670-137">**HasPreferredTimingMode**</span><span class="sxs-lookup"><span data-stu-id="4f670-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-140">Indica si la pantalla tiene un modo de control de tiempo preferido.</span><span class="sxs-lookup"><span data-stu-id="4f670-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="4f670-141">Si **es true**, el primer bloque de tiempo detallado contiene el modo de control de tiempo preferido del monitor.</span><span class="sxs-lookup"><span data-stu-id="4f670-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="4f670-142">El uso del modo de control de tiempo preferido es necesario para EDID v. 1.3 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4f670-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="4f670-143">**sRGBSupported**</span><span class="sxs-lookup"><span data-stu-id="4f670-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-146">Si **es true**, la pantalla admite sRGB.</span><span class="sxs-lookup"><span data-stu-id="4f670-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="4f670-147">**StandbySupported**</span><span class="sxs-lookup"><span data-stu-id="4f670-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-150">Indica si la pantalla es compatible con el modo de espera de la señal de administración de energía (DPMS) de pantalla VESA.</span><span class="sxs-lookup"><span data-stu-id="4f670-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="4f670-151">Si es **true**, se admite el modo de espera de DPMS.</span><span class="sxs-lookup"><span data-stu-id="4f670-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f670-152">**SuspendSupported**</span><span class="sxs-lookup"><span data-stu-id="4f670-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f670-153">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4f670-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f670-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f670-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f670-155">Indica si la pantalla admite la suspensión de la señal de administración de energía (DPMS) de pantalla VESA.</span><span class="sxs-lookup"><span data-stu-id="4f670-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="4f670-156">Si **es true**, se admite la suspensión de DPMS.</span><span class="sxs-lookup"><span data-stu-id="4f670-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f670-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f670-157">Requirements</span></span>



| <span data-ttu-id="4f670-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f670-158">Requirement</span></span> | <span data-ttu-id="4f670-159">Value</span><span class="sxs-lookup"><span data-stu-id="4f670-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f670-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f670-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4f670-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f670-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4f670-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f670-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4f670-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f670-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4f670-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f670-164">Namespace</span></span><br/>                | <span data-ttu-id="4f670-165">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="4f670-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4f670-166">MOF</span><span class="sxs-lookup"><span data-stu-id="4f670-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f670-167"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f670-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f670-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f670-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f670-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f670-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f670-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f670-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f670-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="4f670-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




