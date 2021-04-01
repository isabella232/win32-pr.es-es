---
title: MicrosoftDNS_Domain (clase)
description: La \_ clase de dominio MicrosoftDNS representa un dominio en una jerarquía de DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- DNS de la clase MicrosoftDNS_Domain
- MicrosoftDNS_Domain de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150295"
---
# <a name="microsoftdns_domain-class"></a>\_Clase de dominio MicrosoftDNS

La clase de **\_ dominio MicrosoftDNS** representa un dominio en una jerarquía de DNS.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Miembros

La clase de **\_ dominio MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ dominio MicrosoftDNS** tiene estos métodos.



| Método                   | Descripción                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Obtiene el nombre distintivo de DS para la zona. <br/> Calificadores: implementados<br/> |



 

### <a name="properties"></a>Propiedades

La clase de **\_ dominio MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del contenedor del dominio, que podría ser una zona, caché o RootHints.

En los casos en los que el contenedor es una zona (una instancia de la clase de [**\_ zona MicrosoftDNS**](microsoftdns-zone.md) ), esta propiedad contiene el FQDN de la zona.

Cuando el contenedor es la zona raíz, \\ \\ se debe usar la cadena.

En los casos en los que el contenedor es la memoria caché de DNS de los registros de recursos (una instancia de la clase de [**\_ caché MicrosoftDNS**](microsoftdns-cache.md) ), esta propiedad se establece en la cadena \\ . Caché \\ .

Si el contenedor es RootHints (una instancia de la clase [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), esta propiedad debe establecerse en \\ . RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN o dirección IP del servidor DNS que contiene el dominio.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN del dominio.

En el caso de instancias de caché DNS o RootHints, las cadenas \\ . Almacenar en caché \\ y \\ .. \\ Se debe usar RootHints, respectivamente.

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

[**Método GetDistinguishedName de la \_ clase de dominio MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





