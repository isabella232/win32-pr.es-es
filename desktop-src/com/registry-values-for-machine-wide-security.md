---
title: Valores del registro para la seguridad de System-Wide
description: Valores del registro para la seguridad de System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994089"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="4ace5-103">Valores del registro para la seguridad de System-Wide</span><span class="sxs-lookup"><span data-stu-id="4ace5-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="4ace5-104">No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="4ace5-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="4ace5-105">Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="4ace5-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="4ace5-106">Para obtener más información acerca de cómo establecer la seguridad de todo el proceso, consulte Configuración de la [seguridad de Process-Wide](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="4ace5-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="4ace5-107">Ciertos valores del registro se usan para determinar la configuración de seguridad de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="4ace5-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="4ace5-108">Puede usar Dcomcnfg.exe para modificar estos valores de seguridad predeterminados para un equipo.</span><span class="sxs-lookup"><span data-stu-id="4ace5-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="4ace5-109">Para conocer los procedimientos paso a paso que describen cómo usar Dcomcnfg.exe con este fin, vea [establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="4ace5-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="4ace5-110">Otra manera de cambiar la configuración predeterminada para todo el sistema es manipular los valores del registro directamente.</span><span class="sxs-lookup"><span data-stu-id="4ace5-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="4ace5-111">Sin embargo, solo los administradores y el sistema tienen acceso total a la parte del registro que contiene la configuración predeterminada de seguridad de llamadas en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="4ace5-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="4ace5-112">Todos los demás usuarios tienen solo acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="4ace5-112">All other users have read-access only.</span></span>

<span data-ttu-id="4ace5-113">Los valores con nombre que afectan a los valores predeterminados de seguridad del sistema son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ace5-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="4ace5-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="4ace5-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="4ace5-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="4ace5-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="4ace5-116">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="4ace5-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="4ace5-117">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="4ace5-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="4ace5-118">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="4ace5-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="4ace5-119">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="4ace5-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="4ace5-120">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="4ace5-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="4ace5-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ace5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ace5-122">Configuración de la seguridad de Process-Wide</span><span class="sxs-lookup"><span data-stu-id="4ace5-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




