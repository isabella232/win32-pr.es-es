---
title: Enumeración SoHAttributeType (NapProtocol. h)
description: Especifica el tipo de atributo almacenado en el objeto tipo-longitud-valor (TLV) del atributo.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- NAP de enumeración de SoHAttributeType
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359796"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="5586b-104">Enumeración SoHAttributeType</span><span class="sxs-lookup"><span data-stu-id="5586b-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="5586b-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5586b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5586b-106">La enumeración **SoHAttributeType** especifica el tipo de atributo almacenado en el objeto tipo-longitud-valor (TLV) del atributo.</span><span class="sxs-lookup"><span data-stu-id="5586b-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5586b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5586b-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="5586b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5586b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5586b-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span><span class="sxs-lookup"><span data-stu-id="5586b-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-110">Especifica el tipo de atributo de ID. de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="5586b-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="5586b-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-112">Especifica el tipo de atributo de servidor de corrección de IPv4.</span><span class="sxs-lookup"><span data-stu-id="5586b-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span><span class="sxs-lookup"><span data-stu-id="5586b-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-114">Especifica el tipo de atributo de código de resultado de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="5586b-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span><span class="sxs-lookup"><span data-stu-id="5586b-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-116">Especifica la hora del último tipo de atributo de actualización.</span><span class="sxs-lookup"><span data-stu-id="5586b-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span><span class="sxs-lookup"><span data-stu-id="5586b-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-118">Especifica el tipo de atributo de ID. de cliente.</span><span class="sxs-lookup"><span data-stu-id="5586b-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="5586b-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-120">Especifica el tipo de atributo específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5586b-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span><span class="sxs-lookup"><span data-stu-id="5586b-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-122">Especifica el tipo de atributo de clase de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5586b-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="5586b-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-124">Especifica el tipo de atributo de versión de software.</span><span class="sxs-lookup"><span data-stu-id="5586b-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span><span class="sxs-lookup"><span data-stu-id="5586b-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-126">Especifica el tipo de atributo Product Name.</span><span class="sxs-lookup"><span data-stu-id="5586b-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span><span class="sxs-lookup"><span data-stu-id="5586b-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-128">Especifica el tipo de atributo de estado de clase de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5586b-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span><span class="sxs-lookup"><span data-stu-id="5586b-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-130">Especifica la hora de generación del informe de tipo de atributo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5586b-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span><span class="sxs-lookup"><span data-stu-id="5586b-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-132">Especifica el tipo de atributo del código de error.</span><span class="sxs-lookup"><span data-stu-id="5586b-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span><span class="sxs-lookup"><span data-stu-id="5586b-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-134">Especifica el tipo de atributo de categoría de error.</span><span class="sxs-lookup"><span data-stu-id="5586b-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="5586b-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-136">Especifica el tipo de atributo de servidor de corrección de IPv6.</span><span class="sxs-lookup"><span data-stu-id="5586b-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="5586b-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span><span class="sxs-lookup"><span data-stu-id="5586b-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="5586b-138">Especifica el tipo de atributo de estado de aislamiento extendido.</span><span class="sxs-lookup"><span data-stu-id="5586b-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5586b-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5586b-139">Remarks</span></span>

<span data-ttu-id="5586b-140">La estructura [**SoHAttributeValue**](sohattributevalue-union.md) define los valores de atributo que corresponden a cada tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="5586b-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="5586b-141">Estos tipos de atributo los consume el sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="5586b-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="5586b-142">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="5586b-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="5586b-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="5586b-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="5586b-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="5586b-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="5586b-145">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="5586b-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="5586b-146">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="5586b-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="5586b-147">El resto de los tipos solo está pensado para guiar el uso por parte de los Sha y los SHV.</span><span class="sxs-lookup"><span data-stu-id="5586b-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5586b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5586b-148">Requirements</span></span>



| <span data-ttu-id="5586b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="5586b-149">Requirement</span></span> | <span data-ttu-id="5586b-150">Value</span><span class="sxs-lookup"><span data-stu-id="5586b-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5586b-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5586b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5586b-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5586b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5586b-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5586b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5586b-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5586b-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5586b-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5586b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="5586b-156"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="5586b-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="5586b-157">IDL</span><span class="sxs-lookup"><span data-stu-id="5586b-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5586b-158"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5586b-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5586b-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="5586b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5586b-160">**SoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="5586b-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="5586b-161">**SoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="5586b-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="5586b-162">**SoH**</span><span class="sxs-lookup"><span data-stu-id="5586b-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="5586b-163">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="5586b-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="5586b-164">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="5586b-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





