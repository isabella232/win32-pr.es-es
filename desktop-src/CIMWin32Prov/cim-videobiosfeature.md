---
description: La \_ clase CIM VideoBIOSFeature representa las capacidades del software de bajo nivel que se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659506"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="bee3a-103">\_Clase VideoBIOSFeature de CIM</span><span class="sxs-lookup"><span data-stu-id="bee3a-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="bee3a-104">La clase **CIM \_ VideoBIOSFeature** representa las capacidades del software de bajo nivel que se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="bee3a-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bee3a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bee3a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bee3a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bee3a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bee3a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bee3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bee3a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bee3a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee3a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bee3a-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="bee3a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bee3a-110">Members</span></span>

<span data-ttu-id="bee3a-111">La clase **CIM \_ VideoBIOSFeature** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bee3a-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="bee3a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bee3a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bee3a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bee3a-113">Properties</span></span>

<span data-ttu-id="bee3a-114">La clase **CIM \_ VideoBIOSFeature** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bee3a-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bee3a-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bee3a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bee3a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-119">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="bee3a-119">Short textual description of the object.</span></span>

<span data-ttu-id="bee3a-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bee3a-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-122">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bee3a-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-124">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica BIOS de vídeo DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**Características**")</span><span class="sxs-lookup"><span data-stu-id="bee3a-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-125">Cadenas de forma libre que proporcionan descripciones detalladas de las características del BIOS de vídeo indicadas en la matriz de **características** .</span><span class="sxs-lookup"><span data-stu-id="bee3a-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="bee3a-126">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **características** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="bee3a-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="bee3a-127">**Características**</span><span class="sxs-lookup"><span data-stu-id="bee3a-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-128">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bee3a-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-130">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica BIOS de vídeo DMTF \| 001,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="bee3a-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-131">Características admitidas por el BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bee3a-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="bee3a-132">Por ejemplo, se podría indicar la compatibilidad con la administración de energía VESA o el sombreado del BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bee3a-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="bee3a-133">El valor 3 ("desconocido") no es válido en el esquema CIM, ya que representa que no se admiten características del BIOS en DMI.</span><span class="sxs-lookup"><span data-stu-id="bee3a-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="bee3a-134">En ese caso, no se debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="bee3a-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bee3a-135">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bee3a-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bee3a-136">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="bee3a-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="bee3a-137">**Undefined** (3)</span><span class="sxs-lookup"><span data-stu-id="bee3a-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="bee3a-138">**BIOS de vídeo estándar** (4)</span><span class="sxs-lookup"><span data-stu-id="bee3a-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="bee3a-139">**Extensiones de BIOS VESA compatibles** (5)</span><span class="sxs-lookup"><span data-stu-id="bee3a-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="bee3a-140">**Compatibilidad con la administración de energía VESA** (6)</span><span class="sxs-lookup"><span data-stu-id="bee3a-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="bee3a-141">Se **admite el canal de datos de pantalla VESA** (7)</span><span class="sxs-lookup"><span data-stu-id="bee3a-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="bee3a-142">**Deshabilitación del BIOS de vídeo** (8)</span><span class="sxs-lookup"><span data-stu-id="bee3a-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="bee3a-143">**BIOS de vídeo actualizable** (9)</span><span class="sxs-lookup"><span data-stu-id="bee3a-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bee3a-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bee3a-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-147">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="bee3a-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-148">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="bee3a-148">Textual description of the object.</span></span>

<span data-ttu-id="bee3a-149">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="bee3a-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-153">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**IdentifyingNumber**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="bee3a-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-154">Identificación del producto, como un número de serie en software o un número de matriz en un chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="bee3a-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="bee3a-155">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bee3a-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-157">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bee3a-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-159">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="bee3a-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-160">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="bee3a-160">Date and time the object was installed.</span></span> <span data-ttu-id="bee3a-161">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="bee3a-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bee3a-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-163">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bee3a-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-166">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bee3a-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-167">Etiqueta por la que se conoce el objeto fuera del sistema de procesamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="bee3a-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="bee3a-168">Esta etiqueta es un nombre que identifica de forma única el elemento en el contexto del espacio de nombres del elemento.</span><span class="sxs-lookup"><span data-stu-id="bee3a-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="bee3a-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="bee3a-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-173">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Name**"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="bee3a-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-174">Nombre de producto usado comúnmente.</span><span class="sxs-lookup"><span data-stu-id="bee3a-174">Commonly used product name.</span></span>

<span data-ttu-id="bee3a-175">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-176">**Estado**</span><span class="sxs-lookup"><span data-stu-id="bee3a-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-179">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="bee3a-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-180">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="bee3a-180">Current status of the object.</span></span> <span data-ttu-id="bee3a-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bee3a-182">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bee3a-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bee3a-183">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="bee3a-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bee3a-184">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="bee3a-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bee3a-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="bee3a-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bee3a-186">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="bee3a-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bee3a-187">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="bee3a-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bee3a-188">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="bee3a-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bee3a-189">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="bee3a-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bee3a-190">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="bee3a-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bee3a-191">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="bee3a-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bee3a-192">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="bee3a-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bee3a-193">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="bee3a-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bee3a-194">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="bee3a-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bee3a-195">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="bee3a-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-198">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Vendor**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="bee3a-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-199">Nombre del proveedor del producto, que corresponde a la propiedad **Vendor** en el objeto Product del estándar de intercambio de soluciones DMTF (SES).</span><span class="sxs-lookup"><span data-stu-id="bee3a-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="bee3a-200">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="bee3a-201">**Versión**</span><span class="sxs-lookup"><span data-stu-id="bee3a-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bee3a-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bee3a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bee3a-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bee3a-204">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ producto CIM**](cim-product.md).**Versión**"), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="bee3a-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="bee3a-205">Información de versión del producto, que corresponde a la propiedad **version** en el objeto Product de los ses de DMTF.</span><span class="sxs-lookup"><span data-stu-id="bee3a-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="bee3a-206">Esta propiedad se hereda de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bee3a-207">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bee3a-207">Remarks</span></span>

<span data-ttu-id="bee3a-208">La clase **CIM \_ VideoBIOSFeature** se deriva de [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="bee3a-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="bee3a-209">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="bee3a-209">WMI does not implement this class.</span></span>

<span data-ttu-id="bee3a-210">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bee3a-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bee3a-211">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bee3a-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bee3a-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bee3a-212">Requirements</span></span>



| <span data-ttu-id="bee3a-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="bee3a-213">Requirement</span></span> | <span data-ttu-id="bee3a-214">Value</span><span class="sxs-lookup"><span data-stu-id="bee3a-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bee3a-215">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee3a-215">Minimum supported client</span></span><br/> | <span data-ttu-id="bee3a-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bee3a-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bee3a-217">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee3a-217">Minimum supported server</span></span><br/> | <span data-ttu-id="bee3a-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bee3a-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bee3a-219">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bee3a-219">Namespace</span></span><br/>                | <span data-ttu-id="bee3a-220">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bee3a-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bee3a-221">MOF</span><span class="sxs-lookup"><span data-stu-id="bee3a-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bee3a-222"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bee3a-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bee3a-223">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bee3a-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee3a-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee3a-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee3a-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="bee3a-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee3a-226">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="bee3a-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

