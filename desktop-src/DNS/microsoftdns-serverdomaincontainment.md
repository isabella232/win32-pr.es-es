---
title: MicrosoftDNS_ServerDomainContainment clase
description: Cada instancia de la clase WMI de asociación de servidor MicrosoftDNS puede contener \_ varias instancias de la clase de dominio MicrosoftDNS. \_
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment dns de clase
- MicrosoftDNS_ServerDomainContainment clase DNS , descrita
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
ms.openlocfilehash: bdc747cae72ac4733ad9bec7288858731b6250312d43476a000d2f99a989267d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527255"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>Clase MicrosoftDNS \_ ServerDomainContainment

Cada instancia de la clase WMI de asociación de servidor [**MicrosoftDNS \_**](microsoftdns-server.md) puede contener varias instancias de la [**clase de dominio MicrosoftDNS. \_**](microsoftdns-domain.md) Cada instancia de la **clase de dominio MicrosoftDNS \_** pertenece a una única instancia de la clase de servidor **\_ MicrosoftDNS** y se define como débil para ese servidor.

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

La **clase \_ ServerDomainContainment de MicrosoftDNS** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ServerDomainContainment de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **MicrosoftDNS \_ Server**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Override ("GroupComponent"), Min (1), Max (1)

Descripción: el servidor DNS.

Se hereda del **componente \_ CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Dominio MicrosoftDNS \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Calificadores: Key, Override("PartComponent")

Descripción: dominio, zona, caché o roothints administrados por el servidor DNS.

Se hereda del **componente \_ CIM**.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ ServerDomainContainment de MicrosoftDNS** se deriva de la **clase Cim \_ Component.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dominio de \_ MicrosoftDNSDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





