---
title: LegacyAuthenticationLevel
description: Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman a CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valor del registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076372"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="ab890-104">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="ab890-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="ab890-105">Establece el nivel de autenticación predeterminado para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="ab890-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="ab890-106">No se recomienda cambiar este valor, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab890-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="ab890-107">Si va a cambiar este valor para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="ab890-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="ab890-108">Para obtener más información sobre cómo establecer la seguridad de todo el proceso, consulte [configuración de la seguridad de todo el proceso](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="ab890-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="ab890-109">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="ab890-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="ab890-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab890-110">Remarks</span></span>

<span data-ttu-id="ab890-111">Se trata de un valor de **\_ palabra de registro** equivalente a las \_ constantes de nivel de autenticación de RPC C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab890-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="ab890-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ab890-112">Value</span></span> | <span data-ttu-id="ab890-113">Constante</span><span class="sxs-lookup"><span data-stu-id="ab890-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="ab890-114">1</span><span class="sxs-lookup"><span data-stu-id="ab890-114">1</span></span>     | <span data-ttu-id="ab890-115">nivel de autenticación de RPC \_ C \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="ab890-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="ab890-116">2</span><span class="sxs-lookup"><span data-stu-id="ab890-116">2</span></span>     | <span data-ttu-id="ab890-117">\_conexión de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="ab890-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="ab890-118">3</span><span class="sxs-lookup"><span data-stu-id="ab890-118">3</span></span>     | <span data-ttu-id="ab890-119">\_llamada de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="ab890-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="ab890-120">4</span><span class="sxs-lookup"><span data-stu-id="ab890-120">4</span></span>     | <span data-ttu-id="ab890-121">\_PKT de \_ nivel de \_ autenticación \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="ab890-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="ab890-122">5</span><span class="sxs-lookup"><span data-stu-id="ab890-122">5</span></span>     | <span data-ttu-id="ab890-123">integridad de la PKT de nivel de autenticación de RPC \_ C \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab890-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="ab890-124">6</span><span class="sxs-lookup"><span data-stu-id="ab890-124">6</span></span>     | <span data-ttu-id="ab890-125">\_privacidad de \_ nivel de \_ autenticación \_ de RPC C \_</span><span class="sxs-lookup"><span data-stu-id="ab890-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="ab890-126">Si este valor del registro no está presente, el nivel de autenticación predeterminado establecido por el sistema es 2 (RPC \_ C \_ authn \_ Connect).</span><span class="sxs-lookup"><span data-stu-id="ab890-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab890-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab890-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab890-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="ab890-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="ab890-129">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="ab890-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="ab890-130">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="ab890-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




