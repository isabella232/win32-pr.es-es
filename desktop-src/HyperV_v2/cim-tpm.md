---
description: Describe un dispositivo Módulo de plataforma segura (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: CIM_TPM (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082464"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="7e851-103">\_Clase TPM CIM</span><span class="sxs-lookup"><span data-stu-id="7e851-103">CIM\_TPM class</span></span>

<span data-ttu-id="7e851-104">Describe un dispositivo Módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="7e851-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e851-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e851-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="7e851-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e851-106">Members</span></span>

<span data-ttu-id="7e851-107">La **clase \_ TPM CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e851-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="7e851-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e851-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="7e851-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e851-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7e851-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e851-110">Methods</span></span>

<span data-ttu-id="7e851-111">La **clase \_ TPM CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7e851-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="7e851-112">Método</span><span class="sxs-lookup"><span data-stu-id="7e851-112">Method</span></span>                                                         | <span data-ttu-id="7e851-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e851-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e851-114">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="7e851-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="7e851-115">Cambia la credencial de autorización de propietario de un dispositivo de TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="7e851-116">**RequestTPMStateChange**</span><span class="sxs-lookup"><span data-stu-id="7e851-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="7e851-117">Solicita que el estado del TPM cambie al valor especificado en el parámetro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="7e851-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7e851-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e851-118">Properties</span></span>

<span data-ttu-id="7e851-119">La **clase \_ TPM CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e851-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e851-120">**AvailableRequestedTPMStates**</span><span class="sxs-lookup"><span data-stu-id="7e851-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-121">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e851-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e851-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-123">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**, CIM \_ TPMCapabilities. RequestedTPMStatesSupported ")</span><span class="sxs-lookup"><span data-stu-id="7e851-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-124">Los valores posibles para el parámetro *RequestedTPMState* del método [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="7e851-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e851-125">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7e851-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-126">**S1 habilitada: propiedad activa** (2)</span><span class="sxs-lookup"><span data-stu-id="7e851-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-127">**S2 deshabilitado-propiedad activa** (3)</span><span class="sxs-lookup"><span data-stu-id="7e851-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-128">**S3 habilitado: inactivo-propiedad** (4)</span><span class="sxs-lookup"><span data-stu-id="7e851-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-129">**S4 deshabilitado-inactivo-propiedad** (5)</span><span class="sxs-lookup"><span data-stu-id="7e851-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-130">**S5 habilitado-activo-no propietario** (6)</span><span class="sxs-lookup"><span data-stu-id="7e851-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-131">**S6 deshabilitado-activo-no propietario** (7)</span><span class="sxs-lookup"><span data-stu-id="7e851-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-132">**S7 habilitado: inactivo:** no tiene propiedad (8)</span><span class="sxs-lookup"><span data-stu-id="7e851-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-133">**S8 deshabilitado-inactivo:** no tiene propiedad (9)</span><span class="sxs-lookup"><span data-stu-id="7e851-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e851-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7e851-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e851-135">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7e851-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e851-136">**TPMManafucturerMajorRevision**</span><span class="sxs-lookup"><span data-stu-id="7e851-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e851-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| sección 5,3 \| versión \| revMajor ")</span><span class="sxs-lookup"><span data-stu-id="7e851-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-140">La revisión principal del fabricante del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-141">**TPMManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="7e851-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e851-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v1dot2 \| sección 21,6 \| TPM \_ Cap \_ version \_ info \| tpmVendorID ")</span><span class="sxs-lookup"><span data-stu-id="7e851-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-145">IDENTIFICADOR del fabricante del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-146">**TPMManufacturerInfo**</span><span class="sxs-lookup"><span data-stu-id="7e851-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e851-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-149">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v 1.2. sección de tcg \| 21,6 \| información de \_ versión del Cap de TPM \_ \_ \| vendorSpecific ")</span><span class="sxs-lookup"><span data-stu-id="7e851-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-150">Información adicional definida por el fabricante del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-151">**TPMManufacturerMinorRevision**</span><span class="sxs-lookup"><span data-stu-id="7e851-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e851-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-154">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| sección 5,3 \| versión \| revMinor ")</span><span class="sxs-lookup"><span data-stu-id="7e851-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-155">Revisión secundaria del fabricante del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-156">**TPMSpecMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="7e851-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e851-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-159">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| sección 5,3 \| versión \| principal "," TSS. Sección 2.3.2.18 de TCG de \| nivel 1 v 1.2 \| ")</span><span class="sxs-lookup"><span data-stu-id="7e851-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-160">Versión principal del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-161">**TPMSpecMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="7e851-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e851-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| sección 5,3 \| versión \| secundaria "," TSS. Sección 2.3.2.18 de TCG de \| nivel 1 v 1.2 \| ")</span><span class="sxs-lookup"><span data-stu-id="7e851-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-165">Versión secundaria del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="7e851-166">**TPMState**</span><span class="sxs-lookup"><span data-stu-id="7e851-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e851-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-169">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 1 v1dot2 \| sección 9,4 "," TPM. TCG \| Part 2 v1dot2 \| Section 7,1 \| TPM \_ Permanent \_ flags "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TransitioningToTPMState**")</span><span class="sxs-lookup"><span data-stu-id="7e851-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-170">Estado operativo del TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e851-171">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7e851-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-172">**S1 habilitada: propiedad activa** (2)</span><span class="sxs-lookup"><span data-stu-id="7e851-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-173">**S2 deshabilitado-propiedad activa** (3)</span><span class="sxs-lookup"><span data-stu-id="7e851-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-174">**S3 habilitado: inactivo-propiedad** (4)</span><span class="sxs-lookup"><span data-stu-id="7e851-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-175">**S4 deshabilitado-inactivo-propiedad** (5)</span><span class="sxs-lookup"><span data-stu-id="7e851-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-176">**S5 habilitado-activo-no propietario** (6)</span><span class="sxs-lookup"><span data-stu-id="7e851-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-177">**S6 deshabilitado-activo-no propietario** (7)</span><span class="sxs-lookup"><span data-stu-id="7e851-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-178">**S7 habilitado: inactivo:** no tiene propiedad (8)</span><span class="sxs-lookup"><span data-stu-id="7e851-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-179">**S8 deshabilitado-inactivo:** no tiene propiedad (9)</span><span class="sxs-lookup"><span data-stu-id="7e851-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7e851-180">**No aplicable** (10)</span><span class="sxs-lookup"><span data-stu-id="7e851-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e851-181">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7e851-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e851-182">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7e851-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e851-183">**TransitioningToTPMState**</span><span class="sxs-lookup"><span data-stu-id="7e851-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e851-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e851-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e851-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e851-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e851-186">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TPMState**")</span><span class="sxs-lookup"><span data-stu-id="7e851-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="7e851-187">Estado de destino al que está cambiando el TPM.</span><span class="sxs-lookup"><span data-stu-id="7e851-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e851-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7e851-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 habilitada: propiedad activa** (2)</span><span class="sxs-lookup"><span data-stu-id="7e851-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="7e851-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 deshabilitado-propiedad activa** (3)</span><span class="sxs-lookup"><span data-stu-id="7e851-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 habilitado: inactivo-propiedad** (4)</span><span class="sxs-lookup"><span data-stu-id="7e851-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="7e851-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 deshabilitado-inactivo-propiedad** (5)</span><span class="sxs-lookup"><span data-stu-id="7e851-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 habilitado-activo-no propietario** (6)</span><span class="sxs-lookup"><span data-stu-id="7e851-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 deshabilitado-activo-no propietario** (7)</span><span class="sxs-lookup"><span data-stu-id="7e851-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 habilitado: inactivo:** no tiene propiedad (8)</span><span class="sxs-lookup"><span data-stu-id="7e851-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="7e851-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 deshabilitado-inactivo:** no tiene propiedad (9)</span><span class="sxs-lookup"><span data-stu-id="7e851-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7e851-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (10)</span><span class="sxs-lookup"><span data-stu-id="7e851-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="7e851-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Sin cambios** (11)</span><span class="sxs-lookup"><span data-stu-id="7e851-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="7e851-199">(12)</span><span class="sxs-lookup"><span data-stu-id="7e851-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7e851-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7e851-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7e851-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7e851-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="7e851-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7e851-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7e851-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e851-203">Requirements</span></span>



| <span data-ttu-id="7e851-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e851-204">Requirement</span></span> | <span data-ttu-id="7e851-205">Value</span><span class="sxs-lookup"><span data-stu-id="7e851-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e851-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e851-206">Minimum supported client</span></span><br/> | <span data-ttu-id="7e851-207">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e851-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7e851-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e851-208">Minimum supported server</span></span><br/> | <span data-ttu-id="7e851-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e851-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e851-210">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e851-210">Namespace</span></span><br/>                | <span data-ttu-id="7e851-211">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7e851-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e851-212">MOF</span><span class="sxs-lookup"><span data-stu-id="7e851-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e851-213"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e851-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e851-214">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e851-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e851-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e851-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e851-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e851-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e851-217">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7e851-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

