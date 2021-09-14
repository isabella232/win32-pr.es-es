---
description: Un propietario de objetos tiene implícitamente acceso \_ DE DAC DE ESCRITURA al objeto. Esto significa que el propietario puede modificar la lista de control de acceso discrecional (DACL) de los objetos y, por tanto, puede controlar el acceso al objeto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Propietario de un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265476"
---
# <a name="owner-of-a-new-object"></a>Propietario de un nuevo objeto

El propietario de un objeto tiene implícitamente acceso \_ DE DAC DE ESCRITURA al objeto. Esto significa que el propietario puede modificar la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) del objeto y, por tanto, puede controlar el acceso al objeto.

El propietario de un nuevo objeto es el identificador [](/windows/desktop/SecGloss/p-gly) de seguridad de propietario [](/windows/desktop/SecGloss/s-gly) (SID) predeterminado del token principal o de [*suplantación*](/windows/desktop/SecGloss/i-gly) del proceso de [*creación.*](/windows/desktop/SecGloss/p-gly) Para obtener o establecer el propietario predeterminado en un [*token*](/windows/desktop/SecGloss/a-gly)de acceso, llame a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la [**estructura TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_owner) OWNER. El sistema no permite establecer el propietario predeterminado de un token en un SID que no es válido, como el SID de la cuenta de otro usuario.

Un proceso con el SE el privilegio \_ TAKE OWNERSHIP habilitado puede \_ establecerse como propietario de un objeto. Un proceso con el SE restore NAME habilitado o con acceso WRITE OWNER al objeto puede establecer cualquier SID de usuario o grupo válido como \_ \_ propietario de un \_ objeto.

 

 
