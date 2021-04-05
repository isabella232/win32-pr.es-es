---
description: Configurar aplicaciones de biblioteca
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurar aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080147"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="ae5dd-103">Configurar aplicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae5dd-103">Configuring Library Applications</span></span>

<span data-ttu-id="ae5dd-104">Dado que las aplicaciones de biblioteca COM+ se ejecutan en el proceso del cliente, los elementos configurables para las aplicaciones de biblioteca son considerablemente diferentes a los de las aplicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="ae5dd-105">No se puede configurar ningún aspecto de la aplicación que esté determinado por el proceso de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="ae5dd-106">En el nivel de aplicación, varias configuraciones están limitadas o no están disponibles para las aplicaciones de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="ae5dd-107">Estas restricciones se describen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="ae5dd-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="ae5dd-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="ae5dd-108">Attribute</span></span>                                       | <span data-ttu-id="ae5dd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae5dd-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5dd-110">Nivel de seguridad</span><span class="sxs-lookup"><span data-stu-id="ae5dd-110">Security level</span></span><br/>                       | <span data-ttu-id="ae5dd-111">Debe elegir comprobaciones de acceso de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-111">You must choose component-level access checks.</span></span> <span data-ttu-id="ae5dd-112">La aplicación de biblioteca no puede influir en las comprobaciones de acceso de nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="ae5dd-113">Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ae5dd-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="ae5dd-114">Habilitación o deshabilitación de la autenticación</span><span class="sxs-lookup"><span data-stu-id="ae5dd-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="ae5dd-115">Puede indicar si la aplicación de biblioteca participará en la autenticación realizada por el proceso de host.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="ae5dd-116">Consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="ae5dd-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="ae5dd-117">Nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="ae5dd-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="ae5dd-118">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-118">Unavailable.</span></span> <span data-ttu-id="ae5dd-119">Se usa la configuración del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="ae5dd-120">Identidad de seguridad</span><span class="sxs-lookup"><span data-stu-id="ae5dd-120">Security identity</span></span><br/>                    | <span data-ttu-id="ae5dd-121">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-121">Unavailable.</span></span> <span data-ttu-id="ae5dd-122">La aplicación se ejecuta bajo la identidad del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="ae5dd-123">Cierre de proceso de servidor</span><span class="sxs-lookup"><span data-stu-id="ae5dd-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="ae5dd-124">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="ae5dd-125">Habilitar compatibilidad con 3 GB</span><span class="sxs-lookup"><span data-stu-id="ae5dd-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="ae5dd-126">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="ae5dd-127">Iniciar en el depurador</span><span class="sxs-lookup"><span data-stu-id="ae5dd-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="ae5dd-128">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="ae5dd-129">Habilitar CRM</span><span class="sxs-lookup"><span data-stu-id="ae5dd-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="ae5dd-130">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="ae5dd-131">MSMQ</span><span class="sxs-lookup"><span data-stu-id="ae5dd-131">Queuing</span></span><br/>                              | <span data-ttu-id="ae5dd-132">Dispone.</span><span class="sxs-lookup"><span data-stu-id="ae5dd-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ae5dd-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae5dd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5dd-134">Información general de la aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="ae5dd-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




