---
description: Una aplicación habilitada para tinta se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Arquitectura de la API de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568243"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="5c9ee-103">Arquitectura de la API de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="5c9ee-103">Recognition API Architecture</span></span>

<span data-ttu-id="5c9ee-104">Una aplicación habilitada para tinta se comunica con el sistema de reconocimiento a través de las API de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="5c9ee-105">Las aplicaciones utilizan el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para lograr esto.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="5c9ee-106">La plataforma de Tablet PC interactúa con el reconocedor mediante el uso de las interfaces de estilo C que se documentan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="5c9ee-107">En la ilustración siguiente, el área dentro de la línea discontinua muestra lo que se documenta en esta sección.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![Ilustración de la arquitectura de reconocimiento con el reconocedor resaltado](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="5c9ee-109">Un reconocedor personalizado debe incluir recapitulais. h (se instala de forma predeterminada en C: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ include).</span><span class="sxs-lookup"><span data-stu-id="5c9ee-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="5c9ee-110">Excepto en los casos en los que se indique, la biblioteca de vínculos dinámicos (DLL) debe exportar todas las funciones de la API, incluso si elige que algunos devuelvan E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="5c9ee-111">En ningún caso, el reconocedor será llamado directamente por una aplicación habilitada para tinta.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="5c9ee-112">En su lugar, las aplicaciones llamarán a las API de automatización o a las API administradas para obtener los resultados del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="5c9ee-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



