---
title: Método Modify de la MicrosoftDNS_RTType clase
description: El método Modify actualiza un registro de recursos de Route Through (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_RTType clase
- MicrosoftDNS_RTType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2003f8e2840a2684f91a7a01b0341e2e8dcdf0ca88b6bf31fcf58b3a3c6f79bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692405"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Método Modify de la clase RTType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de Route Through (RT).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Preferencia* \[ en, opcional\]
</dt> <dd>

Preferencia dada a este RR entre otros en el mismo propietario. Se prefieren valores más bajos.

</dd> <dt>

*IntermediateHost* \[ en, opcional\]
</dt> <dd>

FQDN que especifica un host que sirve como intermedio para llegar al host especificado por el propietario.

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MICROSOFTDNS \_ RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





