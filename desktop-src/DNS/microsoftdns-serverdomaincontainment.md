---
title: MicrosoftDNS_ServerDomainContainment (clase)
description: Cada instancia de la \_ clase WMI de la Asociación de servidor microsoftdns puede contener varias instancias de la clase de dominio microsoftdns \_ .
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- DNS de la clase MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d160176b51fc518ff2d00ef87bf08a812ee4d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801351"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>MicrosoftDNS ( \_ clase ServerDomainContainment)

Cada instancia de la clase WMI de la Asociación de [**\_ servidor microsoftdns**](microsoftdns-server.md) puede contener varias instancias de la clase de [**\_ dominio microsoftdns**](microsoftdns-domain.md) . Cada instancia de la clase de **\_ dominio microsoftdns** pertenece a una única instancia de la clase de **\_ servidor microsoftdns** y se define como débil para ese servidor.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ ServerDomainContainment** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ ServerDomainContainment** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servidor MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, invalidación ("GroupComponent"), mín. (1), máx. (1)

Descripción: el servidor DNS.

Heredado **del \_ componente CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ dominio MicrosoftDNS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: clave, invalidación ("PartComponent")

Descripción: dominio, zona, caché o RootHints administrado por el servidor DNS.

Heredado **del \_ componente CIM**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **MicrosoftDNS \_ ServerDomainContainment** se deriva de la clase del **\_ componente CIM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





