---
title: Método Modify de la MicrosoftDNS_AFSDBType clase
description: El método Modify actualiza un registro de recursos del servidor de bases de datos del sistema de archivos De Andrew (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_AFSDBType class
- MicrosoftDNS_AFSDBType dns de clase , método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385b80d853c3b610971803c0b1d80a81b7b7c2335186fe4585e63f60c3e3cca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104065"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Método Modify de la clase AFSDBType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos del servidor de bases de datos del sistema de archivos De Andrew (AFSDB).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Subtipo* \[ in, opcional\]
</dt> <dd>

Subtipo del servidor afs del host. Para el subtipo 1 (valor = 1), el host tiene un servidor de ubicación de volumen afs versión 3.0 para la celda afs con nombre. En el caso del subtipo 2 (valor =2), el host tiene un servidor de nombres autenticado que contiene el nodo de directorio raíz de celda para la celda DCE/NCA con nombre.

</dd> <dt>

*ServerName* \[ in, opcional\]
</dt> <dd>

FQDN que especifica un host que tiene un servidor para la celda afs especificada en el nombre del propietario.

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase \_ AFSDBType de MicrosoftDNS**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





