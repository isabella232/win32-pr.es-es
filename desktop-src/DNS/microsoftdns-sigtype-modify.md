---
title: Método Modify de la clase MicrosoftDNS_SIGType
description: El método Modify actualiza un RR de firma (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SIGType clase
- MicrosoftDNS_SIGType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489436"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Método Modify de la \_ clase MicrosoftDNS SIGType

El método **Modify** actualiza un RR de firma (SIG).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
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

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*TypeCovered* \[ de\]
</dt> <dd>

Tipo de RR que se trata en este SIG.

</dd> <dt>

*Algoritmo* \[ de de\]
</dt> <dd>

Algoritmo usado con la clave especificada en el registro de recursos. Los valores asignados se muestran en la tabla siguiente.



| Value                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografía de curva elíptica<br/> |



 

</dd> <dt>

*Etiquetas* \[ de de\]
</dt> <dd>

Recuento sin signo de etiquetas en el nombre de propietario del RR de firma original. El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.

</dd> <dt>

*OriginalTTL* \[ de\]
</dt> <dd>

TTL del conjunto de RR firmado por el SIG.

</dd> <dt>

*SignatureExpiration* \[ de\]
</dt> <dd>

Fecha de expiración de la firma, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.

</dd> <dt>

*SignatureInception* \[ de\]
</dt> <dd>

Fecha y hora en las que la firma es válida, expresada en segundos desde el comienzo del 1 de enero de 1970, hora del meridiano de Greenwich (GMT), excluyendo los segundos bisiestos.

</dd> <dt>

*KeyTag* \[ de\]
</dt> <dd>

Método usado para elegir una clave que comprueba un SIG. Vea RFC 2535, Apéndice C para el método usado para calcular un KeyTag.

</dd> <dt>

*SignerName* \[ de\]
</dt> <dd>

Nombre de dominio del firmante que generó el RR SIG.

</dd> <dt>

*Firma* \[ de de\]
</dt> <dd>

Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al nuevo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los parámetros no especificados se dejan sin cambios en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SIGType**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





