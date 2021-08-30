---
title: Método ChangeZoneType de la MicrosoftDNS_Zone clase
description: El método ChangeZoneType cambia el tipo de una zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- Dns del método ChangeZoneType
- Método DNS changeZoneType , MicrosoftDNS_Zone clase
- MicrosoftDNS_Zone clase DNS , método ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4878d2937d6a8e3b14a72a1055fd4d044ad047629d9e63cced375d4f75ddb60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984555"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Método ChangeZoneType de la clase Zone de MicrosoftDNS \_

El **método ChangeZoneType** cambia el tipo de una zona.

## <a name="syntax"></a>Sintaxis


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ZoneType* \[ En\]
</dt> <dd>

Tipo de zona. Los valores válidos son los siguientes:



| Value                                                                        | Significado                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Zona principal.<br/>   |
| <dl> <dt>1</dt> </dl> | Zona secundaria.<br/> |
| <dl> <dt>2</dt> </dl> | Zona de rutas internas.<br/>      |
| <dl> <dt>3</dt> </dl> | Reenviador de zona.<br/> |



 

</dd> <dt>

*DataFileName* \[ en, opcional\]
</dt> <dd>

Nombre del archivo de datos asociado a la zona.

</dd> <dt>

*IpAddr* \[ en, opcional\]
</dt> <dd>

Dirección IP del servidor DNS de la zona.

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

[**Método ResetSecondaries de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





