---
title: Método CreateInstanceFromPropertyData de la MicrosoftDNS_RPType clase
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de persona responsable (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- Dns del método CreateInstanceFromPropertyData
- Método DNS CreateInstanceFromPropertyData , MicrosoftDNS_RPType clase
- MicrosoftDNS_RPType clase DNS , método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9493a3ad57e8a30ed08f11b22e35514eb4b58df35a1291987a62dc1840e79c56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642215"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a>Método CreateInstanceFromPropertyData de la clase MICROSOFTDNS \_ RPType

El **método CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de persona responsable (RP).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DnsServerName* \[ En\]
</dt> <dd>

FQDN o dirección IP del servidor DNS que contiene este RR.

</dd> <dt>

*ContainerName* \[ En\]
</dt> <dd>

Nombre del contenedor de la instancia de Zone, Cache o RootHints que contiene este RR.

</dd> <dt>

*OwnerName* \[ En\]
</dt> <dd>

Nombre del propietario del RR.

</dd> <dt>

*RecordClass* \[ en, opcional\]
</dt> <dd>

Clase del RR. El valor predeterminado es 1. Los valores siguientes son válidos.



| Value                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*RPMailbox* \[ En\]
</dt> <dd>

FQDN que especifica el buzón para la persona responsable.

</dd> <dt>

*TXTDomainName* \[ En\]
</dt> <dd>

FQDN para el que existen registros de recursos TXT.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpType de MicrosoftDNS \_**](microsoftdns-rptype.md)
</dt> <dt>

[**Método Modify de la clase RPType de MicrosoftDNS \_**](microsoftdns-rptype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





