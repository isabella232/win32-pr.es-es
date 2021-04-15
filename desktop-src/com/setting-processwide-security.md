---
title: Configuración de la seguridad de Process-Wide
description: Hay varias maneras de establecer la seguridad de todo el proceso.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714269"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="c6187-103">Configuración de la seguridad de Process-Wide</span><span class="sxs-lookup"><span data-stu-id="c6187-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="c6187-104">Hay varias maneras de establecer la seguridad de todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="c6187-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="c6187-105">La primera forma de usar la herramienta Dcomcnfg.exe es que es más fácil porque no requiere programación.</span><span class="sxs-lookup"><span data-stu-id="c6187-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="c6187-106">La segunda técnica ofrece al programador más control y requiere una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c6187-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="c6187-107">Otra técnica consiste en establecer la seguridad de todo el proceso en el registro mediante el uso de la clave [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="c6187-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="c6187-108">Para obtener más información sobre estas técnicas, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6187-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="c6187-109">Establecer la seguridad de Process-Wide mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="c6187-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="c6187-110">Configuración de la seguridad de Process-Wide con CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="c6187-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="c6187-111">Establecer la seguridad de Process-Wide a través del registro</span><span class="sxs-lookup"><span data-stu-id="c6187-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="c6187-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6187-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6187-113">Establecimiento de la seguridad en el nivel de proxy de interfaz</span><span class="sxs-lookup"><span data-stu-id="c6187-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="c6187-114">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="c6187-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




