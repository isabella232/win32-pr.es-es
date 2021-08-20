---
title: Método UpdateFromDS de la MicrosoftDNS_Zone clase
description: El método UpdateFromDS fuerza una actualización de la zona desde el servicio de directorio (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Dns del método UpdateFromDS
- Método DNS UpdateFromDS , MicrosoftDNS_Zone clase
- MicrosoftDNS_Zone clase DNS , método UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca537c6440ae14d0e15dea28f62bdb919f3ed7e3348f3a64a2339e0668b5c8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957194"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Método UpdateFromDS de la clase Zone de MicrosoftDNS \_

El **método UpdateFromDS** fuerza una actualización de la zona desde el servicio de directorio (DS).

## <a name="syntax"></a>Sintaxis


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para ejecutar correctamente este método, zoneType debe ser cero y la zona debe almacenarse en el DS.

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

[**Método AgeAllRecords de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método CreateZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResetSecondaries de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método WriteBackZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





