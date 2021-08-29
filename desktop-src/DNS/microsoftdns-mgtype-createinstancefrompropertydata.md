---
title: Método CreateInstanceFromPropertyData de la MicrosoftDNS_MGType clase
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de grupo de correo (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- Dns del método CreateInstanceFromPropertyData
- Método DNS CreateInstanceFromPropertyData , MicrosoftDNS_MGType clase
- MicrosoftDNS_MGType clase DNS , método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0a9eee3f26e563b70bca1a0801443b6ce3db5b6522b2ce04e33efa83a5f6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795544"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a>Método CreateInstanceFromPropertyData de la clase MGType de MicrosoftDNS \_

El **método CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de grupo de correo (MG).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
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

Nombre del contenedor para la instancia de Zone, Cache o RootHints que contiene este RR.

</dd> <dt>

*OwnerName* \[ En\]
</dt> <dd>

Nombre del propietario del RR.

</dd> <dt>

*RecordClass* \[ in, opcional\]
</dt> <dd>

Clase del RR. El valor predeterminado es 1. Los valores siguientes son válidos.



| Value                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MGMailbox* \[ En\]
</dt> <dd>

FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre de propietario del registro.

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

[**MgType de MicrosoftDNS \_**](microsoftdns-mgtype.md)
</dt> <dt>

[**Método Modify de la clase MGType de MicrosoftDNS \_**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





