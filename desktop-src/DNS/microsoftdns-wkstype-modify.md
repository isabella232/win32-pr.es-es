---
title: Método Modify de la MicrosoftDNS_WKSType clase
description: El método Modify actualiza un registro de recursos Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_WKSType clase
- MicrosoftDNS_WKSType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f58a71b7d3a3237a744d42c90bc437714ed50553639253bafb0b2b9fb2977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692245"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Método Modify de la clase WKSType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos Well-Known Services (WKS).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*InternetAddress* \[ en, opcional\]
</dt> <dd>

Dirección IP de Internet del propietario del registro.

</dd> <dt>

*IPProtocol* \[ en, opcional\]
</dt> <dd>

Cadena que representa el protocolo IP para este registro. Los valores válidos son UDP o TCP.

</dd> <dt>

*Servicios* \[ en, opcional\]
</dt> <dd>

Cadena que contiene todos los servicios utilizados por el registro Well Known Service (WKS).

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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase WKSType de MicrosoftDNS \_**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





