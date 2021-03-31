---
title: MicrosoftDNS_Cache (clase)
description: La \_ clase de caché MicrosoftDNS describe una caché existente en un servidor DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS de la clase MicrosoftDNS_Cache
- MicrosoftDNS_Cache de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079382"
---
# <a name="microsoftdns_cache-class"></a>\_Clase de caché MicrosoftDNS

La clase de **\_ caché MicrosoftDNS** describe una caché existente en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real. La clase de **\_ caché MicrosoftDNS** es un contenedor para los registros de recursos almacenados en memoria caché por el servidor DNS. No lo confunda con un archivo caché que contiene sugerencias de raíz.

Cada instancia de la clase **de \_ caché MicrosoftDNS** debe asignarse exactamente a un servidor DNS. Puede estar asociado a varias instancias de las clases de [**\_ dominio Microsoftdns**](microsoftdns-domain.md) o [**microsoftdns \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Miembros

La clase de **\_ caché MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase de **\_ caché MicrosoftDNS** tiene estos métodos.



| Método                   | Descripción                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Borra la memoria caché del servidor DNS de los registros de recursos. <br/> Calificadores: implementados<br/> |
| **GetDistinguishedName** | Recupera el nombre distintivo de la zona. <br/> Calificadores: implementados<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dominio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método ClearCache de la \_ clase cache MicrosoftDNS**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase cache MicrosoftDNS**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





