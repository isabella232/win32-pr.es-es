---
title: Método Modify de la clase MicrosoftDNS_AType
description: El método Modify actualiza el TTL y la dirección IP de un registro de recursos de dirección de host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_AType clase
- MicrosoftDNS_AType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079383"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Método Modify de la \_ clase MicrosoftDNS AType

El método **Modify** actualiza el TTL y la dirección IP de un registro de recursos de dirección de host (a).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Dirección IP* \[ en, opcional\]
</dt> <dd>

Cadena que representa la dirección IP del host.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





