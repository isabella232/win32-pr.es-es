---
title: Método Modify de la MicrosoftDNS_MRType clase
description: El método Modify actualiza un registro de recursos de cambio de nombre de buzón (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_MRType clase
- MicrosoftDNS_MRType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bc22f87a8f06bbd9497ec6dc6648e411fa8abfe3a6b8f5a1eccad81cbaf3da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131705"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a>Método Modify de la clase MRType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de cambio de nombre de buzón (MR).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MRMailbox* \[ En\]
</dt> <dd>

FQDN que especifica un buzón que es el nombre adecuado del buzón especificado en el nombre de propietario del registro.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin modificar en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MRType de MicrosoftDNS \_**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





