---
title: Método CreateInstanceFromPropertyData de la MicrosoftDNS_SIGType clase
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de firma (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- Dns del método CreateInstanceFromPropertyData
- Método DNS CreateInstanceFromPropertyData , MicrosoftDNS_SIGType clase
- MicrosoftDNS_SIGType clase DNS , método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90501af2f6e492e56d17f88fb6bc74cc72522503760688457832a2374918100e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076729"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Método CreateInstanceFromPropertyData de la clase SIGType de MicrosoftDNS \_

El **método CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de firma (SIG).

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
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

*TypeCovered* \[ En\]
</dt> <dd>

Tipo de RR cubierto por esta SIG.

</dd> <dt>

*Algoritmo* \[ En\]
</dt> <dd>

Algoritmo utilizado con la clave especificada en el registro de recursos. Los valores asignados se muestran en la tabla siguiente.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografía de curva elíptica<br/> |



 

</dd> <dt>

*Etiquetas* \[ En\]
</dt> <dd>

Recuento sin signo de etiquetas en el nombre de propietario de RR sig original. El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.

</dd> <dt>

*OriginalTTL* \[ En\]
</dt> <dd>

TTL del conjunto RR firmado por sig.

</dd> <dt>

*SignatureExpiration* \[ En\]
</dt> <dd>

Fecha de expiración de la firma, expresada en segundos desde el 1 de enero de 1970, hora media de Greenwich (GMT), excepto los segundos bisiestos.

</dd> <dt>

*SignatureInception* \[ En\]
</dt> <dd>

Fecha y hora en que la firma pasa a ser válida, expresada en segundos desde el principio del 1 de enero de 1970, hora media de Greenwich (GMT), excepto los segundos bisiestos.

</dd> <dt>

*KeyTag* \[ En\]
</dt> <dd>

Método utilizado para elegir una clave que comprueba una SIG. Consulte RFC 2535, Apéndice C para el método usado para calcular un KeyTag.

</dd> <dt>

*SignerName* \[ En\]
</dt> <dd>

Nombre de dominio del firmante que generó el RR de SIG.

</dd> <dt>

*Firma* \[ En\]
</dt> <dd>

Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.

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

[**SigType de MicrosoftDNS \_**](microsoftdns-sigtype.md)
</dt> <dt>

[**Método Modify de la clase SIGType de MicrosoftDNS \_**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





