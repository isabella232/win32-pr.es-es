---
title: Determinación de las necesidades de seguridad
description: La forma de configurar la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación. Hay varias situaciones comunes que determinan lo que debe hacer.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779969"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="d6a0f-104">Determinación de las necesidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="d6a0f-104">Determining Your Security Needs</span></span>

<span data-ttu-id="d6a0f-105">La forma de configurar la seguridad COM para la aplicación depende del tipo de seguridad que necesite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="d6a0f-106">Hay varias situaciones comunes que determinan lo que debe hacer.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="d6a0f-107">Si decide usar los valores predeterminados de seguridad COM, no tiene que hacer anythingâ "COM lo controla todo.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="d6a0f-108">Para obtener información sobre cuál es la configuración predeterminada, vea [valores predeterminados de seguridad com](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="d6a0f-109">También puede evitar las llamadas remotas en el equipo deshabilitando DCOM por completo (COM entre equipos remotos).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="d6a0f-110">Para obtener más información, vea [establecer la seguridad de System-Wide mediante DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="d6a0f-111">En el caso de las aplicaciones heredadas o nuevas, puede establecer la seguridad de todo el proceso en el registro.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="d6a0f-112">Para obtener más información, consulte [configuración de la seguridad de Processwide a través del registro](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="d6a0f-113">También puede invalidar la configuración de seguridad predeterminada para las llamadas a determinadas interfaces en el proceso mientras establece la seguridad predeterminada para el resto del proceso (para permitir que COM controle los casos generales).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="d6a0f-114">Para obtener más información, consulte [configuración de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="d6a0f-115">En cuanto a los requisitos de seguridad complejos, puede administrar toda la seguridad mediante programación en lugar de permitir que COM lo controle.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="d6a0f-116">Para ello, llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para deshabilitar la autenticación automática y, a continuación, controle toda la configuración de seguridad mediante el establecimiento de la seguridad en una base de proxy por interfaz.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="d6a0f-117">Para obtener más información, consulte Configuración de la [seguridad de Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) y [configuración de la seguridad en el nivel de proxy de interfaz](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="d6a0f-118">En algunos escenarios, puede que desee desactivar la seguridad por completo.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="d6a0f-119">Podría decidir que la aplicación no necesita ninguna seguridad o que desee deshabilitar la seguridad durante el tiempo de desarrollo para que pueda habilitar las características de seguridad de forma individual.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="d6a0f-120">Para obtener información sobre cómo deshabilitar la seguridad de COM, consulte desactivación de la [seguridad](turning-off-security.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="d6a0f-121">La seguridad en COM se basa en los servicios de autenticación administrados por paquetes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="d6a0f-122">NTLMSSP funciona bien con muchas aplicaciones, pero no proporciona la seguridad más sólida que ofrecen otros paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="d6a0f-123">Por lo tanto, COM admite el paquete de seguridad Schannel y el protocolo de seguridad Kerberos V5.</span><span class="sxs-lookup"><span data-stu-id="d6a0f-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="d6a0f-124">Para obtener más información sobre el uso de estos paquetes de seguridad, consulte [com y paquetes de seguridad](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="d6a0f-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6a0f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6a0f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6a0f-126">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="d6a0f-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




