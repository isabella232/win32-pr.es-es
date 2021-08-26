---
title: Método Modify de la MicrosoftDNS_MBType clase
description: El método Modify actualiza un registro de recursos de buzón (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_MBType class
- MicrosoftDNS_MBType clase DNS , Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b0e4183a2b736d0ed896fee4bf2cc57e35f0e6b628a9aee4345f4c33b33ed6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918345"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a>Método Modify de la clase MBType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de buzón (MB).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MBHost* \[ En\]
</dt> <dd>

Cadena que representa el nombre de host del buzón para el registro MB.

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

[**MbType de MicrosoftDNS \_**](microsoftdns-mbtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MBType de MicrosoftDNS \_**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





