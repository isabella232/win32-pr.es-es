---
title: SoHAttributeValue Union (NapProtocol. h)
description: Define el contenido del miembro de tipo en una estructura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- SoHAttributeValue Union NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492334"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="a9141-104">Unión SoHAttributeValue</span><span class="sxs-lookup"><span data-stu-id="a9141-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="a9141-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9141-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a9141-106">La Unión **SoHAttributeValue** define el contenido del miembro de **tipo** en una estructura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="a9141-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="a9141-107">La estructura de la Unión **SoHAttributeValue** viene determinada por el [**SoHAttributeType**](sohattributetype-enum.md) especificado en el miembro de **tipo** de la estructura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="a9141-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9141-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9141-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="a9141-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9141-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9141-110">**idVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-111">**caso (sohAttributeTypeSystemHealthId)**</span><span class="sxs-lookup"><span data-stu-id="a9141-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="a9141-112">Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del agente de mantenimiento del sistema (SHA) o el validador de mantenimiento del sistema (SHV) que construyó este paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="a9141-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="a9141-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-114">**caso (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="a9141-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="a9141-115">Las direcciones IPv4 de los servidores de corrección en uso por el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a9141-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="a9141-116">**count**</span><span class="sxs-lookup"><span data-stu-id="a9141-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-117">El número de direcciones IPv4 en el miembro **Addresses** en el intervalo de 1 a [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9141-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9141-118">**addresses**</span><span class="sxs-lookup"><span data-stu-id="a9141-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-119">Una matriz de estructuras [**direcciónipv4**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) que contienen las direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="a9141-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9141-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-121">**caso (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="a9141-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="a9141-122">Las direcciones IPv6 de los servidores de corrección en uso por el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a9141-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="a9141-123">**count**</span><span class="sxs-lookup"><span data-stu-id="a9141-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-124">El número de direcciones IPv4 en el miembro **Addresses** en el intervalo de 1 a [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9141-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9141-125">**addresses**</span><span class="sxs-lookup"><span data-stu-id="a9141-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-126">Una matriz de estructuras [**DirecciónIPv6**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) que contienen las direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="a9141-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9141-127">**codesVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-128">**Case (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span><span class="sxs-lookup"><span data-stu-id="a9141-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="a9141-129">Una estructura [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) que contiene los códigos de resultado de compatibilidad definidos por la aplicación de las [**constantes de error**](nap-error-constants.md)de cliente o NAP.</span><span class="sxs-lookup"><span data-stu-id="a9141-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="a9141-130">Un paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) debe contener este TLV o el TLV **sohAttributeTypeFailureCategory** .</span><span class="sxs-lookup"><span data-stu-id="a9141-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="a9141-131">**dateTimeVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-132">**Case (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span><span class="sxs-lookup"><span data-stu-id="a9141-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="a9141-133">Una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene la hora de la última actualización de [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) o la hora de generación de **SOH** .</span><span class="sxs-lookup"><span data-stu-id="a9141-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="a9141-134">**vendorSpecificVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-135">**caso (sohAttributeTypeVendorSpecific)**</span><span class="sxs-lookup"><span data-stu-id="a9141-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="a9141-136">Datos específicos de la aplicación definidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a9141-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="a9141-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="a9141-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-138">Identificador de 4 bytes que define el identificador de par SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="a9141-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="a9141-139">Los primeros 3 bytes son el código SMI asignado por IETF del proveedor y el último byte identifica el propio componente.</span><span class="sxs-lookup"><span data-stu-id="a9141-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="a9141-140">Al implementar un SHA o SHV, no use los valores de identificador asignados a los componentes internos de mantenimiento del sistema de Microsoft en las [**constantes de proveedor de NAP**](nap-vendor-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9141-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9141-141">**size**</span><span class="sxs-lookup"><span data-stu-id="a9141-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-142">Tamaño, en bytes, de los datos del proveedor en el intervalo de 0 a ([**maxSoHAttributeSize**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="a9141-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="a9141-143">**vendorSpecificData**</span><span class="sxs-lookup"><span data-stu-id="a9141-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-144">Puntero a los datos específicos del proveedor en el orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="a9141-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9141-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="a9141-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-146">**Case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**</span><span class="sxs-lookup"><span data-stu-id="a9141-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="a9141-147">La clase de estado, la categoría de error o el estado de aislamiento extendido de un componente NAP como un valor de [**HealthClassValue**](healthclassvalue-enum.md) o [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) , o una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="a9141-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a9141-148">**octetStringVal**</span><span class="sxs-lookup"><span data-stu-id="a9141-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-149">**default**</span><span class="sxs-lookup"><span data-stu-id="a9141-149">**default**</span></span>

<span data-ttu-id="a9141-150">Los valores de los atributos siguientes son cadenas de octeto:</span><span class="sxs-lookup"><span data-stu-id="a9141-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="a9141-151">sohAttributeTypeSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="a9141-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="a9141-152">sohAttributeTypeClientId</span><span class="sxs-lookup"><span data-stu-id="a9141-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="a9141-153">sohAttributeTypeProductName</span><span class="sxs-lookup"><span data-stu-id="a9141-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="a9141-154">sohAttributeTypeHealthClassStatus</span><span class="sxs-lookup"><span data-stu-id="a9141-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="a9141-155">En cuanto a la compatibilidad con versiones posteriores, todos los atributos no reconocidos se devuelven como cadenas de octeto.</span><span class="sxs-lookup"><span data-stu-id="a9141-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="a9141-156">los **datos** deben estar en el orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="a9141-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="a9141-157">**size**</span><span class="sxs-lookup"><span data-stu-id="a9141-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-158">Tamaño, en bytes, de los **datos** del intervalo de 0 a [**maxSoHAttributeSize**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9141-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9141-159">**data**</span><span class="sxs-lookup"><span data-stu-id="a9141-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="a9141-160">Puntero al valor de la cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="a9141-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="a9141-161">Diseño de datos real</span><span class="sxs-lookup"><span data-stu-id="a9141-161">Actual data layout</span></span>

<span data-ttu-id="a9141-162">Debido a la naturaleza del entorno de publicación de SDK, las uniones no se representan claramente en bloques de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="a9141-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="a9141-163">Esta es la sintaxis real del archivo de encabezado NapProtocol. h.</span><span class="sxs-lookup"><span data-stu-id="a9141-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="a9141-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9141-164">Remarks</span></span>

<span data-ttu-id="a9141-165">Estos tipos de atributo los consume el sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="a9141-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="a9141-166">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="a9141-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="a9141-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="a9141-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="a9141-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="a9141-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="a9141-169">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="a9141-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="a9141-170">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="a9141-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="a9141-171">El resto de los [**SoHAttributeTypes**](sohattributetype-enum.md) están pensados exclusivamente como instrucciones prescriptivas para el uso por parte de los Sha y los SHV.</span><span class="sxs-lookup"><span data-stu-id="a9141-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9141-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9141-172">Requirements</span></span>



| <span data-ttu-id="a9141-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9141-173">Requirement</span></span> | <span data-ttu-id="a9141-174">Value</span><span class="sxs-lookup"><span data-stu-id="a9141-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9141-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9141-175">Minimum supported client</span></span><br/> | <span data-ttu-id="a9141-176">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a9141-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9141-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9141-177">Minimum supported server</span></span><br/> | <span data-ttu-id="a9141-178">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9141-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a9141-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9141-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9141-180"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9141-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9141-181">IDL</span><span class="sxs-lookup"><span data-stu-id="a9141-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9141-182"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9141-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9141-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9141-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9141-184">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="a9141-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="a9141-185">Estructuras de NAP</span><span class="sxs-lookup"><span data-stu-id="a9141-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

