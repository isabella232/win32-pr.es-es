---
title: Asignar Active Directory sintaxis a la sintaxis ADSI
description: En la tabla siguiente se asignan las sintaxis de Active Directory a sus correspondientes sintaxis de ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- atributos ADSI, asignar sintaxis Active Directory a la sintaxis ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656165"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Asignar Active Directory sintaxis a la sintaxis ADSI

En la tabla siguiente se asignan las sintaxis de Active Directory a sus correspondientes sintaxis de ADSI.



| IDENTIFICADOR de sintaxis de atributo | Active Directory tipo de sintaxis             | Tipo de sintaxis ADSI equivalente                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Cadena DN<br/>                     | Cadena DN<br/>                                                |
| 2.5.5.2<br/>  | Identificador de objeto<br/>                     | Cadena CaseIgnore<br/>                                        |
| 2.5.5.3<br/>  | Cadena que distingue mayúsculas de minúsculas<br/>         | Cadena CaseExact<br/>                                         |
| 2.5.5.4<br/>  | Caso de cadena omitida<br/>           | Cadena CaseIgnore<br/>                                        |
| 2.5.5.5<br/>  | Cadena de caso de impresión<br/>             | Cadena imprimible<br/>                                         |
| 2.5.5.6<br/>  | Cadena numérica<br/>                | Cadena numérica<br/>                                           |
| 2.5.5.7<br/>  | **O bien** Nombre DNWithOctetString<br/> | No compatible<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Entero<br/>                       | Entero<br/>                                                  |
| 2.5.5.10<br/> | Cadena de octeto<br/>                  | Cadena de octeto<br/>                                             |
| 2.5.5.11<br/> | Hora<br/>                          | Hora UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Distinción de mayúsculas y minúsculas<br/>                                       |
| 2.5.5.13<br/> | Dirección<br/>                       | No compatible<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Descriptor de seguridad de NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Entero grande<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Cadena de octeto<br/>                                             |



 

 

 





