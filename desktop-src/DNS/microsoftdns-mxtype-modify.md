---
title: Método Modify de la MicrosoftDNS_MXType clase
description: El método Modify actualiza un registro de recursos de Mail Exchanger (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_MXType class
- MicrosoftDNS_MXType clase DNS , Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fb31da6bf0861c94c54163fa9c771ac592fca105a5459214e17031c3b8e6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076789"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Método Modify de la clase MXType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de Mail Exchanger (MR).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Preferencia* \[ in, opcional\]
</dt> <dd>

Preferencia dada a este RR entre otras personas en el mismo propietario. Se prefieren valores inferiores.

</dd> <dt>

*MailExchange* \[ in, opcional\]
</dt> <dd>

FQDN que especifica un host dispuesto a actuar como intercambio de correo para el nombre del propietario.

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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MxType de MicrosoftDNS \_**](microsoftdns-mxtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MXType de MicrosoftDNS \_**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





