---
title: Método Modify de la MicrosoftDNS_SIGType clase
description: El método Modify actualiza un RR de firma (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_SIGType class
- MicrosoftDNS_SIGType clase DNS , Método Modify
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
ms.openlocfilehash: be64eb494eb72ace437aeade8d7d01a6675f99b2b44c4fa461a8e60c8ed3de1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692285"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Método Modify de la clase SIGType de MicrosoftDNS \_

El **método Modify** actualiza un RR de firma (SIG).

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

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin cambios en el registro modificado.

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

[**Método CreateInstanceFromPropertyData de la clase SIGType de MicrosoftDNS \_**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





