---
title: Método CreateInstanceFromTextRepresentation de la MicrosoftDNS_ResourceRecord clase
description: El método CreateInstanceFromTextRepresentation crea una instancia de un objeto \_ ResourceRecord de MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- Método DNS CreateInstanceFromTextRepresentation
- Método DNS CreateInstanceFromTextRepresentation , MicrosoftDNS_ResourceRecord clase
- MicrosoftDNS_ResourceRecord clase DNS , método CreateInstanceFromTextRepresentation
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
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104025"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Método CreateInstanceFromTextRepresentation de la clase ResourceRecord de MicrosoftDNS \_

El **método CreateInstanceFromTextRepresentation** crea una instancia de un objeto [**\_ ResourceRecord de MicrosoftDNS.**](microsoftdns-resourcerecord.md)

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

*DnsServerName* \[ En\]
</dt> <dd>

Nombre del servidor DNS en el que se debe crear el RR.

</dd> <dt>

*ContainerName* \[ En\]
</dt> <dd>

Nombre del contenedor en el que se debe colocar el nuevo RR.

</dd> <dt>

*TextRepresentation* \[ En\]
</dt> <dd>

Representación de texto de la instancia rr que se va a crear.

</dd> <dt>

*RR* \[ out, ref\]
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

[**Método GetObjectByTextRepresentation de la clase \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





