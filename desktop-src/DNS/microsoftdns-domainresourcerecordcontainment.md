---
title: MicrosoftDNS_DomainResourceRecordContainment clase
description: La clase DomainResourceRecordContainment de MicrosoftDNS se usa para la contención de RR; cada instancia del dominio MicrosoftDNS puede contener varias instancias de la clase ResourceRecord de \_ \_ MicrosoftDNS. \_
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment DNS de clase
- MicrosoftDNS_DomainResourceRecordContainment clase DNS , descrita
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
ms.openlocfilehash: 498d9b953895ebece94dc77edb587045d1cfdd45c29f04c202756bd1080dc9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795615"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>Clase MicrosoftDNS \_ DomainResourceRecordContainment

La **clase \_ DomainResourceRecordContainment de MicrosoftDNS** se usa para la contención de RR; cada instancia del dominio [**MicrosoftDNS \_**](microsoftdns-domain.md) puede contener varias instancias de la clase [**\_ ResourceRecord de MicrosoftDNS.**](microsoftdns-resourcerecord.md) Cada instancia de la **clase \_ ResourceRecord de MicrosoftDNS** pertenece a una única instancia de la clase De dominio **de MicrosoftDNS \_** y se define como débil para esa instancia.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DomainResourceRecordContainment de MicrosoftDNS** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DomainResourceRecordContainment de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Override("GroupComponent")

Descripción: zona, caché, roothints o dominio que contiene directamente el registro de recursos.

Se hereda del \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ ResourceRecord de MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Override("PartComponent")

Descripción: el registro de recursos contenido en un dominio, zona, caché o roothints.

Se hereda del componente \_ CIM.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**Dominio de \_ MicrosoftDNSDominioContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





