---
title: Método CreateInstanceFromTextRepresentation de la clase MicrosoftDNS_ResourceRecord
description: El método CreateInstanceFromTextRepresentation crea una instancia de un \_ objeto MicrosoftDNS ResourceRecord.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- CreateInstanceFromTextRepresentation el método DNS
- Método CreateInstanceFromTextRepresentation DNS, clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de clase DNS, método CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079481"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord

El método **CreateInstanceFromTextRepresentation** crea una instancia de un objeto [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DnsServerName* \[ de\]
</dt> <dd>

Nombre del servidor DNS en el que se debe crear el RR.

</dd> <dt>

*ContainerName* \[ de\]
</dt> <dd>

Nombre del contenedor en el que se debe colocar el nuevo RR.

</dd> <dt>

*TextRepresentation* \[ de\]
</dt> <dd>

Representación de texto de la instancia de RR que se va a crear.

</dd> <dt>

*RR* \[ out, Ref\]
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

[**Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





