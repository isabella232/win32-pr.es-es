---
title: Método Modify de la MicrosoftDNS_SOAType clase
description: El método Modify actualiza un registro de recursos de Inicio de autoridad (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificación del DNS del método
- Modify method DNS , MicrosoftDNS_SOAType class
- MicrosoftDNS_SOAType clase DNS , Método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825085"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Método Modify de la clase SOAType de MicrosoftDNS \_

El **método Modify** actualiza un registro de recursos de Inicio de autoridad (SOA).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*SerialNumber* \[ in, opcional\]
</dt> <dd>

Número de serie SOA que representa el número [](s-gly.md) de veces que se ha actualizado la zona, que usan los servidores secundarios para determinar si es necesaria la transferencia de zona.

</dd> <dt>

*PrimaryServer* \[ in, opcional\]
</dt> <dd>

Nombre del servidor principal.

</dd> <dt>

*ResponsibleParty* \[ in, opcional\]
</dt> <dd>

Dirección de buzón de la parte responsable, en forma de alias.domain, como xyz.microsoft.com. Tenga en cuenta el uso de un punto en lugar de un símbolo at (@).

</dd> <dt>

*RefreshInterval* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, antes de que se actualice la zona que contiene este registro.

</dd> <dt>

*RetryDelay* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, el servidor DNS debe retrasarse entre los intentos de resolución de nombres.

</dd> <dt>

*ExpireLimit* \[ in, opcional\]
</dt> <dd>

Tiempo, en segundos, que los servidores secundarios deben esperar una respuesta del servidor principal antes de descartar sus copias del archivo de zona como no válidas.

</dd> <dt>

*MinimumTTL* \[ in, opcional\]
</dt> <dd>

Tiempo de TTL, en segundos, aplicado a los registros de recursos de la zona que no especifican su propio TTL.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al objeto modificado

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





