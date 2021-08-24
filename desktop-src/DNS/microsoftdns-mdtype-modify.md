---
title: Método Modify de la MicrosoftDNS_MDType clase
description: El método Modify actualiza un registro de recursos del Agente de correo para dominio (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_MDType class
- MicrosoftDNS_MDType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c402a753394c5ca7c12acf212377823a87d16e5d17f0d97981ab5e75d8a537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527265"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a>Método Modify de la clase MDType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos del Agente de correo para dominio (MD).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MDHost* \[ in, opcional\]
</dt> <dd>

Cadena que representa el host de entrega de correo.

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

[**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MDType de MicrosoftDNS \_**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





