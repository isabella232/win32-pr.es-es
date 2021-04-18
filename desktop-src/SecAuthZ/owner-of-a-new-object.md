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
# <a name="owner-of-a-new-object"></a><span data-ttu-id="0e31c-104">Propietario de un nuevo objeto</span><span class="sxs-lookup"><span data-stu-id="0e31c-104">Owner of a New Object</span></span>

<span data-ttu-id="0e31c-105">El propietario de un objeto tiene implícitamente \_ el acceso de escritura de DAC al objeto.</span><span class="sxs-lookup"><span data-stu-id="0e31c-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="0e31c-106">Esto significa que el propietario puede modificar la lista de [*control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto y, por tanto, puede controlar el acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="0e31c-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="0e31c-107">El propietario de un nuevo objeto es el identificador de [*seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del propietario predeterminado del token de [*suplantación*](/windows/desktop/SecGloss/i-gly) o [*principal*](/windows/desktop/SecGloss/p-gly) del [*proceso*](/windows/desktop/SecGloss/p-gly)de creación.</span><span class="sxs-lookup"><span data-stu-id="0e31c-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="0e31c-108">Para obtener o establecer el propietario predeterminado en un [*token de acceso*](/windows/desktop/SecGloss/a-gly), llame a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la estructura del [**\_ propietario del token**](/windows/desktop/api/Winnt/ns-winnt-token_owner) .</span><span class="sxs-lookup"><span data-stu-id="0e31c-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="0e31c-109">El sistema no permite establecer el propietario predeterminado de un token en un SID que no sea válido, como el SID de la cuenta de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="0e31c-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="0e31c-110">Un proceso con el \_ \_ privilegio de Take Ownership habilitado se puede establecer como propietario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="0e31c-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="0e31c-111">Un proceso con el \_ privilegio de nombre de restauración se \_ habilitado o con acceso de propietario de escritura \_ al objeto puede establecer cualquier SID de usuario o grupo válido como propietario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="0e31c-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
