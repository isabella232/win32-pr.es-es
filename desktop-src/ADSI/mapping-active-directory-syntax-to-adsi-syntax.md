---
title: Asignación Active Directory sintaxis a la sintaxis ADSI
description: En la tabla siguiente se asigna la Active Directory sintaxis a sus sintaxis ADSI correspondientes.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- atributos ADSI, asignación Active Directory sintaxis a sintaxis ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04682a1e299e14c55c520310bff697ea6664d4dabe71380f7a146fd2dfff053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179283"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Asignación Active Directory sintaxis a la sintaxis ADSI

En la tabla siguiente se asigna la Active Directory sintaxis a sus sintaxis ADSI correspondientes.



| Identificador de sintaxis de atributo | Active Directory de sintaxis             | Tipo de sintaxis ADSI equivalente                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Cadena de DN<br/>                     | Cadena de DN<br/>                                                |
| 2.5.5.2<br/>  | Identificador de objeto<br/>                     | CaseIgnore String<br/>                                        |
| 2.5.5.3<br/>  | Cadena que distingue mayúsculas de minúsculas<br/>         | CaseExact String<br/>                                         |
| 2.5.5.4<br/>  | Cadena omitido por mayúsculas y minúsculas<br/>           | CaseIgnore String<br/>                                        |
| 2.5.5.5<br/>  | Cadena de caso de impresión<br/>             | Cadena imprimible<br/>                                         |
| 2.5.5.6<br/>  | Cadena numérica<br/>                | Cadena numérica<br/>                                           |
| 2.5.5.7<br/>  | **O BIEN** Nombre DNWithOctetString<br/> | No compatible<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Entero<br/>                       | Entero<br/>                                                  |
| 2.5.5.10<br/> | Cadena de octeto<br/>                  | Cadena de octeto<br/>                                             |
| 2.5.5.11<br/> | Time<br/>                          | Hora UTC<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Case Ignore String<br/>                                       |
| 2.5.5.13<br/> | Dirección<br/>                       | No compatible<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | NT Security Descriptor<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Entero grande<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Cadena de octeto<br/>                                             |



 

 

 





