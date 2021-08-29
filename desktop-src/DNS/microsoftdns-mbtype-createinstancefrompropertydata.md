---
title: Método CreateInstanceFromPropertyData de la MicrosoftDNS_MBType clase
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de buzón de correo (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- Dns del método CreateInstanceFromPropertyData
- Método DNS CreateInstanceFromPropertyData , MicrosoftDNS_MBType clase
- MicrosoftDNS_MBType clase DNS , método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e412cb67ee269cdf291e0c992dc3724ff1187b1704f600ceb3e7fa595e57708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795565"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a>Método CreateInstanceFromPropertyData de la clase MBType de MicrosoftDNS \_

El **método CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de buzón de correo (MB).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
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

*RecordClass* \[ En\]
</dt> <dd>

Opcional. Clase del RR. El valor predeterminado es 1. Los valores siguientes son válidos.



| Value                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ En\]
</dt> <dd>

Opcional. Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MBHost* \[ En\]
</dt> <dd>

Nombre de host de buzón para rr.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)
</dt> <dt>

[**Método Modify de la clase MBType de MicrosoftDNS \_**](microsoftdns-mbtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





