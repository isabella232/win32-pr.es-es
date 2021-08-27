---
title: MicrosoftDNS_Cache clase
description: La clase MicrosoftDNS \_ Cache describe una memoria caché existente en un servidor DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache DNS de clase
- MicrosoftDNS_Cache clase DNS , descrita
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
ms.openlocfilehash: 03728a82f7668e38e43c92e3edacff1717333c6b073ee3491389723fb63b5f7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077075"
---
# <a name="microsoftdns_cache-class"></a>Clase MicrosoftDNS \_ Cache

La **clase MicrosoftDNS \_ Cache** describe una memoria caché existente en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real. La **clase MicrosoftDNS \_ Cache** es un contenedor para los registros de recursos almacenados en caché por el servidor DNS. No confunda esto con un archivo de caché que contenga sugerencias raíz.

Todas las instancias de la **clase MicrosoftDNS \_ Cache** deben asignarse exactamente a un servidor DNS. Puede estar asociado a varias instancias de las clases [**MicrosoftDNS \_ Domain o**](microsoftdns-domain.md) [**MicrosoftDNS \_ ResourceRecord.**](microsoftdns-resourcerecord.md)

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ Cache** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ Cache** tiene estos métodos.



| Método                   | Descripción                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Borra la caché del servidor DNS de los registros de recursos. <br/> Calificadores: Implementado<br/> |
| **GetDistinguishedName** | Recupera el nombre distintivo de la zona. <br/> Calificadores: Implementado<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dominio de \_ MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método ClearCache de la clase de caché MicrosoftDNS \_**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase de caché MicrosoftDNS \_**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





