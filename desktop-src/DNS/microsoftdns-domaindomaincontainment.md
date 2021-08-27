---
title: MicrosoftDNS_DomainDomainContainment clase
description: La clase DomainDomainContainment de MicrosoftDNS se \_ usa para la contención del dominio; Los dominios DNS pueden contener otros dominios DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment dns de clase
- MicrosoftDNS_DomainDomainContainment clase DNS , descrita
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
ms.openlocfilehash: f8f96d03f007af463fb4c4f672eb0d1374867636f4a4224469589563b9c5882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084755"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>Clase DomainDomainContainment de MicrosoftDNS \_

La **clase \_ DomainDomainContainment de MicrosoftDNS** se usa para la contención del dominio; Los dominios DNS pueden contener otros dominios DNS. Cada instancia de la [**clase de dominio MicrosoftDNS \_**](microsoftdns-domain.md) puede contener varias otras instancias del **dominio MicrosoftDNS \_**. Una instancia de un **objeto de dominio MicrosoftDNS \_** se encuentra directamente en no más de un dominio **MicrosoftDNS de nivel \_ superior.**

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DomainDomainContainment de MicrosoftDNS** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DomainDomainContainment de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Max(1), Override("GroupComponent")

Descripción: dominio, zona, caché o roothints de nivel superior.

Se hereda del \_ componente CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Override("PartComponent")

Descripción: dominio contenido por un dominio, zona, caché o roothints de nivel superior.

Se hereda del componente \_ CIM.

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

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





