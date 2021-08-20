---
title: MicrosoftDNS_Domain clase
description: La clase De dominio de MicrosoftDNS \_ representa un dominio en una jerarquía DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain DNS de clase
- MicrosoftDNS_Domain clase DNS , descrita
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
ms.openlocfilehash: a30b171777e6c8a99ddadcfb39c8cdfdd90b09a43ae255c9bbcc026db09bdb1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163324"
---
# <a name="microsoftdns_domain-class"></a>Clase de dominio MicrosoftDNS \_

La **clase De \_ dominio de MicrosoftDNS** representa un dominio en una jerarquía DNS.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase de \_ dominio MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase de \_ dominio MicrosoftDNS** tiene estos métodos.



| Método                   | Descripción                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Obtiene el nombre distintivo de DS para la zona. <br/> Calificadores: Implementado<br/> |



 

### <a name="properties"></a>Propiedades

La **clase de \_ dominio MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del contenedor del dominio, que podría ser Zona, Caché o RootHints.

En los casos en los que el contenedor es una zona (una instancia de la clase [**Zona MicrosoftDNS), \_**](microsoftdns-zone.md) esta propiedad contiene el FQDN de la zona.

Cuando el contenedor es la zona raíz, se debe usar \\ \\ la cadena .

En los casos en los que el contenedor es la caché DNS de los registros de recursos (una instancia de la clase [**MicrosoftDNS \_ Cache),**](microsoftdns-cache.md) esta propiedad se establece en la \\ cadena .. Almacenar en \\ caché .

Si el contenedor es RootHints (una instancia de la clase [**\_ RootHints de MicrosoftDNS),**](microsoftdns-roothints.md) esta propiedad debe establecerse en \\ . RootHints \\ .

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

En el caso de las instancias de Dns Cache o RootHints, las cadenas \\ .. Almacenar \\ en caché y \\ . Se deben usar RootHints, \\ respectivamente.

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

[**Método GetDistinguishedName de la clase de dominio MicrosoftDNS \_**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





