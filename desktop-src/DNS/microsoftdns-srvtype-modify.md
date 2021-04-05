---
title: Método Modify de la clase MicrosoftDNS_SRVType
description: El método Modify actualiza un registro de recursos de servicio (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SRVType clase
- MicrosoftDNS_SRVType de clase DNS, Modify (método)
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
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079703"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Método Modify de la \_ clase MicrosoftDNS SRVType

El método **Modify** actualiza un registro de recursos de servicio (SRV).

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

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Prioridad* \[ de en, opcional\]
</dt> <dd>

Prioridad del host de destino especificado en el nombre del propietario. Los números más bajos implican prioridades más altas.

</dd> <dt>

*Peso* \[ de en, opcional\]
</dt> <dd>

Peso del host de destino. Esto resulta útil al seleccionar entre los hosts que tienen la misma prioridad. Las posibilidades de usar este host deben ser proporcionales a su peso.

</dd> <dt>

*Puerto* \[ de en, opcional\]
</dt> <dd>

Puerto usado en el host de destino de un servicio de protocolo.

</dd> <dt>

*SRVDomainName* \[ en, opcional\]
</dt> <dd>

FQDN del host de destino. Un destino de \\ . \\ significa que el servicio no está disponible en este dominio.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al nuevo objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los parámetros no especificados se dejan sin cambios en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





