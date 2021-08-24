---
title: MicrosoftDNS_ResourceRecord clase
description: La clase ResourceRecord de MicrosoftDNS \_ representa las propiedades generales de un RR de DNS. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord dns de clase
- MicrosoftDNS_ResourceRecord clase DNS , descrita
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
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874805"
---
# <a name="microsoftdns_resourcerecord-class"></a>Clase ResourceRecord de MicrosoftDNS \_

La **clase \_ ResourceRecord de MicrosoftDNS** representa las propiedades generales de un RR de DNS.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase \_ ResourceRecord de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ResourceRecord de MicrosoftDNS** tiene estos métodos.



| Método                                   | Descripción                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analiza el RR en la cadena TextRepresentation y, con los nombres de contenedor y servidor DNS de entrada, define y crea instancias de un objeto ResourceRecord. El método devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Ninguno<br/> |
| **GetObjectByTextRepresentation**        | Recupera una instancia existente de la subclase ResourceRecord de MicrosoftDns, representada por la cadena TextRepresentation junto con el servidor DNS y el \_ nombre del contenedor. <br/> Calificadores: Ninguno<br/>                                                        |



 

### <a name="properties"></a>Propiedades

La **clase \_ ResourceRecord de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre del contenedor para la instancia de Zone, Cache o RootHints que contiene el RR.

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

Representa el FQDN del dominio que contiene el RR. Esta propiedad puede contener las cadenas \\ .. Caché \\ o \\ .. RootHints \\ si la caché interna o RootHints contienen el RR, respectivamente.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del propietario del RR.

</dd> <dt>

**RecordClass=1**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**Windows Server 2003: **

Esta cadena representa la clase del registro de recursos. Los valores válidos son:

1: IN (Internet)

2: CS (CSNET)

3: CH (CHAOS)

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

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se actualizó el RR por última vez, expresada en horas transcurridos desde el 1 de enero de 1601, hora media de Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché [*el RR.*](r-gly.md)

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

[**Método CreateInstanceFromTextRepresentation de la clase ResourceRecord de \_ MicrosoftDNS**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Método GetObjectByTextRepresentation de la clase \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





