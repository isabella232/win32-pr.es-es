---
title: Método Modify de la MicrosoftDNS_WINSRType clase
description: El método Modify actualiza un registro de recursos wins reverse look up (WINSR).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificación del dns del método
- Modificar método DNS , MicrosoftDNS_WINSRType clase
- MicrosoftDNS_WINSRType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076669"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Método Modify de la clase WINSRType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos WINS Reverse Look up (WINSR).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MappingFlag* \[ en, opcional\]
</dt> <dd>

Marca de asignación WINSR que especifica si el registro debe incluirse en la replicación de zona. Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y sin replicación (registro local), respectivamente.

</dd> <dt>

*LookupTimeout* \[ en, opcional\]
</dt> <dd>

Tiempo de espera, en segundos, para un servidor DNS que usa WINS Reverse Look up.

</dd> <dt>

*CacheTimeout* \[ en, opcional\]
</dt> <dd>

El tiempo, en segundos, un servidor DNS que usa WINS Look up puede almacenar en caché la respuesta del servidor WINS.

</dd> <dt>

*ResultDomain* \[ en, opcional\]
</dt> <dd>

Nombre de dominio que se anexará a los nombres NetBIOS devueltos.

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase \_ WINSRType de MicrosoftDNS**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





