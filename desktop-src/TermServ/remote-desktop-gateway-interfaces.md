---
title: Interfaces de puerta de enlace de Escritorio remoto
description: La API de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) admite las siguientes interfaces. Puede utilizar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993957"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="a55c5-104">Interfaces de puerta de enlace de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a55c5-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="a55c5-105">La API de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="a55c5-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="a55c5-106">Puede utilizar estas interfaces para implementar complementos que proporcionan autenticación y autorización personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a55c5-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="a55c5-107">No hay ninguna dependencia entre el complemento de autenticación y el complemento de autorización, y solo puede implementar un complemento si lo desea.</span><span class="sxs-lookup"><span data-stu-id="a55c5-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="a55c5-108">Los complementos de autenticación son [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) y [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="a55c5-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="a55c5-109">Los complementos de autorización son [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)y [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="a55c5-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a55c5-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a55c5-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a55c5-111">**ITSGAccountingEngine**</span><span class="sxs-lookup"><span data-stu-id="a55c5-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="a55c5-112">Expone métodos que proporcionan información sobre la creación o el cierre de sesiones para una conexión.</span><span class="sxs-lookup"><span data-stu-id="a55c5-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="a55c5-113">**ITSGAuthenticateUserSink**</span><span class="sxs-lookup"><span data-stu-id="a55c5-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="a55c5-114">Expone métodos que notifican a la puerta de enlace de escritorio remoto sobre eventos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a55c5-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="a55c5-115">**ITSGAuthenticationEngine**</span><span class="sxs-lookup"><span data-stu-id="a55c5-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="a55c5-116">Expone métodos que autentican a los usuarios para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a55c5-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="a55c5-117">**ITSGAuthorizeConnectionSink**</span><span class="sxs-lookup"><span data-stu-id="a55c5-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="a55c5-118">Expone métodos que envían una notificación a la puerta de enlace de escritorio remoto sobre el resultado de un intento de autorizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="a55c5-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="a55c5-119">**ITSGAuthorizeResourceSink**</span><span class="sxs-lookup"><span data-stu-id="a55c5-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="a55c5-120">Expone métodos que envían una notificación a la puerta de enlace de escritorio remoto sobre el resultado de un intento de autorizar un recurso.</span><span class="sxs-lookup"><span data-stu-id="a55c5-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="a55c5-121">**ITSGPolicyEngine**</span><span class="sxs-lookup"><span data-stu-id="a55c5-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="a55c5-122">Expone métodos que autorizan conexiones y recursos.</span><span class="sxs-lookup"><span data-stu-id="a55c5-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




