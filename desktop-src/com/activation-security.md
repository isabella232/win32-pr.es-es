---
title: Seguridad de activación
description: Seguridad de activación
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488366"
---
# <a name="activation-security"></a><span data-ttu-id="a164e-103">Seguridad de activación</span><span class="sxs-lookup"><span data-stu-id="a164e-103">Activation Security</span></span>

<span data-ttu-id="a164e-104">La seguridad de activación (también denominada seguridad de inicio) ayuda a controlar quién puede iniciar un servidor.</span><span class="sxs-lookup"><span data-stu-id="a164e-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="a164e-105">El administrador de control de servicios (SCM) de un equipo determinado aplica automáticamente la seguridad de activación.</span><span class="sxs-lookup"><span data-stu-id="a164e-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="a164e-106">Tras recibir una solicitud de un cliente para activar un objeto (tal y como se describe en [funciones auxiliares de creación de instancias](instance-creation-helper-functions.md)), el SCM comprueba la solicitud con la información de seguridad de activación almacenada en el registro.</span><span class="sxs-lookup"><span data-stu-id="a164e-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="a164e-107">(La seguridad de activación también se comprueba para las activaciones del mismo equipo).</span><span class="sxs-lookup"><span data-stu-id="a164e-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="a164e-108">Al determinar la identidad del cliente, la activación examina la marca de Cloaking establecida en la llamada del cliente a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a164e-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a164e-109">Si se establece la marca de Cloaking (para Cloaking dinámico o estático), se utiliza el token de subproceso, si está presente, para determinar la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="a164e-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="a164e-110">Si no se establece ningún Cloaking, se utiliza el token de proceso en lugar del token de subproceso.</span><span class="sxs-lookup"><span data-stu-id="a164e-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="a164e-111">Para obtener más información sobre la seguridad de activación, consulte [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) y [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="a164e-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a164e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a164e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a164e-113">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="a164e-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 