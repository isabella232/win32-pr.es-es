---
description: Un propietario de objetos tiene implícitamente \_ el acceso de escritura de DAC al objeto. Esto significa que el propietario puede modificar la lista de control de acceso discrecional (DACL) de los objetos y, por tanto, puede controlar el acceso al objeto.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Propietario de un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667919"
---
# <a name="owner-of-a-new-object"></a>Propietario de un nuevo objeto

El propietario de un objeto tiene implícitamente \_ el acceso de escritura de DAC al objeto. Esto significa que el propietario puede modificar la lista de [*control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto y, por tanto, puede controlar el acceso al objeto.

El propietario de un nuevo objeto es el identificador de [*seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del propietario predeterminado del token de [*suplantación*](/windows/desktop/SecGloss/i-gly) o [*principal*](/windows/desktop/SecGloss/p-gly) del [*proceso*](/windows/desktop/SecGloss/p-gly)de creación. Para obtener o establecer el propietario predeterminado en un [*token de acceso*](/windows/desktop/SecGloss/a-gly), llame a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la estructura del [**\_ propietario del token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) . El sistema no permite establecer el propietario predeterminado de un token en un SID que no sea válido, como el SID de la cuenta de otro usuario.

Un proceso con el \_ \_ privilegio de Take Ownership habilitado se puede establecer como propietario de un objeto. Un proceso con el \_ privilegio de nombre de restauración se \_ habilitado o con acceso de propietario de escritura \_ al objeto puede establecer cualquier SID de usuario o grupo válido como propietario de un objeto.

 

 
