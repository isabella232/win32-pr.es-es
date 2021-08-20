---
title: MicrosoftDNS_Zone clase
description: La clase MicrosoftDNS \_ Zone describe una zona DNS. Todas las instancias de la clase Zona De MicrosoftDNS \_ deben asignarse exactamente a un servidor DNS. Las zonas pueden asociarse a varias instancias de las clases MicrosoftDNS Domain o \_ MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone dns de clase
- MicrosoftDNS_Zone clase DNS , descrita
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
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957184"
---
# <a name="microsoftdns_zone-class"></a>Clase MicrosoftDNS \_ Zone

> [!NOTE]
> Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

> [!NOTE]
> Este artículo contiene referencias al término servidor maestro, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

La **clase MicrosoftDNS \_ Zone** describe una zona DNS. Todas las instancias de la **clase Zona De MicrosoftDNS \_** deben asignarse exactamente a un servidor DNS. Las zonas pueden asociarse a varias instancias de las [**clases MicrosoftDNS \_ Domain**](microsoftdns-domain.md) o [**MicrosoftDNS \_ ResourceRecord.**](microsoftdns-resourcerecord.md)

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase MicrosoftDNS \_ Zone** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ Zone** tiene estos métodos.



| Método                   | Descripción                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Habilita el tiempo de vida de algunos o todos los registros que no son NS y que no son SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Cambia los tipos de zona. <br/> Calificadores: Implementado<br/>                                                                                                                                         |
| **CreateZone**           | Crea una nueva zona. <br/> Calificadores: None.<br/>                                                                                                                                               |
| **ForceRefresh**         | Fuerza una actualización de la base de datos secundaria desde el servidor DNS maestro. <br/> Calificadores: Implementado<br/>                                                                                               |
| **GetDistinguishedName** | Obtiene el nombre distintivo de DS para la zona. <br/> Calificadores: Implementado<br/>                                                                                                                 |
| **PauseZone**            | Pausa la zona. <br/> Calificadores: Implementado<br/>                                                                                                                                            |
| **ReloadZone**           | Vuelve a cargar la zona. <br/> Calificadores: Implementado<br/>                                                                                                                                           |
| **ResetSecondaries**     | Restablece la matriz de direcciones IP secundarias. <br/> Calificadores: Implementado<br/>                                                                                                                      |
| **ResumeZone**           | Reanuda la zona. <br/> Calificadores: Implementado<br/>                                                                                                                                           |
| **UpdateFromDS**         | Fuerza una actualización de la zona desde el servicio de directorio (DS). Para que este método sea válido, ZoneType debe ser 0; la zona debe almacenarse realmente en el DS. <br/> Calificadores: Implementado<br/> |
| **WriteBackZone**        | Guarda los datos de zona en su archivo de zona. <br/> Calificadores: implementados, estáticos<br/>                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ Zone** tiene estas propiedades.

<dl> <dt>

**Envejecimiento**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el comportamiento de anticuado y de búsqueda de la zona. Cero indica que la búsqueda está deshabilitada. Cuando la búsqueda de archivos está deshabilitada, las marcas de tiempo de los registros de la zona no se actualizan y los registros no están sujetos a scavenging. Cuando se establece en uno, los registros se somete a scavenging y sus marcas de tiempo se actualizan cuando el servidor recibe la solicitud de actualización dinámica de los registros. Para Active Directory integradas, este valor se establece en la *propiedad DefaultAgingState* del servidor DNS donde se crea la zona. En el caso de las zonas primarias estándar, el valor predeterminado es cero.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona acepta solicitudes de actualización dinámicas.

</dd> <dt>

**AutoCreated**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona se crea automáticamente.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la hora a la que el servidor puede intentar buscar la zona. Incluso si la zona está configurada para habilitar la búsqueda del servidor DNS, no intentará buscar esta zona hasta después de este momento. Este valor se establece en la hora actual más el intervalo de actualización de la zona cada vez que se carga la zona. Este parámetro se almacena localmente y no se replica en otras copias de la zona.

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

**ForwarderVicee**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el DNS usa recursividad al resolver los nombres de la zona de reenvío especificada. Solo se aplica a las zonas de reenvío condicional.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tiempo, en segundos, que un servidor DNS reenvía una consulta para el nombre en la zona de reenvío espera la resolución del reenviador antes de intentar resolver la propia consulta. Este parámetro solo es aplicable a las zonas de reenvío.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de segundos desde el principio del 1 de enero de 1970 GMT, desde que se comprobó por última vez el número de serie soA de la zona.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de segundos desde el principio del 1 de enero de 1970 GMT, desde que la zona se transfirieron por última vez desde un servidor maestro.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Direcciones IP locales de los servidores DNS maestros para esta zona. Si se establece, estos maestros sobrecarbue los MasterServers que se encuentran en Active Directory.

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Direcciones IP de los servidores DNS maestros para esta zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el intervalo de tiempo entre la última actualización de la marca de tiempo de un registro y el momento más antiguo en que se puede actualizar la marca de tiempo.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona maestra notifica a las secundarias los cambios en su base de datos de RR. Establezca en 1 para notificar a las secundarias.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumera las direcciones IP de los servidores DNS a los que se notificarán los cambios en esta zona.

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

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el intervalo de actualización, durante el cual se espera que los registros con marca de tiempo distinto de cero se actualicen para permanecer en la zona. La siguiente búsqueda realizada por un servidor podría quitar los registros que no se hayan actualizado al expirar el intervalo de actualización. Este valor nunca debe ser menor que el período de actualización más largo de los registros registrados en la zona. Los valores demasiado pequeños pueden provocar la eliminación de registros DNS válidos. los valores que son demasiado grandes prorrogar la duración de los registros obsoletos. Este valor se establece en la *propiedad DefaultRefreshInterval* del servidor DNS donde se crea la zona.

</dd> <dt>

**Marcha atrás**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona es inversa (TRUE) o hacia delante (FALSE).

</dd> <dt>

**ScaveaveaveServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumera la lista de direcciones IP de servidores DNS que pueden realizar la búsqueda de registros obsoletos de esta zona. Si no se especifica la lista, cualquier servidor DNS principal autoritativo para la zona puede buscar la zona cuando se cumplan otros requisitos previos.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que enumera las direcciones IP de los servidores DNS que pueden recibir esta zona a través de la replicación de zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la transferencia de zona solo se permite a las secundarias designadas. Las secundarias designadas son servidores DNS cuyas direcciones IP se enumeran en SecondariesIPAddressesArray.

</dd> <dt>

**Apagar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la copia de la zona ha expirado. Si es TRUE, la zona ha expirado o se ha apagado.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Este valor booleano indica si la zona usa la búsqueda inversa NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la zona usa la apariencia WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tipo de zona. Los valores válidos son:

-   DS integrado
-   Principal
-   Secundario

**Windows Server 2003: **

Valores adicionales:

-   Cache
-   Trozo
-   Reenviador

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dominio de \_ MicrosoftDNS**](microsoftdns-domain.md)
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

[**Método UpdateFromDS de la clase de zona MicrosoftDNS \_**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone de la clase Zone de MicrosoftDNS \_**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





