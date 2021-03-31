---
title: MicrosoftDNS_DomainResourceRecordContainment (clase)
description: La \_ clase MicrosoftDNS DomainResourceRecordContainment se usa para la contención de RR; cada instancia del \_ dominio MicrosoftDNS puede contener varias instancias de la \_ clase MicrosoftDNS ResourceRecord.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- DNS de la clase MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490648"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>MicrosoftDNS ( \_ clase DomainResourceRecordContainment)

La clase **MicrosoftDNS \_ DomainResourceRecordContainment** se usa para la contención de RR; cada instancia [**del \_ dominio MicrosoftDNS**](microsoftdns-domain.md) puede contener varias instancias de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) . Cada instancia de la clase **MicrosoftDNS \_ ResourceRecord** pertenece a una única instancia de la clase de **\_ dominio microsoftdns** y se define como débil para esa instancia.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ DomainResourceRecordContainment** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ DomainResourceRecordContainment** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, invalidación ("GroupComponent")

Descripción: la zona, la memoria caché, el RootHints o el dominio que contiene directamente el registro de recursos.

Heredado del \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, invalidación ("PartComponent")

Descripción: el registro de recursos contenido en un dominio, zona, caché o RootHints.

Heredado del \_ componente CIM.

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

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





