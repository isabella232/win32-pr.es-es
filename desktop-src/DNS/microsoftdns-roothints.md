---
title: MicrosoftDNS_RootHints (clase)
description: La \_ clase MicrosoftDNS RootHints describe el RootHints almacenado en un archivo caché en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS de la clase MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints de la clase DNS, descrito
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
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150445"
---
# <a name="microsoftdns_roothints-class"></a>MicrosoftDNS ( \_ clase RootHints)

La clase **MicrosoftDNS \_ RootHints** describe el RootHints almacenado en un archivo caché en un servidor DNS. Esta clase simplifica la visualización de la contención de objetos DNS, en lugar de representar un objeto real.

**MicrosoftDNS \_ RootHints** es un contenedor para los registros de recursos almacenados por el servidor DNS en un archivo caché. Cada instancia de la clase **MicrosoftDNS \_ RootHints** debe estar asignada exactamente a un servidor DNS. Puede estar asociado a varias instancias de la clase [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ RootHints** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ RootHints** tiene estos métodos.



| Método                        | Descripción                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Recupera el nombre distintivo de la zona. <br/> Calificadores: implementados<br/>   |
| **WriteBackRootHintDatafile** | Vuelve a escribir RootHints en el archivo de caché DNS. <br/> Calificadores: implementados<br/> |



 

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

[**Método WriteBackRootHintDatafile de la \_ clase MicrosoftDNS RootHints**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Método GetDistinguishedName de la \_ clase MicrosoftDNS RootHints**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





