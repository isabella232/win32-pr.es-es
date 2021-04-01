---
title: Método Modify de la clase MicrosoftDNS_WKSType
description: El método Modify actualiza un registro de recursos de Well-Known Services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_WKSType clase
- MicrosoftDNS_WKSType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905388"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Método Modify de la \_ clase MicrosoftDNS WKSType

El método **Modify** actualiza un registro de recursos de Well-Known Services (WKS).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*InternetAddress* \[ en, opcional\]
</dt> <dd>

Dirección IP de Internet del propietario del registro.

</dd> <dt>

*IPProtocol* \[ en, opcional\]
</dt> <dd>

Cadena que representa el protocolo IP para este registro. Los valores válidos son UDP o TCP.

</dd> <dt>

*Servicios* \[ de en, opcional\]
</dt> <dd>

Cadena que contiene todos los servicios utilizados por el registro de servicio conocido (WKS).

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WKSType**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





