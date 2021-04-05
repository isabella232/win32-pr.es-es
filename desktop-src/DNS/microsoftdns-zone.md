---
title: MicrosoftDNS_Zone (clase)
description: La \_ clase de zona MicrosoftDNS describe una zona DNS. Cada instancia de la \_ clase de zona MicrosoftDNS debe asignarse exactamente a un servidor DNS. Las zonas pueden estar asociadas a varias instancias de \_ las clases de dominio microsoftdns o microsoftdns \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS de la clase MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079870"
---
# <a name="microsoftdns_zone-class"></a>MicrosoftDNS ( \_ clase de zona)

> [!NOTE]
> Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

> [!NOTE]
> Este artículo contiene referencias al término servidor maestro, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

La clase de **\_ zona MicrosoftDNS** describe una zona DNS. Cada instancia de la clase de **\_ zona MicrosoftDNS** debe asignarse exactamente a un servidor DNS. Las zonas pueden estar asociadas a varias instancias de las clases de [**\_ dominio Microsoftdns**](microsoftdns-domain.md) o [**microsoftdns \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a>Miembros

La clase de **\_ zona MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ zona MicrosoftDNS** tiene estos métodos.



| Método                   | Descripción                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Habilita la detección de registros de algunos o de todos los registros que no son de y no SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Cambia los tipos de zona. <br/> Calificadores: implementados<br/>                                                                                                                                         |
| **CreateZone**           | Crea una nueva zona. <br/> Calificadores: ninguno.<br/>                                                                                                                                               |
| **ForceRefresh**         | Fuerza una actualización de la secundaria desde el servidor DNS maestro. <br/> Calificadores: implementados<br/>                                                                                               |
| **GetDistinguishedName** | Obtiene el nombre distintivo de DS para la zona. <br/> Calificadores: implementados<br/>                                                                                                                 |
| **PauseZone**            | Pausa la zona. <br/> Calificadores: implementados<br/>                                                                                                                                            |
| **ReloadZone**           | Vuelve a cargar la zona. <br/> Calificadores: implementados<br/>                                                                                                                                           |
| **ResetSecondaries**     | Restablece la matriz de direcciones IP secundarias. <br/> Calificadores: implementados<br/>                                                                                                                      |
| **ResumeZone**           | Reanuda la zona. <br/> Calificadores: implementados<br/>                                                                                                                                           |
| **UpdateFromDS**         | Fuerza una actualización de la zona desde el servicio de directorio (DS). Para que este método sea válido, ZoneType debe ser 0 la zona debe estar almacenada en el DS. <br/> Calificadores: implementados<br/> |
| **WriteBackZone**        | Guarda los datos de la zona en su archivo de zona. <br/> Calificadores: implementados, estáticos<br/>                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La clase de **\_ zona MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**Edad**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el comportamiento de detección y eliminación de registros obsoletos de la zona. Cero indica que la eliminación de registros obsoletos está deshabilitada. Cuando se deshabilita la eliminación de registros obsoletos, no se actualizan las marcas de tiempo de los registros de la zona y los registros no se someten a la eliminación de registros obsoletos. Cuando se establece en uno, los registros están sujetos a limpieza y sus marcas de tiempo se actualizan cuando el servidor recibe la solicitud de actualización dinámica de los registros. En el caso de las zonas integradas en Active Directory, este valor se establece en la propiedad *DefaultAgingState* del servidor DNS donde se crea la zona. En el caso de las zonas principales estándar, el valor predeterminado es cero.

</dd> <dt>

**Recibe**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona acepta solicitudes de actualización dinámica.

</dd> <dt>

**Creado automáticamente**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona se ha creado de forma autocreada.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora a la que el servidor puede intentar la eliminación de registros obsoletos de la zona. Incluso si la zona está configurada para habilitar la eliminación de registros obsoletos, el servidor DNS no intentará limpiar esta zona hasta después de este momento. Este valor se establece en la hora actual más el intervalo de actualización de la zona cada vez que se carga la zona. Este parámetro se almacena localmente y no se replica en otras copias de la zona.

</dd> <dt>

**DataFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre del archivo de zona.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se replica el registro WINS. Si se establece en TRUE, la replicación de registros WINS está deshabilitada.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la zona está integrada en DS.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el DNS usa la recursividad cuando se resuelven los nombres de la zona de reenvío especificada. Aplicable solo a zonas de reenvío condicional.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tiempo, en segundos, que un servidor DNS que reenvía una consulta para el nombre en la zona de avance espera la resolución del reenviador antes de intentar resolver la propia consulta. Este parámetro solo es aplicable a las zonas de reenvío.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de segundos desde el comienzo del 1 de enero de 1970 GMT, desde que se comprobó por última vez el número de serie de SOA de la zona.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de segundos desde el comienzo del 1 de enero de 1970 GMT, ya que la zona se transfirió por última vez desde un servidor maestro.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Direcciones IP locales de los servidores DNS maestros para esta zona. Si se establece, estos maestros sobrepasan los MasterServers encontrados en Active Directory.

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Direcciones IP de los servidores DNS maestros para esta zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el intervalo de tiempo entre la última actualización de la marca de tiempo de un registro y el momento más antiguo en el que se puede actualizar la marca de tiempo.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona maestra notifica los cambios en la base de datos de RRs a las secundarias. Establézcalo en 1 para notificar a las secundarias.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumeran las direcciones IP de los servidores DNS a los que se notificarán los cambios en esta zona.

</dd> <dt>

**En pausa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona está en pausa.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el intervalo de actualización, durante el cual se espera que los registros con una marca de tiempo que no sea cero se actualicen para permanecer en la zona. Los registros que no se han actualizado mediante la expiración del intervalo de actualización podrían quitarse mediante la siguiente eliminación de registros obsoletos realizada por un servidor. Este valor nunca debe ser menor que el período de actualización más largo de los registros registrados en la zona. Los valores demasiado pequeños pueden dar lugar a la eliminación de registros DNS válidos. los valores demasiado grandes prolongan la duración de los registros obsoletos. Este valor se establece en la propiedad *defaultrefreshinterval,* del servidor DNS donde se crea la zona.

</dd> <dt>

**Viceversa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona es inversa (TRUE) o adelantada (FALSE).

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumera la lista de direcciones IP de los servidores DNS que pueden realizar la eliminación de registros obsoletos de esta zona. Si no se especifica la lista, se permite a cualquier servidor DNS principal autorizado para la zona borrar la zona cuando se cumplen otros requisitos previos.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumeran las direcciones IP de los servidores DNS que permiten recibir esta zona a través de la replicación de zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se permite la transferencia de zona solo a las secundarias designadas. Las secundarias designadas son servidores DNS cuyas direcciones IP se enumeran en SecondariesIPAddressesArray.

</dd> <dt>

**Apagar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la copia de la zona ha expirado. Si es TRUE, la zona ha expirado o se ha cerrado.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Este valor booleano indica si la zona utiliza la búsqueda inversa de NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona utiliza la búsqueda de WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tipo de la zona. Los valores válidos son:

-   DS integrado
-   Principal
-   Secundario

* * Windows Server 2003: * *

Valores adicionales:

-   Cache
-   Agrupa
-   Reenviador

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dominio MicrosoftDNS**](microsoftdns-domain.md)
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

[**Método ResetSecondaries de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la \_ clase de zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





