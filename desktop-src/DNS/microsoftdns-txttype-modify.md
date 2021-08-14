---
title: Método Modify de la MicrosoftDNS_TXTType clase
description: El método Modify actualiza un registro de recursos text (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modificación del DNS del método
- Modificar el método DNS , MicrosoftDNS_TXTType clase
- MicrosoftDNS_TXTType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e565d4c48b048b4d72b11c939b644752cb14f1993c2810f127bb14f60bec929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957304"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Método Modify de la clase TXTType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos text (TXT).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Texto descriptivo* \[ En\]
</dt> <dd>

Texto descriptivo, cuya semántica depende del dominio propietario.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin modificar en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase TXTType de MicrosoftDNS \_**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





