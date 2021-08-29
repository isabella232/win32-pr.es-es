---
title: Método Modify de la MicrosoftDNS_WINSType clase
description: El método Modify actualiza un registro Windows de recursos del Servicio de nombres de Internet (WINS).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificación del dns del método
- Modificar el método DNS , MicrosoftDNS_WINSType clase
- MicrosoftDNS_WINSType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf14bd6801900ea9b697ac7db0efea5970c7d5b06317aef4acdd073fc78b1b13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984635"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Método Modify de la clase WINSType de MicrosoftDNS \_

El **método Modify** actualiza un Windows de recursos del Servicio de nombres de Internet (WINS).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MappingFlag* \[ en, opcional\]
</dt> <dd>

Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona. Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y sin replicación (registro local), respectivamente. Los valores siguientes son válidos.



| Value                                                                                                                                               | Significado                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Marca de replicación<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Marca sin replicación (registro local)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un servidor DNS intenta resolver mediante WINS Look up.

</dd> <dt>

*CacheTimeout* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un servidor DNS que usa WINS Look up puede almacenar en caché la respuesta del servidor WINS.

</dd> <dt>

*WinsServers* \[ en, opcional\]
</dt> <dd>

Lista de direcciones IP separadas por comas de servidores WINS que se usan en búsquedas WINS.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cualquier parámetro no especificado se deja sin modificar en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase WINSType de MicrosoftDNS \_**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





