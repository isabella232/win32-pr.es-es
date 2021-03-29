---
description: Cada usuario y el identificador de seguridad de grupo (SID) de un token de acceso tiene un conjunto de atributos que controlan el modo en que el sistema utiliza el SID en una comprobación de acceso. En la tabla siguiente se enumeran los atributos que controlan la comprobación de acceso.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Atributos SID en un token de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a93e180c8c6ffe03a26591d5b9f722c2266356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810706"
---
# <a name="sid-attributes-in-an-access-token"></a>Atributos SID en un token de acceso

Cada usuario y el [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) de grupo (SID) de un [*token de acceso*](/windows/desktop/SecGloss/a-gly) tiene un conjunto de atributos que controlan el modo en que el sistema utiliza el SID en una comprobación de acceso. En la tabla siguiente se enumeran los atributos que controlan la comprobación de acceso.



| Atributo                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grupo de SE \_ \_ habilitado              | Un SID con este atributo está habilitado para las comprobaciones de acceso. Cuando el sistema realiza una comprobación de acceso, comprueba [*las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) permitidas y de acceso denegado que se aplican a uno de los SID habilitados en el token de acceso. Un SID sin este atributo se omite durante una comprobación de acceso, a menos que \_ \_ se establezca el atributo de uso del grupo se \_ para \_ solo denegar \_ .<br/> |
| \_ \_ uso de grupo \_ de se para \_ denegar \_ únicamente | Un SID con este atributo es un SID de solo denegación. Cuando el sistema realiza una comprobación de acceso, comprueba las ACE de acceso denegado que se aplican al SID, pero omite las ACE con acceso permitido para el SID. Si se establece este atributo, no se \_ establece el atributo de grupo se \_ habilitado y no se puede volver a habilitar el SID.<br/>                                                                                                                                                          |



 

Para establecer o borrar el \_ \_ atributo de grupo se habilitado de un SID de grupo, utilice la función [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) . No se puede deshabilitar un SID de grupo que tenga el \_ atributo obligatorio de grupo se \_ . No se puede usar **AdjustTokenGroups** para deshabilitar el SID de usuario de un token de acceso.

Para determinar si un SID está habilitado en un token, es decir, si tiene el \_ atributo de grupo se \_ habilitado, llame a la función [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) .

Para establecer el \_ atributo se \_ usa \_ para \_ el \_ atributo de solo denegación de un SID, incluya el SID en la lista de SID de solo denegación que especifique al llamar a la función [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . **CreateRestrictedToken** puede aplicar el \_ uso del grupo se para el \_ \_ \_ \_ atributo solo denegar a cualquier SID, incluidos los SID de usuario y de grupo que tienen el \_ atributo obligatorio de grupo se \_ . Sin embargo, no se puede quitar el atributo de solo denegación de un SID, ni se puede usar [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) para establecer el \_ atributo de grupo se \_ habilitado en un SID de solo denegación.

Para obtener los atributos de un SID, llame a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con el valor TokenGroups. La función devuelve una matriz de estructuras de [**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) que identifican los SID de grupo y sus atributos.

 

