---
title: Método Modify de la MicrosoftDNS_RPType clase
description: El método Modify actualiza un registro de recursos de persona responsable (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_RPType class
- MicrosoftDNS_RPType clase DNS , Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587495"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Método Modify de la clase RPType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de persona responsable (RP).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*RPMailbox* \[ in, opcional\]
</dt> <dd>

FQDN que especifica el buzón para la persona responsable.

</dd> <dt>

*TXTDomainName* \[ in, opcional\]
</dt> <dd>

FQDN para el que existen registros de recursos TXT.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin cambios en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpType de MicrosoftDNS \_**](microsoftdns-rptype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase RPType de MicrosoftDNS \_**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





