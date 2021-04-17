---
title: Método GetObjectByTextRepresentation de la clase MicrosoftDNS_ResourceRecord
description: El método GetObjectByTextRepresentation recupera una instancia existente de la clase MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- GetObjectByTextRepresentation el método DNS
- Método GetObjectByTextRepresentation DNS, clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de clase DNS, método GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491170"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord

El método **GetObjectByTextRepresentation** recupera una instancia existente de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Sintaxis


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DnsServerName* \[ de\]
</dt> <dd>

Nombre del servidor DNS desde el que se debe recuperar el RR.

</dd> <dt>

*ContainerName* \[ de\]
</dt> <dd>

Nombre del contenedor del que se debe obtener el RR.

</dd> <dt>

*TextRepresentation* \[ de\]
</dt> <dd>

Representación de texto del RR que se va a recuperar.

</dd> <dt>

*RR* \[ enuncia\]
</dt> <dd>

Referencia al RR con instancias.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





