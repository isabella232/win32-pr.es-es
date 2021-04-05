---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_WINSType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos del servicio de nombres Internet de Windows (WINS).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802834"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSType

El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos del servicio de nombres Internet de Windows (WINS).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DnsServerName* \[ de\]
</dt> <dd>

FQDN o dirección IP del servidor DNS que contiene este RR.

</dd> <dt>

*ContainerName* \[ de\]
</dt> <dd>

Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.

</dd> <dt>

*Nombrepropietario* \[ de\]
</dt> <dd>

Nombre del propietario del RR.

</dd> <dt>

*RecordClass* \[ en, opcional\]
</dt> <dd>

Clase del RR. El valor predeterminado es 1. Los valores siguientes son válidos.



| Value                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | EN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MappingFlag* \[ de\]
</dt> <dd>

Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona. Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente. Los valores siguientes son válidos.



| Value                                                                                                                                               | Significado                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Marca de replicación<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Marca de no replicación (registro local)<br/> |



 

</dd> <dt>

*Tiempodeesperadebúsqueda* \[ de\]
</dt> <dd>

Tiempo, en segundos, que un servidor DNS intenta resolver mediante la búsqueda de WINS.

</dd> <dt>

*CacheTimeout* \[ de\]
</dt> <dd>

Tiempo, en segundos, que un servidor DNS que usa WINS buscan puede almacenar en caché la respuesta del servidor WINS.

</dd> <dt>

*WinsServers* \[ de\]
</dt> <dd>

Lista de direcciones IP separadas por comas de los servidores WINS utilizados en WINS looks.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al nuevo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS WINSType**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





