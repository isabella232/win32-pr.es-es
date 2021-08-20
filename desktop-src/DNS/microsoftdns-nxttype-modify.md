---
title: Método Modify de la MicrosoftDNS_NXTType clase
description: El método Modify actualiza un registro de recursos Next (NXT).
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_NXTType class
- MicrosoftDNS_NXTType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163206"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Método Modify de la clase NXTType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos Next (NXT).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*NextDomainName* \[ En\]
</dt> <dd>

Siguiente nombre de dominio.

</dd> <dt>

*Tipos* \[ En\]
</dt> <dd>

Lista separada por espacios de los elementos mnemotécnicos de tipo RR para el nombre de propietario del registro de recursos NXT.

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

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase NXTType de MicrosoftDNS \_**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





