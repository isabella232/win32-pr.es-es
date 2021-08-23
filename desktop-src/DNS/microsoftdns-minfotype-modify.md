---
title: Método Modify de la MicrosoftDNS_MINFOType clase
description: El método Modify actualiza un registro de recursos de información de correo (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_MINFOType clase
- MicrosoftDNS_MINFOType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692565"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Método Modify de la clase MINFOType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de información de correo (MINFO).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*ResponsibleMailbox* \[ en, opcional\]
</dt> <dd>

FQDN que especifica un buzón de correo responsable de la lista de distribución de correo o buzón especificado en el nombre de propietario del registro.

</dd> <dt>

*ErrorMailbox* \[ en, opcional\]
</dt> <dd>

FQDN que especifica un buzón para recibir mensajes de error relacionados con la lista de distribución de correo o con el buzón especificado por el nombre de propietario del registro MINFO.

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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MINFOType de MicrosoftDNS \_**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





