---
title: Método Modify de la clase MicrosoftDNS_MINFOType
description: El método Modify actualiza un registro de recursos de información de correo (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MINFOType clase
- MicrosoftDNS_MINFOType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489773"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Método Modify de la \_ clase MicrosoftDNS MINFOType

El método **Modify** actualiza un registro de recursos de información de correo (MINFO).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*ResponsibleMailbox* \[ en, opcional\]
</dt> <dd>

FQDN que especifica un buzón responsable de la lista de distribución de correo o el buzón especificado en el nombre del propietario del registro.

</dd> <dt>

*ErrorMailbox* \[ en, opcional\]
</dt> <dd>

FQDN que especifica un buzón para recibir mensajes de error relacionados con la lista de distribución de correo o con el buzón especificado por el nombre del propietario del registro MINFO.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al objeto modificado.

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

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MINFOType**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





