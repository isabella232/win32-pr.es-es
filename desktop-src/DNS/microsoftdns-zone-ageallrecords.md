---
title: Método AgeAllRecords de la clase MicrosoftDNS_Zone
description: El método AgeAllRecords habilita la detección de registros de algunos o todos los registros que no son NS y no SOA de una zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords el método DNS
- Método AgeAllRecords DNS, clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de clase DNS, método AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492370"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>Método AgeAllRecords de la \_ clase de zona MicrosoftDNS

El método **AgeAllRecords** habilita la detección de registros de algunos o todos los registros que no son NS y no SOA de una zona.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nodename* \[ en, opcional\]
</dt> <dd>

Nombre del nodo que se va a edad.

</dd> <dt>

*ApplyToSubtree* \[ en, opcional\]
</dt> <dd>

Especifica si la detección debe aplicarse a todos los registros del subárbol. Establézcalo en TRUE para aplicar la detección de registros obsoletos a todos los registros del subárbol, empezando por NodeName.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

ERROR \_ correcto indica que la detección se ha completado correctamente. Cualquier otro valor es un código de error.

## <a name="remarks"></a>Observaciones

Si no se especifica *nodename* , todos los registros estarán sujetos a detección y eliminación de registros obsoletos.

Si se especifica *nodename* y *ApplyToSubtree* no se especifica o se establece en cero, los registros del nodo especificado estarán sujetos a la detección y eliminación de registros obsoletos.

Si se especifica *nodename* y *ApplyToSubtree* se establece en 1, todos los registros del subárbol que se inicia en *nodename* estarán sujetos a la detección y eliminación de registros obsoletos. La marca de tiempo se establece en la hora actual para todos los RRs no NS y no SOA con los nombres de propietario identificados por los parámetros de entrada.

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

[**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





