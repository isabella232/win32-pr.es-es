---
description: En el siguiente tema se describe cómo funciona la API de la plataforma de evaluación de Windows como servicio (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Acerca de la plataforma de evaluación de WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667597"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="0a3fe-103">Acerca de la plataforma de evaluación de WaaS</span><span class="sxs-lookup"><span data-stu-id="0a3fe-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="0a3fe-104">En el siguiente tema se describe cómo funciona la API de la plataforma de evaluación de Windows como servicio (WaaS).</span><span class="sxs-lookup"><span data-stu-id="0a3fe-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="0a3fe-105">La API de evaluación de WaaS ofrece al llamador la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="0a3fe-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="0a3fe-106">Si un dispositivo está en las últimas actualizaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="0a3fe-107">Si el dispositivo ha alcanzado el final del soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="0a3fe-108">Los tiempos de lanzamiento de las actualizaciones aplicables más recientes para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="0a3fe-109">Una evaluación de la razón por la que un dispositivo no está actualizado y el posible impacto que puede tener en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="0a3fe-110">La plataforma de evaluación de WaaS usa el modelo de API de COM y se ejecuta automáticamente al menos una vez al día.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="0a3fe-111">Este ciclo captura la información de la versión aplicable.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="0a3fe-112">Durante el período de almacenamiento en caché, las evaluaciones se realizan en la información de la versión almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="0a3fe-113">Si se realiza una llamada fuera de la ventana de expiración de la caché, se realiza una nueva llamada y evaluación, se almacena en caché y se devuelve.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="0a3fe-114">Cuando se realiza una llamada, el cliente de evaluación de WaaS se pone en contacto con el servicio de evaluación de WaaS con los atributos del dispositivo y recibe un expediente de información aplicable al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="0a3fe-115">Después, el cliente usa esta información en la información que recopila sobre el dispositivo para realizar la evaluación.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="0a3fe-116">El código debe tener privilegios de administrador para llamar a la API de evaluación de WAAS.</span><span class="sxs-lookup"><span data-stu-id="0a3fe-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="0a3fe-117">Para obtener más información sobre cómo desarrollar aplicaciones que requieran privilegios de administrador, consulte [este artículo](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="0a3fe-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
