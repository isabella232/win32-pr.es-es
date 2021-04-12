---
title: Método CreateZone de la clase MicrosoftDNS_Zone
description: El método CreateZone crea una zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- CreateZone el método DNS
- Método CreateZone DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método CreateZone
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
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079548"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Método CreateZone de la \_ clase de zona MicrosoftDNS

El método **CreateZone** crea una zona DNS.

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

*Nombre_zona* \[ de\]
</dt> <dd>

Cadena que representa el nombre de la zona.

</dd> <dt>

*ZoneType* \[ de\]
</dt> <dd>

Tipo de zona. Los valores válidos son los siguientes:



| Value                                                                        | Significado                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | AD integrado.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Zona secundaria.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Zona de rutas internas.<br/> **Windows Server 2003:** Este tipo de zona se introduce en Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Reenviador de zona.<br/> **Windows Server 2003:** Este tipo de zona se introduce en Windows Server 2003.<br/> |



 

</dd> <dt>

*DsIntegrated* \[ de\]
</dt> <dd>

Indica si los datos de zona se almacenan en el Active Directory o en archivos. Si es TRUE, los datos se almacenan en el Active Directory; Si es FALSE, los datos se almacenan en archivos.

</dd> <dt>

*Nombre de archivo* \[ en, opcional\]
</dt> <dd>

Nombre del archivo de datos asociado a la zona.

</dd> <dt>

*DirIP* \[ en, opcional\]
</dt> <dd>

Dirección IP del servidor DNS maestro de la zona.

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

[**Método ChangeZoneType de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
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

 

 





