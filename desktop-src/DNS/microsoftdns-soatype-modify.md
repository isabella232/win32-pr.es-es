---
title: Método Modify de la clase MicrosoftDNS_SOAType
description: El método Modify actualiza un registro de recursos de inicio de autoridad (SOA).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_SOAType clase
- MicrosoftDNS_SOAType de clase DNS, Modify (método)
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
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078991"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Método Modify de la \_ clase MicrosoftDNS SOAType

El método **Modify** actualiza un registro de recursos de inicio de autoridad (SOA).

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

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*SerialNumber* \[ en, opcional\]
</dt> <dd>

Número de serie SOA que representa el número de veces que se ha actualizado la zona, utilizada por [*los servidores secundarios*](s-gly.md) para determinar si es necesaria la transferencia de zona.

</dd> <dt>

*PrimaryServer* \[ en, opcional\]
</dt> <dd>

Nombre del servidor principal.

</dd> <dt>

*ResponsibleParty* \[ en, opcional\]
</dt> <dd>

Dirección de buzón del usuario responsable, en forma de alias. Domain, como xyz.microsoft.com. Observe el uso de un punto en lugar de un símbolo de arroba (@).

</dd> <dt>

*RefreshInterval* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, antes de que se actualice la zona que contiene este registro.

</dd> <dt>

*RetryDelay* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que el servidor DNS debe retrasarse entre los intentos de resolución de nombres.

</dd> <dt>

*ExpireLimit* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que los servidores secundarios deben esperar una respuesta del servidor principal antes de descartar las copias del archivo de zona como no válidas.

</dd> <dt>

*MinimumTTL* \[ en, opcional\]
</dt> <dd>

Tiempo de TTL, en segundos, aplicado a los registros de recursos de la zona que no especifican su propio TTL.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al objeto modificado

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





