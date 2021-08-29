---
title: Método Modify de la MicrosoftDNS_SRVType clase
description: El método Modify actualiza un registro de recursos de servicio (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_SRVType class
- MicrosoftDNS_SRVType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9e1a4b3b3da3fc7f7cb732c094f4ddfce2e2c0ca3e8836f25bb3034b590bf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076719"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Método Modify de la clase SRVType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de servicio (SRV).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Prioridad* \[ in, opcional\]
</dt> <dd>

Prioridad del host de destino especificado en el nombre del propietario. Los números más bajos implican prioridades más altas.

</dd> <dt>

*Peso* \[ in, opcional\]
</dt> <dd>

Peso del host de destino. Esto resulta útil al seleccionar entre hosts que tienen la misma prioridad. Las posibilidades de usar este host deben ser proporcionales a su peso.

</dd> <dt>

*Puerto* \[ in, opcional\]
</dt> <dd>

Puerto usado en el host de destino de un servicio de protocolo.

</dd> <dt>

*SRVDomainName* \[ in, opcional\]
</dt> <dd>

FQDN del host de destino. Un destino de . significa que el servicio no está disponible \\ \\ en este dominio.

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

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase SRVType de MicrosoftDNS \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





