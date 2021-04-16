---
title: Modificación de los valores predeterminados de seguridad de un equipo
description: Modificación de los valores predeterminados de seguridad de un equipo
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418343"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="23781-103">Modificación de los valores predeterminados de seguridad de un equipo</span><span class="sxs-lookup"><span data-stu-id="23781-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="23781-104">No se recomienda cambiar la configuración de seguridad de todo el sistema, ya que esto afectará a todas las aplicaciones de servidor COM que no establezcan su propia seguridad en todo el proceso y podrían impedir que funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="23781-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="23781-105">Si va a cambiar la configuración de seguridad de todo el sistema para que afecte a la configuración de seguridad de una aplicación COM determinada, debe cambiar la configuración de seguridad de todo el proceso para esa aplicación COM en particular.</span><span class="sxs-lookup"><span data-stu-id="23781-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="23781-106">Para obtener más información acerca de cómo establecer la seguridad de todo el proceso, consulte Configuración de la [seguridad de Process-Wide](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="23781-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="23781-107">Algunos valores del registro determinan la configuración de seguridad de las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="23781-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="23781-108">Puede modificar esta configuración mediante Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="23781-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="23781-109">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="23781-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="23781-110">Valores del registro para la seguridad de System-Wide</span><span class="sxs-lookup"><span data-stu-id="23781-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="23781-111">Establecer la seguridad de System-Wide mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="23781-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="23781-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23781-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23781-113">Establecer la seguridad de todo el proceso</span><span class="sxs-lookup"><span data-stu-id="23781-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="23781-114">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="23781-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




