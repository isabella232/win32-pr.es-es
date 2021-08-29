---
title: Método Modify de la MicrosoftDNS_ISDNType clase
description: El método Modify actualiza un registro de recursos isdn.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- Modificación del dns del método
- Modificar método DNS , MicrosoftDNS_ISDNType clase
- MicrosoftDNS_ISDNType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932eb1947287ad6c24592f025301bcf42d5ffb4fc1924d1c18f771bc000396c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795575"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a>Método Modify de la clase MicrosoftDNS \_ ISDNType

El **método Modify** actualiza un registro de recursos isdn.

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*ISDNNumber* \[ en, opcional\]
</dt> <dd>

Número ISDN y DDI del propietario del registro.

</dd> <dt>

*SubAddress* \[ en, opcional\]
</dt> <dd>

Subdirección del propietario, si se define.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

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

[**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase \_ ISDNType de MicrosoftDNS**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





