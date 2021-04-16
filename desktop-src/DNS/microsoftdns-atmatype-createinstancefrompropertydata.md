---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_ATMAType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de dirección ATM en nombre (ATMA).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656538"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a>Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType

El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de dirección ATM en nombre (Atma).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
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

*Formato* \[ de\]
</dt> <dd>

Formato de dirección ATM. Dos valores posibles para FORMAT son: 0, que indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 que indica el formato E. 164.

</dd> <dt>

*ATMAddress* \[ de\]
</dt> <dd>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR. Los primeros cuatro bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

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

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS ATMAType**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





