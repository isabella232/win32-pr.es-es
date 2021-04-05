---
title: Persistencia de configuración
description: Persistencia de configuración
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistencia
- SDK de Windows Media Format, persistencia de configuración
- Advanced Systems Format (ASF), persistencia
- ASF (formato de sistemas avanzados), persistencia
- Advanced Systems Format (ASF), persistencia de configuración
- ASF (formato de sistemas avanzados), persistencia de configuración
- persistencia de configuración
- persistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420319"
---
# <a name="configuration-persistence"></a><span data-ttu-id="bd05a-111">Persistencia de configuración</span><span class="sxs-lookup"><span data-stu-id="bd05a-111">Configuration Persistence</span></span>

<span data-ttu-id="bd05a-112">El SDK de Windows Media guarda ninguna de las propiedades habilitadas para escritura descritas en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="bd05a-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="bd05a-113">Cada aplicación que usa el SDK debe proporcionar sus propios procedimientos de persistencia según sea necesario e invocar el método de conjunto adecuado en cada instancia del SDK.</span><span class="sxs-lookup"><span data-stu-id="bd05a-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="bd05a-114">De esta forma, los cambios de configuración realizados por una aplicación no afectan a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd05a-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="bd05a-115">Por ejemplo, cambiar el tiempo de almacenamiento en búfer en un reproductor no afecta a otro reproductor.</span><span class="sxs-lookup"><span data-stu-id="bd05a-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="bd05a-116">La única excepción a esta regla es para la información de las credenciales.</span><span class="sxs-lookup"><span data-stu-id="bd05a-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="bd05a-117">Si la aplicación indica, en su retorno de la llamada a **AcquireCredentials** , que la información de ID. de usuario y contraseña debe persistir, el SDK guarda esta información.</span><span class="sxs-lookup"><span data-stu-id="bd05a-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd05a-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd05a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd05a-119">**Implementación de la funcionalidad de red**</span><span class="sxs-lookup"><span data-stu-id="bd05a-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="bd05a-120">**Interfaz IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="bd05a-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




