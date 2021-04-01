---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_PTRType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de puntero (PTR).
ms.assetid: ff8beaca-fa0d-4294-8dab-3aa62baa3fe3
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6123b503fff1548b7fee3f643920b49ebacf636c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150257"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_ptrtype-class"></a>Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS PTRType

El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de puntero (PTR).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
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

*PTRDomainName* \[ de\]
</dt> <dd>

Cadena que representa la dirección del nombre de dominio del registro PTR.

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

[**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS PTRType**](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





