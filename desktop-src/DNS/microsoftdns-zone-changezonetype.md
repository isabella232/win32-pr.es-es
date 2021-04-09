---
title: Método ChangeZoneType de la clase MicrosoftDNS_Zone
description: El método ChangeZoneType cambia el tipo de una zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- ChangeZoneType el método DNS
- Método ChangeZoneType DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método ChangeZoneType
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
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079250"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Método ChangeZoneType de la \_ clase de zona MicrosoftDNS

El método **ChangeZoneType** cambia el tipo de una zona.

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

*ZoneType* \[ de\]
</dt> <dd>

Tipo de zona. Los valores válidos son los siguientes:



| Value                                                                        | Significado                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Zona principal.<br/>   |
| <dl> <dt>1</dt> </dl> | Zona secundaria.<br/> |
| <dl> <dt>2</dt> </dl> | Zona de rutas internas.<br/>      |
| <dl> <dt>3</dt> </dl> | Reenviador de zona.<br/> |



 

</dd> <dt>

*Nombre de archivo* \[ en, opcional\]
</dt> <dd>

Nombre del archivo de datos asociado a la zona.

</dd> <dt>

*DirIP* \[ en, opcional\]
</dt> <dd>

Dirección IP del servidor DNS de maestro para la zona.

</dd> <dt>

*AdminEmailName* \[ en, opcional\]
</dt> <dd>

Dirección de correo electrónico del administrador responsable de la zona.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR de tipo **la \_ zona MicrosoftDns**.

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

[**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





