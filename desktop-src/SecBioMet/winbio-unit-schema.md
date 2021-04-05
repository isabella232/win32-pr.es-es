---
title: Estructura de WINBIO_UNIT_SCHEMA (Winbio \_ Types. h)
description: Describe las capacidades de una unidad biométrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- Plataforma de biometría de Windows API de WINBIO_UNIT_SCHEMA Structure
- PWINBIO_UNIT_SCHEMA de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997079"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="1e430-105">Estructura de esquema de \_ unidad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="1e430-106">La estructura de **\_ \_ esquema de unidad WINBIO** describe las capacidades de una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="1e430-107">Lo utiliza la función [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .</span><span class="sxs-lookup"><span data-stu-id="1e430-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e430-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e430-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="1e430-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e430-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e430-110">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="1e430-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-111">Valor que identifica la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-112">**PoolType**</span><span class="sxs-lookup"><span data-stu-id="1e430-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-113">Valor **ULong** que especifica el tipo de la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="1e430-114">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1e430-114">This can be one of the following values:</span></span>



| <span data-ttu-id="1e430-115">Value</span><span class="sxs-lookup"><span data-stu-id="1e430-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="1e430-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1e430-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="1e430-117"><dt>**Grupo de WINBIO \_ \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="1e430-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="1e430-118">Se desconoce el tipo.</span><span class="sxs-lookup"><span data-stu-id="1e430-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="1e430-119"><dt>**\_sistema de grupo de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e430-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="1e430-120">La sesión se conecta a una colección compartida de unidades biométricas administradas por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="1e430-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="1e430-121"><dt>**Grupo de WINBIO \_ \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="1e430-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="1e430-122">La sesión se conecta a una colección de unidades biométricas administradas por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1e430-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="1e430-123">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="1e430-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-124">Valor que especifica el tipo de unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="1e430-125">Actualmente solo se admite la **\_ \_ huella digital de tipo WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="1e430-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-126">**SensorSubType**</span><span class="sxs-lookup"><span data-stu-id="1e430-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-127">Un subtipo de sensor definido para el tipo biométrico especificado por el miembro **BiometricFactor** .</span><span class="sxs-lookup"><span data-stu-id="1e430-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="1e430-128">Actualmente solo se admiten los tipos de huellas digitales (WINBIO de tipo de huella **\_ \_ digital**).</span><span class="sxs-lookup"><span data-stu-id="1e430-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="1e430-129">Los siguientes subtipos están definidos actualmente para huellas digitales:</span><span class="sxs-lookup"><span data-stu-id="1e430-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="1e430-130">subtipo de sensor de WINBIO \_ \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="1e430-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="1e430-131">WINBIO \_ de \_ subtipo de sensor FP \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e430-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="1e430-132">\_toque de \_ subtipo de sensor FP \_ \_ de WINBIO</span><span class="sxs-lookup"><span data-stu-id="1e430-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="1e430-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1e430-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-134">Una máscara de la funcionalidad del sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="1e430-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="1e430-135">Puede ser **una operación OR bit a bit** de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1e430-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="1e430-136">\_sensor de capacidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="1e430-137">coincidencia de la \_ funcionalidad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="1e430-138">base de datos de \_ capacidad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="1e430-139">procesamiento de la capacidad de WINBIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e430-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="1e430-140">\_cifrado de capacidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="1e430-141">navegación por la \_ funcionalidad WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="1e430-142">\_indicador de capacidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="1e430-143">\_ \_ sensor virtual de capacidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1e430-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="1e430-144">La constante del **\_ \_ \_ sensor virtual de la funcionalidad WINBIO** solo se aplica a Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1e430-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="1e430-145">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="1e430-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-146">Valor de cadena que contiene el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e430-146">A string value that contains the device ID.</span></span> <span data-ttu-id="1e430-147">La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="1e430-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-148">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e430-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-149">Valor de cadena que contiene una descripción de la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="1e430-150">La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="1e430-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-151">**Le**</span><span class="sxs-lookup"><span data-stu-id="1e430-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-152">Valor de cadena que contiene el nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="1e430-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="1e430-153">La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="1e430-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-154">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="1e430-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-155">Valor de cadena que contiene el número de modelo de la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="1e430-156">La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="1e430-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1e430-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-158">Una cadena Unicode terminada en **null** que contiene el número de serie de la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="1e430-159">La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.</span><span class="sxs-lookup"><span data-stu-id="1e430-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1e430-160">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="1e430-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1e430-161">Una estructura de [**\_ versión de WINBIO**](winbio-version.md) que contiene los números de versión principal y secundaria para la unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1e430-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e430-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e430-162">Requirements</span></span>



| <span data-ttu-id="1e430-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e430-163">Requirement</span></span> | <span data-ttu-id="1e430-164">Value</span><span class="sxs-lookup"><span data-stu-id="1e430-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e430-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e430-165">Minimum supported client</span></span><br/> | <span data-ttu-id="1e430-166">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e430-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1e430-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e430-167">Minimum supported server</span></span><br/> | <span data-ttu-id="1e430-168">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e430-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1e430-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e430-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e430-170"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e430-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e430-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e430-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e430-172">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="1e430-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="1e430-173">**WinBioEnumBiometricUnits**</span><span class="sxs-lookup"><span data-stu-id="1e430-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





