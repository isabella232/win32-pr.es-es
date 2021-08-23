---
title: Método GetObjectByTextRepresentation de la MicrosoftDNS_ResourceRecord clase
description: El método GetObjectByTextRepresentation recupera una instancia existente de la clase ResourceRecord de \_ MicrosoftDNS.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Método DNS GetObjectByTextRepresentation
- Método DNS GetObjectByTextRepresentation , MicrosoftDNS_ResourceRecord clase
- MicrosoftDNS_ResourceRecord clase DNS , método GetObjectByTextRepresentation
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
ms.openlocfilehash: 08e3b824ccabe86e842d4ef6f61799b33110b5d28a58658a6d4cbedc824c134b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692425"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método GetObjectByTextRepresentation de la clase \_ ResourceRecord de MicrosoftDNS

El **método GetObjectByTextRepresentation** recupera una instancia existente de la [**clase \_ ResourceRecord de MicrosoftDNS.**](microsoftdns-resourcerecord.md)

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

*DnsServerName* \[ En\]
</dt> <dd>

Nombre del servidor DNS del que se debe recuperar el RR.

</dd> <dt>

*ContainerName* \[ En\]
</dt> <dd>

Nombre del contenedor del que se debe obtener el RR.

</dd> <dt>

*TextRepresentation* \[ En\]
</dt> <dd>

Representación de texto del RR que se va a recuperar.

</dd> <dt>

*RR* \[ out\]
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
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromTextRepresentation de la clase ResourceRecord de \_ MicrosoftDNS**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





