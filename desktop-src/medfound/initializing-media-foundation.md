---
description: Inicializar Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializar Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678647"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="42d73-103">Inicializar Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42d73-103">Initializing Media Foundation</span></span>

<span data-ttu-id="42d73-104">Antes de usar cualquier objeto o interfaz de Microsoft Media Foundation, debe llamar a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="42d73-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="42d73-105">Pase la **\_ versión** de la constante MF.</span><span class="sxs-lookup"><span data-stu-id="42d73-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="42d73-106">La función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inicializa la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="42d73-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="42d73-107">Si **MFStartup** devuelve la \_ \_ \_ versión de inicio incorrecta MF E \_ , significa que la aplicación se compiló con una versión de los media Foundation encabezados que no coinciden con los media Foundation dll del sistema.</span><span class="sxs-lookup"><span data-stu-id="42d73-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="42d73-108">Para cada llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), la aplicación debe llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="42d73-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="42d73-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42d73-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d73-110">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42d73-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="42d73-111">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="42d73-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



