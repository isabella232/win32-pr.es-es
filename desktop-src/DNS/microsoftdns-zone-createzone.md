---
title: Método CreateZone de la MicrosoftDNS_Zone clase
description: El método CreateZone crea una zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Dns del método CreateZone
- Método DNS createZone , MicrosoftDNS_Zone clase
- MicrosoftDNS_Zone clase DNS , método CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22b03e544e89389a9836aa0d7b3dcb964791c7a50124946409481329fbbb122e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131695"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Método CreateZone de la clase MicrosoftDNS \_ Zone

El **método CreateZone** crea una zona DNS.

## <a name="syntax"></a>Sintaxis


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ZoneName* \[ En\]
</dt> <dd>

Cadena que representa el nombre de la zona.

</dd> <dt>

*ZoneType* \[ En\]
</dt> <dd>

Tipo de zona. Los valores válidos son los siguientes:



| Value                                                                        | Significado                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | AD integrado.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Zona secundaria.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Zona de rutas internas.<br/> **Windows Server 2003:** Este tipo de zona se introdujo en Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Reenviador de zona.<br/> **Windows Server 2003:** Este tipo de zona se introdujo en Windows Server 2003.<br/> |



 

</dd> <dt>

*DsIntegrated* \[ En\]
</dt> <dd>

Indica si los datos de zona se almacenan en el Active Directory o en archivos. Si es TRUE, los datos se almacenan en el Active Directory; si es FALSE, los datos se almacenan en archivos.

</dd> <dt>

*DataFileName* \[ en, opcional\]
</dt> <dd>

Nombre del archivo de datos asociado a la zona.

</dd> <dt>

*IpAddr* \[ en, opcional\]
</dt> <dd>

Dirección IP del servidor DNS maestro para la zona.

</dd> <dt>

*AdminEmailName* \[ en, opcional\]
</dt> <dd>

Dirección de correo electrónico del administrador responsable de la zona.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR de tipo **MicrosoftDns \_ Zone**.

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

[**Método ForceRefresh de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResetSecondaries de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





