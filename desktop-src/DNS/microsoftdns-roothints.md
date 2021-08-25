---
title: MicrosoftDNS_RootHints clase
description: La clase RootHints de MicrosoftDNS describe los roothints almacenados en un \_ archivo de caché en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints dns de clase
- MicrosoftDNS_RootHints clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050da9acb1d3865fb490035b6de57fcc1279a45b6f9d78c57df305993d590c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913005"
---
# <a name="microsoftdns_roothints-class"></a>Clase RootHints de MicrosoftDNS \_

La **clase \_ RootHints de MicrosoftDNS** describe los roothints almacenados en un archivo de caché en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.

**MicrosoftDNS \_ RootHints es** un contenedor para los registros de recursos almacenados por el servidor DNS en un archivo de caché. Todas las instancias de **la clase \_ RootHints de MicrosoftDNS** deben asignarse exactamente a un servidor DNS. Puede estar asociado a varias instancias de la [**clase \_ ResourceRecord de MicrosoftDNS.**](microsoftdns-resourcerecord.md)

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RootHints de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase \_ RootHints de MicrosoftDNS** tiene estos métodos.



| Método                        | Descripción                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Recupera el nombre distintivo de la zona. <br/> Calificadores: Implementado<br/>   |
| **WriteBackRootHintDatafile** | Escribe RootHints de nuevo en el archivo de caché DNS. <br/> Calificadores: Implementado<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dominio de \_ MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método WriteBackRootHintDatafile de la clase RootHints de MicrosoftDNS \_**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Método GetDistinguishedName de la clase RootHints de MicrosoftDNS \_**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





