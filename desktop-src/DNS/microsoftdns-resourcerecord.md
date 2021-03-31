---
title: MicrosoftDNS_ResourceRecord (clase)
description: La \_ clase MicrosoftDNS ResourceRecord representa las propiedades generales de un RR de DNS. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- DNS de la clase MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996546"
---
# <a name="microsoftdns_resourcerecord-class"></a>MicrosoftDNS ( \_ clase ResourceRecord)

La clase **MicrosoftDNS \_ ResourceRecord** representa las propiedades generales de un RR de DNS.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ ResourceRecord** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ ResourceRecord** tiene estos métodos.



| Método                                   | Descripción                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analiza el RR de la cadena TextRepresentation y con el servidor DNS de entrada y los nombres de contenedor, define y crea instancias de un objeto ResourceRecord. El método devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Ninguno<br/> |
| **GetObjectByTextRepresentation**        | Recupera una instancia existente de la \_ subclase MicrosoftDns ResourceRecord, representada por la cadena TextRepresentation junto con el servidor DNS y el nombre del contenedor. <br/> Calificadores: Ninguno<br/>                                                        |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ ResourceRecord** tiene estas propiedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene el RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el FQDN o la dirección IP del servidor DNS que contiene el RR.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Representa el FQDN del dominio que contiene el RR. Esta propiedad puede contener las cadenas \\ . Almacenar en caché \\ o \\ .. RootHints \\ si la memoria caché interna o RootHints contiene el RR, respectivamente.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del propietario del RR.

</dd> <dt>

**RecordClass = 1**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

* * Windows Server 2003: * *

Esta cadena representa la clase del registro de recursos. Los valores válidos son:

1: en (Internet)

2: CS (CSNET)

3: CH (CAOS)

4: HS (Hesiod)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos de registro de recursos.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Representación de texto de todo el RR.

</dd> <dt>

**Indicaciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se actualizó por última vez el RR, expresado en horas transcurridas desde el 1 de enero de 1601, hora del meridiano de Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, que un [*solucionador*](r-gly.md)DNS puede almacenar en caché el RR.

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

[**Método CreateInstanceFromTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Método GetObjectByTextRepresentation de la \_ clase MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





