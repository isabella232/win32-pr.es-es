---
description: Habilitar la autenticación para una aplicación de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitar la autenticación para una aplicación de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686448"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="a5eac-103">Habilitar la autenticación para una aplicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5eac-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="a5eac-104">Dado que las aplicaciones de biblioteca COM+ están hospedadas en otros procesos, sus requisitos de seguridad pueden ser diferentes de los de las aplicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="a5eac-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="a5eac-105">Si el explorador va a hospedar la aplicación de biblioteca, es posible que tenga que recibir devoluciones de llamada no autenticadas.</span><span class="sxs-lookup"><span data-stu-id="a5eac-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="a5eac-106">Para satisfacer esta necesidad, puede deshabilitar la autenticación para que el proceso de hospedaje no realice comprobaciones de seguridad para los llamadores de la aplicación de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a5eac-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="a5eac-107">Al deshabilitar la autenticación, las llamadas a la aplicación de biblioteca se desconectan de forma eficaz; todas las llamadas a ella se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5eac-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="a5eac-108">Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="a5eac-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="a5eac-109">**Para habilitar (o deshabilitar) la autenticación para una aplicación de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="a5eac-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="a5eac-110">Haga clic con el botón secundario en la aplicación COM+ para la que va a habilitar o deshabilitar la autenticación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="a5eac-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="a5eac-111">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="a5eac-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="a5eac-112">En **autenticación**, active la casilla **Habilitar autenticación** para habilitar la autenticación; Si desactiva la casilla, se deshabilitará la autenticación.</span><span class="sxs-lookup"><span data-stu-id="a5eac-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="a5eac-113">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5eac-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5eac-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5eac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5eac-115">Establecer un nivel de autenticación para una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="a5eac-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



