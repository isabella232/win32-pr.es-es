---
title: Constantes de tipo NAP (NapTypes.h)
description: Se definen las siguientes constantes nap.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0201f29d19969de6050ce3eeebf29a7bee73792dcc6b61b2359e5660db12d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685925"
---
# <a name="nap-type-constants"></a>Constantes de tipo NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Se definen las siguientes constantes nap.

Las siguientes constantes nap se definen en NapTypes.h:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Número máximo de [**objetos SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) asociados a un [**paquete SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Tamaño máximo, en bytes, de un [**objeto SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) asociado a un paquete de instrucción de mantenimiento [**(SoH).**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



Tamaño mínimo, en bytes, de un [**paquete SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Tamaño máximo, en bytes, de un [**paquete SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/ sizeof(DWORD)
</dt> <dt>



Número máximo de valores DWORD asociados a [**soHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



Número máximo de direcciones IPv4 asociadas a [**soHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



Número máximo de direcciones IPv6 asociadas a [**soHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Longitud máxima de una cadena especificada por la [**estructura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

(maxStringLength + 1) \* sizeof(WCHAR)
</dt> <dt>



Longitud máxima, en bytes, de una cadena especificada por la [**estructura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Número máximo de entidades de mantenimiento del sistema, como SHV y SHA.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxSystemHealthEntityCount)\] 
</dt> <dt>



Intervalo de valores posibles para el número de entidades de mantenimiento del sistema.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Número máximo de entidades de cumplimiento, como los QEC.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxEnforcerCount)\]
</dt> <dt>



Intervalo de valores posibles para el número de entidades de cumplimiento.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



Tamaño máximo, en bytes, de una [**estructura PrivateData.**](/windows/win32/api/naptypes/ns-naptypes-privatedata)


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Número máximo de [**objetos INapEnforcementClientConnection**](inapenforcementclientconnection.md) asociados a una entidad de cumplimiento.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



Número máximo de conexiones SoH almacenadas en caché para todas las entidades de cumplimiento y mantenimiento del sistema.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Especifica que [**soHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)se debe a una nueva solicitud, no a una solicitud almacenada en caché. El agente NAP usa esta marca en un [**objeto INapEnforcementClientConnection.**](inapenforcementclientconnection.md)


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Especifica que se requiere una corrección. Sha usa esta marca.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Número de categorías de error contenidas en una [**estructura FailureCategoryMapping.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



El componente es un cliente de cumplimiento de cuarentena (QEC) que envía un [**paquete SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) en banda durante la autenticación de conexión.

> [!Note]  
> Este valor no lo usan las SHA y SHV.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



El componente es un QEC que implementa [**INapCertRelyingParty**](inapcertrelyingparty.md) y debe interactuar con el servidor de certificados de mantenimiento (HCS) para obtener un certificado de mantenimiento.

> [!Note]  
> Este valor no lo usan las SHA y SHV.

 


</dt> </dl> </dd> </dl>

Las siguientes constantes nap se definen en NapEnforcementClient.h.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



Tamaño máximo predeterminado, en bytes, de un paquete SoH.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Tamaño máximo posible, en bytes, de un paquete SoH.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



El tamaño máximo más pequeño posible, en bytes, de un paquete SoH. El tamaño real del paquete SoH puede ser menor que **minProtocolMaxSize.**


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

range(minProtocolMaxSize, maxProtocolMaxSize)
</dt> <dt>



Intervalo de valores posibles para el tamaño máximo de un paquete SoH.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes nap**](nap-constants.md)
</dt> </dl>

 

 





