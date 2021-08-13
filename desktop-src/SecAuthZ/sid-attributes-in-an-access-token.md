---
description: Cada identificador de seguridad de usuario y grupo (SID) de un token de acceso tiene un conjunto de atributos que controlan cómo usa el sistema el SID en una comprobación de acceso. En la tabla siguiente se enumeran los atributos que controlan la comprobación de acceso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Atributos de SID en un token de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413425"
---
# <a name="sid-attributes-in-an-access-token"></a>Atributos de SID en un token de acceso

Cada identificador de [*seguridad*](/windows/desktop/SecGloss/s-gly) de usuario y grupo (SID) de un [*token*](/windows/desktop/SecGloss/a-gly) de acceso tiene un conjunto de atributos que controlan cómo usa el sistema el SID en una comprobación de acceso. En la tabla siguiente se enumeran los atributos que controlan la comprobación de acceso.



| Atributo                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_SE GROUP \_ ENABLED              | Un SID con este atributo está habilitado para las comprobaciones de acceso. Cuando el sistema realiza una comprobación de acceso, comprueba si hay entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) con acceso permitido y denegado que se aplican a uno de los SID habilitados en el token de acceso. Un SID sin este atributo se omite durante una comprobación de acceso a menos que se establezca SE \_ atributo GROUP USE FOR DENY \_ \_ \_ \_ ONLY.<br/> |
| \_SE USO \_ DE GRUPOS SOLO PARA \_ \_ DENEGAR \_ | Un SID con este atributo es un SID de solo denegación. Cuando el sistema realiza una comprobación de acceso, comprueba si hay ACE con acceso denegado que se aplican al SID, pero omite las ACE con acceso permitido para el SID. Si se establece este atributo, no se SE el atributo GROUP ENABLED y no se puede volver a \_ \_ habilitar el SID.<br/>                                                                                                                                                          |



 

Para establecer o borrar el SE GROUP ENABLED de un SID de \_ \_ grupo, use la [**función AdjustTokenGroups.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) No se puede deshabilitar un SID de grupo que tenga el SE \_ GROUP \_ MANDATORY. No puede usar **AdjustTokenGroups para** deshabilitar el SID de usuario de un token de acceso.

Para determinar si un SID está habilitado en un token, es decir, si tiene el atributo SE GROUP ENABLED, llame a la \_ \_ función [**CheckTokenMembership.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)

Para establecer el atributo SE GROUP USE FOR DENY ONLY de un SID, incluya el SID en la lista de SID de solo denegación que especifique al llamar a la función \_ \_ \_ \_ \_ [**CreateRestrictedToken.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) **CreateRestrictedToken** puede aplicar el atributo SE GROUP USE FOR DENY ONLY a cualquier \_ \_ \_ \_ \_ SID, incluidos el SID de usuario y los SID de grupo que tienen el SE \_ GROUP \_ MANDATORY. Sin embargo, no puede quitar el atributo de solo denegación de un SID, ni puede usar [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) para establecer el atributo SE GROUP ENABLED en un SID de solo \_ \_ denegación.

Para obtener los atributos de un SID, llame a la [**función GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con el valor TokenGroups. La función devuelve una matriz de [**estructuras SID \_ Y \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) que identifican los SID de grupo y sus atributos.

 

