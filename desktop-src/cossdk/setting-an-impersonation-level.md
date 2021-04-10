---
description: Cuando se establece un nivel de suplantación para una aplicación, se determina el grado de autoridad que la aplicación concede a otras aplicaciones para usar su identidad cuando las llama.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Establecer un nivel de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153194"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="8950e-103">Establecer un nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="8950e-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="8950e-104">Cuando se establece un nivel de suplantación para una aplicación, se determina el grado de autoridad que la aplicación concede a otras aplicaciones para usar su identidad cuando las llama.</span><span class="sxs-lookup"><span data-stu-id="8950e-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="8950e-105">Solo puede establecer esta opción para las aplicaciones de servidor COM+: las aplicaciones de biblioteca se ejecutan bajo la identidad del proceso de hospedaje y usan el nivel de suplantación que especifica.</span><span class="sxs-lookup"><span data-stu-id="8950e-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="8950e-106">Para obtener más información, consulte [niveles de suplantación](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="8950e-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="8950e-107">**Para seleccionar un nivel de suplantación**</span><span class="sxs-lookup"><span data-stu-id="8950e-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="8950e-108">Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la suplantación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="8950e-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="8950e-109">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="8950e-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="8950e-110">En el cuadro **nivel de suplantación** , seleccione el nivel adecuado.</span><span class="sxs-lookup"><span data-stu-id="8950e-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="8950e-111">Los niveles son los siguientes, ordenados de la concesión de la autoridad de menos a la más importante:</span><span class="sxs-lookup"><span data-stu-id="8950e-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="8950e-112">**Anónimo**.</span><span class="sxs-lookup"><span data-stu-id="8950e-112">**Anonymous**.</span></span> <span data-ttu-id="8950e-113">El cliente es anónimo para el servidor.</span><span class="sxs-lookup"><span data-stu-id="8950e-113">The client is anonymous to the server.</span></span> <span data-ttu-id="8950e-114">El servidor puede suplantar al cliente, pero el token de suplantación (una credencial local) no contiene ninguna información acerca del cliente.</span><span class="sxs-lookup"><span data-stu-id="8950e-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="8950e-115">**Identifique**.</span><span class="sxs-lookup"><span data-stu-id="8950e-115">**Identify**.</span></span> <span data-ttu-id="8950e-116">El servidor puede obtener la identidad del cliente y puede suplantar al cliente para realizar comprobaciones ACL.</span><span class="sxs-lookup"><span data-stu-id="8950e-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="8950e-117">**Suplantar**.</span><span class="sxs-lookup"><span data-stu-id="8950e-117">**Impersonate**.</span></span> <span data-ttu-id="8950e-118">El servidor puede suplantar al cliente mientras actúa en su nombre, aunque con restricciones.</span><span class="sxs-lookup"><span data-stu-id="8950e-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="8950e-119">El servidor puede obtener acceso a recursos del mismo equipo que el cliente.</span><span class="sxs-lookup"><span data-stu-id="8950e-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="8950e-120">Si el servidor está en el mismo equipo que el cliente, puede obtener acceso a los mismos recursos de red que el cliente.</span><span class="sxs-lookup"><span data-stu-id="8950e-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="8950e-121">Si el servidor se encuentra en un equipo diferente del cliente, solo podrá tener acceso a los recursos que se encuentren en el mismo equipo que el servidor.</span><span class="sxs-lookup"><span data-stu-id="8950e-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="8950e-122">Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="8950e-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="8950e-123">**Delegado**.</span><span class="sxs-lookup"><span data-stu-id="8950e-123">**Delegate**.</span></span> <span data-ttu-id="8950e-124">El servidor puede suplantar al cliente mientras actúa en su nombre, ya sea en el mismo equipo que el cliente.</span><span class="sxs-lookup"><span data-stu-id="8950e-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="8950e-125">Durante la suplantación, las credenciales del cliente (las con local y las que tienen la validez de la red) se pueden pasar a cualquier número de equipos.</span><span class="sxs-lookup"><span data-stu-id="8950e-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="8950e-126">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="8950e-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8950e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8950e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8950e-128">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="8950e-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="8950e-129">Configuración de la Directiva de restricción de software</span><span class="sxs-lookup"><span data-stu-id="8950e-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="8950e-130">Habilitar la autenticación para una aplicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="8950e-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="8950e-131">Establecer un nivel de autenticación para una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="8950e-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
