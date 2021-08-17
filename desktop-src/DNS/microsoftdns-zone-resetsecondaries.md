---
title: Método ResetSecondaries de la MicrosoftDNS_Zone clase
description: El método ResetSecondaries restablece las direcciones IP de los servidores DNS secundarios de la zona.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Dns del método ResetSecondaries
- Método DNS ResetSecondaries , MicrosoftDNS_Zone clase
- MicrosoftDNS_Zone clase DNS , método ResetSecondaries
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
ms.openlocfilehash: 5ab3737bc8143f712560e5ea253237c97da4e2401b98886428642210805ca586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957294"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Método ResetSecondaries de la clase Zone de MicrosoftDNS \_

El **método ResetSecondaries** restablece las direcciones IP de los servidores DNS secundarios de la zona.

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

*SecondaryServers* \[ En\]
</dt> <dd>

Matriz de direcciones IP para servidores DNS secundarios.

</dd> <dt>

*SecureSecondaries* \[ En\]
</dt> <dd>

Especifica la seguridad que se va a aplicar y debe ser una de las siguientes:

-   ZONA \_ SECSECURE \_ NO \_ SECURITY
-   ZONE \_ SECSECURE \_ NS \_ ONLY
-   ZONE \_ SECSECURE \_ LIST \_ ONLY
-   ZONE \_ SECSECURE \_ NO \_ XFR

</dd> <dt>

*NotifyServers* \[ En\]
</dt> <dd>

Dirección IP de los servidores DNS a los que se notificará cuando cambie la zona.

</dd> <dt>

*Notificar* \[ En\]
</dt> <dd>

La configuración de notificación y debe ser una de las siguientes:

-   ZONE \_ NOTIFY \_ OFF
-   NOTIFICACIÓN \_ DE ZONA A TODAS LAS \_ \_ SECUNDARIAS
-   SOLO LISTA \_ DE NOTIFICACIONES \_ DE \_ ZONA

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR de tipo [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Zona MicrosoftDNS \_**](microsoftdns-zone.md)
</dt> <dt>

[**Método AgeAllRecords de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método CreateZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResumeZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





