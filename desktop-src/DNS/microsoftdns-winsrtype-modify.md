---
title: Método Modify de la clase MicrosoftDNS_WINSRType
description: El método Modify actualiza un registro de recursos de búsqueda inversa de WINS (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_WINSRType clase
- MicrosoftDNS_WINSRType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151037"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Método Modify de la \_ clase MicrosoftDNS WINSRType

El método **Modify** actualiza un registro de recursos de búsqueda inversa de WINS (WINSR).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MappingFlag* \[ en, opcional\]
</dt> <dd>

Marca de asignación de WINSr que especifica si el registro debe incluirse en la replicación de zona. Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y no replicación (registro local), respectivamente.

</dd> <dt>

*Tiempodeesperadebúsqueda* \[ en, opcional\]
</dt> <dd>

Tiempo de espera, en segundos, para un servidor DNS que usa la búsqueda inversa de WINS.

</dd> <dt>

*CacheTimeout* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un servidor DNS que usa la búsqueda WINS puede almacenar en caché la respuesta del servidor WINS.

</dd> <dt>

*ResultDomain* \[ en, opcional\]
</dt> <dd>

Nombre de dominio que se va a anexar a los nombres NetBIOS devueltos.

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS WINSRType**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





