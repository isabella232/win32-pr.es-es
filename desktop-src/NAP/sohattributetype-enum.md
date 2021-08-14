---
title: Enumeración SoHAttributeType (NapProtocol.h)
description: Especifica el tipo de atributo almacenado en el objeto type-length-value (TLV) del atributo.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- NAP de enumeración SoHAttributeType
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
ms.openlocfilehash: 1c3fabf3a8911274b912f3762dd07d0c64fc4111d22e372d1962a92221f1d068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939062"
---
# <a name="sohattributetype-enumeration"></a>Enumeración SoHAttributeType

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **enumeración SoHAttributeType** especifica el tipo de atributo almacenado en el objeto type-length-value (TLV) del atributo.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**
</dt> <dd>

Especifica el tipo de atributo de identificador de estado del sistema.

</dd> <dt>

<span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**
</dt> <dd>

Especifica el tipo de atributo de servidor de corrección IPv4.

</dd> <dt>

<span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**
</dt> <dd>

Especifica el tipo de atributo de código de resultado de cumplimiento.

</dd> <dt>

<span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**
</dt> <dd>

Especifica la hora del último tipo de atributo de actualización.

</dd> <dt>

<span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**
</dt> <dd>

Especifica el tipo de atributo id. de cliente.

</dd> <dt>

<span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**
</dt> <dd>

Especifica el tipo de atributo específico del proveedor.

</dd> <dt>

<span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**
</dt> <dd>

Especifica el tipo de atributo de clase de mantenimiento.

</dd> <dt>

<span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**
</dt> <dd>

Especifica el tipo de atributo de versión de software.

</dd> <dt>

<span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**
</dt> <dd>

Especifica el tipo de atributo de nombre de producto.

</dd> <dt>

<span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**
</dt> <dd>

Especifica el tipo de atributo de estado de la clase de mantenimiento.

</dd> <dt>

<span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**
</dt> <dd>

Especifica el tiempo de generación del tipo de atributo Statement of Health.

</dd> <dt>

<span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**
</dt> <dd>

Especifica el tipo de atributo de código de error.

</dd> <dt>

<span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**
</dt> <dd>

Especifica el tipo de atributo de categoría de error.

</dd> <dt>

<span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**
</dt> <dd>

Especifica el tipo de atributo de servidor de corrección IPv6.

</dd> <dt>

<span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**
</dt> <dd>

Especifica el tipo de atributo de estado de aislamiento extendido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**estructura SoHAttributeValue**](sohattributevalue-union.md) define los valores de atributo que corresponden a cada tipo de atributo.

El sistema NAP consume estos tipos de atributos:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

El resto de los tipos solo están diseñados para guiar el uso de SHAs y SHV.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SoHAttributeValue**](sohattributevalue-union.md)
</dt> <dt>

[**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





