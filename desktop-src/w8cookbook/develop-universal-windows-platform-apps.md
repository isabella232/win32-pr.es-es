---
title: Desarrollo de aplicaciones Plataforma universal de Windows (UWP)
description: Desarrollo de aplicaciones Plataforma universal de Windows (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105714339"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="40793-103">Desarrollo de aplicaciones Plataforma universal de Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="40793-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="40793-104">Se recomienda que todos los ISV de aplicaciones de escritorio (Win32) lleven las aplicaciones de escritorio al [plataforma universal de Windows (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) a través del puente de escritorio.</span><span class="sxs-lookup"><span data-stu-id="40793-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="40793-105">Las aplicaciones para UWP también se admiten en la [Tienda Windows](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), por lo que es más fácil actualizar automáticamente a los usuarios a una versión coherente, y esto reduce los costes de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="40793-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="40793-106">Si las aplicaciones de escritorio no se pueden convertir mediante el puente de escritorio, le recomendamos encarecidamente que use un instalador que siga los procedimientos recomendados y que esté totalmente probado.</span><span class="sxs-lookup"><span data-stu-id="40793-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="40793-107">Un instalador es la primera experiencia del usuario o del cliente con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40793-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="40793-108">Con demasiada frecuencia, el instalador no funciona correctamente o no se ha probado de forma completa en todos los escenarios.</span><span class="sxs-lookup"><span data-stu-id="40793-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="40793-109">El [Kit de certificación de aplicaciones de Windows](https://dev.windows.com/develop/app-certification-kit) puede ayudarle a probar la instalación y desinstalación de la aplicación Win32 y a identificar el uso de API no documentadas, así como otros problemas básicos relacionados con el rendimiento, antes de que los usuarios lo hagan.</span><span class="sxs-lookup"><span data-stu-id="40793-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="40793-110">Procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="40793-110">Best practices:</span></span>

-   <span data-ttu-id="40793-111">Usa instaladores que funcionen para versiones de Windows de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="40793-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="40793-112">Diseña tus instaladores para que funcionen en varios escenarios (en el nivel de usuario o de equipo).</span><span class="sxs-lookup"><span data-stu-id="40793-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="40793-113">Mantén todos los redistribuibles de Windows en el paquete original; si cambias el paquete, es posible que el instalador no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="40793-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="40793-114">Programa el tiempo de desarrollo para tus instaladores, que a menudo se omiten como un entregable durante el ciclo de vida de desarrollo de software.</span><span class="sxs-lookup"><span data-stu-id="40793-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




