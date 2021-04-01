---
title: Método ResetSecondaries de la clase MicrosoftDNS_Zone
description: El método ResetSecondaries restablece las direcciones IP de los servidores DNS secundarios de la zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- ResetSecondaries el método DNS
- Método ResetSecondaries DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996711"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Método ResetSecondaries de la \_ clase de zona MicrosoftDNS

El método **ResetSecondaries** restablece las direcciones IP de los servidores DNS secundarios de la zona.

## <a name="syntax"></a>Sintaxis


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecondaryServers* \[ de\]
</dt> <dd>

Matriz de direcciones IP para los servidores DNS secundarios.

</dd> <dt>

*SecureSecondaries* \[ de\]
</dt> <dd>

Especifica la seguridad que se va a aplicar y debe ser una de las siguientes:

-   ZONA \_ SECSECURE \_ sin \_ seguridad
-   \_solo zona SECSECURE \_ NS \_
-   \_ \_ solo lista de SECSECURE de zona \_
-   ZONA \_ SECSECURE \_ no \_ XFR

</dd> <dt>

*NotifyServers* \[ de\]
</dt> <dd>

Dirección IP de los servidores DNS a los que se notificará cuando cambie la zona.

</dd> <dt>

*Notificar* \[ a de\]
</dt> <dd>

Configuración de notificación y debe ser uno de los siguientes:

-   notificación de zona \_ \_ desactivada
-   ZONA de \_ notificación de \_ todos los \_ secundarios
-   \_solo lista de notificaciones de zona \_ \_

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR de tipo [**la \_ zona MicrosoftDNS**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Zona MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Método AgeAllRecords de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método CreateZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResumeZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





