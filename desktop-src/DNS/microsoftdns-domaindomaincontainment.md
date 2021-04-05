---
title: MicrosoftDNS_DomainDomainContainment (clase)
description: La \_ clase MicrosoftDNS DomainDomainContainment se usa para la contención de dominio; Los dominios DNS pueden contener otros dominios DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- DNS de la clase MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079617"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>MicrosoftDNS ( \_ clase DomainDomainContainment)

La clase **MicrosoftDNS \_ DomainDomainContainment** se usa para la contención de dominio; Los dominios DNS pueden contener otros dominios DNS. Cada instancia de la clase de [**\_ dominio microsoftdns**](microsoftdns-domain.md) puede contener varias instancias del **\_ dominio microsoftdns**. Una instancia de un objeto de **\_ dominio microsoftdns** se encuentra directamente en no más de un **\_ dominio MicrosoftDNS** de nivel superior.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ DomainDomainContainment** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ DomainDomainContainment** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, máximo (1), invalidación ("GroupComponent")

Descripción: un dominio de nivel superior, zona, caché o RootHints.

Heredado del \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, invalidación ("PartComponent")

Descripción: el dominio contenido en un dominio de nivel superior, zona, caché o RootHints.

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

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





