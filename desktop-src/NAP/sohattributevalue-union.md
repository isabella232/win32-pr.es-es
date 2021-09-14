---
title: Unión de SoHAttributeValue (NapProtocol.h)
description: Define el contenido del miembro de tipo en una estructura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- Nap de unión de SoHAttributeValue
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161235"
---
# <a name="sohattributevalue-union"></a>Unión de SoHAttributeValue

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **unión SoHAttributeValue** define el contenido del miembro **de tipo** en una estructura [**SoHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) La estructura de la **unión SoHAttributeValue** viene determinada por el [**Valor SoHAttributeType**](sohattributetype-enum.md) especificado en el miembro **type** de la [**estructura SoHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Members

<dl> <dt>

**idVal**
</dt> <dd>

**case(sohAttributeTypeSystemHealthId)**

[SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del agente de mantenimiento del sistema (SHA) o del validador de estado del sistema (SHV) que construyó este [**paquete soH.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**case(sohAttributeTypeIpv4FixupServers)**

Las direcciones IPv4 de los servidores de corrección en uso por el sistema NAP.

<dl> <dt>

**count**
</dt> <dd>

Número de direcciones IPv4 del miembro **addresses** en el intervalo de 1 a [**maxIpv4CountPerSoHAttribute.**](nap-type-constants.md)

</dd> <dt>

**addresses**
</dt> <dd>

Matriz de [**estructuras Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) que contienen las direcciones IPv4.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**case(sohAttributeTypeIpv6FixupServers)**

Las direcciones IPv6 de los servidores de corrección en uso por el sistema NAP.

<dl> <dt>

**count**
</dt> <dd>

Número de direcciones IPv4 del miembro **addresses** en el intervalo de 1 a [**maxIpv6CountPerSoHAttribute.**](nap-type-constants.md)

</dd> <dt>

**addresses**
</dt> <dd>

Matriz de [**estructuras Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) que contienen las direcciones IPv4.

</dd> </dl> </dd> <dt>

**codesVal**
</dt> <dd>

**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**

Estructura [**ResultCodes que**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) contiene los códigos de resultados de cumplimiento definidos por la aplicación del cliente o [**las constantes de error nap**](nap-error-constants.md). Un [**paquete SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) debe contener este TLV o **sohAttributeTypeFailureCategory** TLV.

</dd> <dt>

**dateTimeVal**
</dt> <dd>

**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**

Estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contiene la hora de la última actualización [**de SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) o el tiempo **de generación de SoH.**

</dd> <dt>

**vendorSpecificVal**
</dt> <dd>

**case(sohAttributeTypeVendorSpecific)**

Datos específicos de la aplicación definidos por el proveedor.

<dl> <dt>

**vendorId**
</dt> <dd>

Identificador de 4 bytes que define el identificador de par SHA/SHV. Los tres primeros bytes son el código SMI asignado por IETF del proveedor y el último byte identifica el propio componente. Al implementar sha o SHV, no use los valores de identificador asignados a los componentes internos de mantenimiento del sistema de Microsoft en [**las constantes del proveedor nap**](nap-vendor-constants.md).

</dd> <dt>

**size**
</dt> <dd>

Tamaño, en bytes, de los datos del proveedor en el intervalo de 0 a ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).

</dd> <dt>

**vendorSpecificData**
</dt> <dd>

Puntero a los datos específicos del proveedor en orden de bytes de red.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**

Clase de mantenimiento, categoría de error o estado de aislamiento extendido de un componente NAP como un [**valor HealthClassValue**](healthclassvalue-enum.md) o [**FailureCategory,**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) o una [**estructura IsolationInfoEx.**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)

</dd> <dt>

**octetStringVal**
</dt> <dd>

**default**

Los valores de los atributos siguientes son cadenas de octeto:

-   sohAttributeTypeSoftwareVersion
-   sohAttributeTypeClientId
-   sohAttributeTypeProductName
-   sohAttributeTypeHealthClassStatus

Por compatibilidad con versiones adicionales, todos los atributos no reconocidos se devuelven como cadenas de octeto. **los datos** deben estar en orden de bytes de red.

<dl> <dt>

**size**
</dt> <dd>

Tamaño, en bytes, de **los datos** del intervalo de 0 a [**maxSoHAttributeSize.**](nap-type-constants.md)

</dd> <dt>

**data**
</dt> <dd>

Puntero al valor de cadena de octeto.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Diseño de datos real

Debido a la naturaleza del entorno de publicación del SDK, las uniones no se representan claramente en bloques de sintaxis. Esta es la sintaxis real del archivo de encabezado NapProtocol.h.


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



## <a name="remarks"></a>Observaciones

El sistema NAP consume estos tipos de atributo:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

El resto de [**los SoHAttributeTypes**](sohattributetype-enum.md) están diseñados exclusivamente como instrucciones preceptivas para su uso por parte de SHAs y SHV.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de NAP](nap-reference.md)
</dt> <dt>

[Estructuras nap](nap-structures.md)
</dt> </dl>

 

