---
description: Representa las características básicas de pantalla de un monitor de equipo.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Clase WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706820"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="985e3-103">Clase WmiMonitorBasicDisplayParams</span><span class="sxs-lookup"><span data-stu-id="985e3-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="985e3-104">La clase WMI **WmiMonitorBasicDisplayParams** representa las características básicas de pantalla de un monitor de equipo.</span><span class="sxs-lookup"><span data-stu-id="985e3-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="985e3-105">El valor de la propiedad **VideoInputType** indica si el monitor es analógico o digital.</span><span class="sxs-lookup"><span data-stu-id="985e3-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="985e3-106">Los datos de esta clase se corresponden con los datos del bloque básico de parámetros de presentación/características de la Asociación de vídeo electrónica estándar (VESA) estándar mejorado de identificación de visualización extendida (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="985e3-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="985e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="985e3-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="985e3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="985e3-108">Members</span></span>

<span data-ttu-id="985e3-109">La clase **WmiMonitorBasicDisplayParams** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="985e3-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="985e3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="985e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="985e3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="985e3-111">Properties</span></span>

<span data-ttu-id="985e3-112">La clase **WmiMonitorBasicDisplayParams** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="985e3-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="985e3-113">**Activo**</span><span class="sxs-lookup"><span data-stu-id="985e3-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="985e3-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-116">Indica el monitor activo.</span><span class="sxs-lookup"><span data-stu-id="985e3-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="985e3-117">**DisplayTransferCharacteristic**</span><span class="sxs-lookup"><span data-stu-id="985e3-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-118">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="985e3-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-120">Visualización de la característica de transferencia (100 \* gamma-100).</span><span class="sxs-lookup"><span data-stu-id="985e3-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="985e3-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="985e3-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="985e3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="985e3-124">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="985e3-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="985e3-125">Nombre de la instancia de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="985e3-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="985e3-126">**MaxHorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="985e3-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-127">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="985e3-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-129">Tamaño máximo de imagen horizontal en centímetros.</span><span class="sxs-lookup"><span data-stu-id="985e3-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="985e3-130">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="985e3-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="985e3-131">**MaxVerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="985e3-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-132">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="985e3-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-134">Tamaño máximo de imagen vertical en centímetros.</span><span class="sxs-lookup"><span data-stu-id="985e3-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="985e3-135">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="985e3-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="985e3-136">**SupportedDisplayFeatures**</span><span class="sxs-lookup"><span data-stu-id="985e3-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-137">Tipo de datos: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="985e3-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-139">Mostrar las características admitidas por el monitor.</span><span class="sxs-lookup"><span data-stu-id="985e3-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="985e3-140">**VideoInputType**</span><span class="sxs-lookup"><span data-stu-id="985e3-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="985e3-141">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="985e3-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="985e3-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="985e3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="985e3-143">Tipo de entrada de vídeo.</span><span class="sxs-lookup"><span data-stu-id="985e3-143">Video input type.</span></span>



| <span data-ttu-id="985e3-144">Value</span><span class="sxs-lookup"><span data-stu-id="985e3-144">Value</span></span>                                                                              | <span data-ttu-id="985e3-145">Significado</span><span class="sxs-lookup"><span data-stu-id="985e3-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="985e3-146"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="985e3-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="985e3-147">Analógico</span><span class="sxs-lookup"><span data-stu-id="985e3-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="985e3-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="985e3-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="985e3-149">Digital</span><span class="sxs-lookup"><span data-stu-id="985e3-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="985e3-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="985e3-150">Remarks</span></span>

<span data-ttu-id="985e3-151">**MaxHorizontalImageSize** y **MaxVerticalImageSize** representan las dimensiones de imagen máximas que el monitor puede mostrar correctamente para todo el conjunto de combinaciones de control de tiempo y formato admitidas.</span><span class="sxs-lookup"><span data-stu-id="985e3-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="985e3-152">La dimensión de imagen máxima se define mediante el estándar de definición de área de imagen de vídeo (VIAD) de VESA y se redondea al centímetro más cercano.</span><span class="sxs-lookup"><span data-stu-id="985e3-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="985e3-153">El sistema del equipo host puede usar estos datos para seleccionar el tamaño y la relación de aspecto de la imagen que permitirá el texto escalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="985e3-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="985e3-154">Tenga en cuenta que, si uno o ambos de estos campos son cero, el sistema no realiza suposiciones sobre el tamaño de presentación.</span><span class="sxs-lookup"><span data-stu-id="985e3-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="985e3-155">Por ejemplo, puede que el tamaño de una pantalla de proyección no esté determinado.</span><span class="sxs-lookup"><span data-stu-id="985e3-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="985e3-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="985e3-156">Requirements</span></span>



| <span data-ttu-id="985e3-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="985e3-157">Requirement</span></span> | <span data-ttu-id="985e3-158">Value</span><span class="sxs-lookup"><span data-stu-id="985e3-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="985e3-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="985e3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="985e3-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="985e3-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="985e3-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="985e3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="985e3-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="985e3-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="985e3-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="985e3-163">Namespace</span></span><br/>                | <span data-ttu-id="985e3-164">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="985e3-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="985e3-165">MOF</span><span class="sxs-lookup"><span data-stu-id="985e3-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="985e3-166"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="985e3-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="985e3-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="985e3-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="985e3-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="985e3-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985e3-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="985e3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985e3-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="985e3-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




