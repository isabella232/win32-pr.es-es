---
title: Cambios clave desde Windows 7 para garantizar la compatibilidad
description: Cambios clave desde Windows 7 para garantizar la compatibilidad
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357507"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="d9756-103">Cambios clave desde Windows 7 para garantizar la compatibilidad</span><span class="sxs-lookup"><span data-stu-id="d9756-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="d9756-104">Sabemos que la compatibilidad es importante para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="d9756-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="d9756-105">Los ISV y los desarrolladores quieren garantizar que sus aplicaciones se ejecuten según lo previsto en todas las versiones compatibles del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d9756-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="d9756-106">Este aspecto es clave para la inversión de los consumidores y las empresas: desean saber con seguridad que las aplicaciones por las que han pagado continuarán funcionando.</span><span class="sxs-lookup"><span data-stu-id="d9756-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="d9756-107">Sabemos que la compatibilidad es el criterio principal para la toma de decisiones de compra.</span><span class="sxs-lookup"><span data-stu-id="d9756-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="d9756-108">Las aplicaciones que se escriben correctamente en función de los procedimientos recomendados darán lugar a una renovación de código mucho menor cuando se lance una nueva versión de Windows y reducirán la fragmentación: estas aplicaciones tienen una inversión de ingeniería reducida para mantener y un tiempo de comercialización más rápido.</span><span class="sxs-lookup"><span data-stu-id="d9756-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="d9756-109">En el marco de Windows 7, el enfoque hacia la compatibilidad era mucho más reactivo.</span><span class="sxs-lookup"><span data-stu-id="d9756-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="d9756-110">En Windows 8 comenzamos a variar nuestra perspectiva respecto a este tema y trabajamos en el interior de Windows para garantizar que la compatibilidad fuera una cuestión que se incluyera ya en la fase de diseño y que no fuese una idea posterior.</span><span class="sxs-lookup"><span data-stu-id="d9756-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="d9756-111">Windows 10 es la versión del sistema operativo más compatible por diseño hasta la fecha.</span><span class="sxs-lookup"><span data-stu-id="d9756-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="d9756-112">A continuación se muestran algunas de los aspectos clave gracias a los que lo hemos conseguido:</span><span class="sxs-lookup"><span data-stu-id="d9756-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="d9756-113">Telemetría de la aplicación: esto nos ayuda a comprender la popularidad de las aplicaciones en el ecosistema de Windows para informar sobre las pruebas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d9756-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="d9756-114">Asociaciones de ISV: trabaje directamente con asociados externos para proporcionarles datos y ayudar a solucionar los problemas que experimenten nuestros usuarios.</span><span class="sxs-lookup"><span data-stu-id="d9756-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="d9756-115">Revisiones de diseño, detección ascendente: asociado con equipos de características para reducir el número de cambios importantes en Windows.</span><span class="sxs-lookup"><span data-stu-id="d9756-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="d9756-116">La revisión de la compatibilidad es una prueba que nuestros equipos de características deben superar.</span><span class="sxs-lookup"><span data-stu-id="d9756-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="d9756-117">Mayor control sobre los cambios de la API & la comunicación mejorada</span><span class="sxs-lookup"><span data-stu-id="d9756-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="d9756-118">Bucle de vuelos y comentarios: el rellenado de Windows Insider recibe compilaciones piloto que ayudan a mejorar nuestra capacidad de encontrar problemas de compatibilidad antes de que se lance una compilación final a los clientes.</span><span class="sxs-lookup"><span data-stu-id="d9756-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="d9756-119">Este proceso de comentarios no solo expone errores, sino que también garantiza que publicamos características que nuestros usuarios desean.</span><span class="sxs-lookup"><span data-stu-id="d9756-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




