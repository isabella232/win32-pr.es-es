---
description: El archivo de encabezado Winternl. h expone prototipos de API de Windows internas. No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Llamar a API internas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998254"
---
# <a name="calling-internal-apis"></a><span data-ttu-id="55aee-104">Llamar a API internas</span><span class="sxs-lookup"><span data-stu-id="55aee-104">Calling Internal APIs</span></span>

<span data-ttu-id="55aee-105">El archivo de encabezado Winternl. h expone prototipos de API de Windows internas.</span><span class="sxs-lookup"><span data-stu-id="55aee-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="55aee-106">No hay ninguna biblioteca de importación asociada, por lo que los desarrolladores deben usar la vinculación dinámica en tiempo de ejecución para llamar a las funciones descritas en este archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="55aee-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="55aee-107">Las funciones y estructuras de Winternl. h son internas del sistema operativo y están sujetas a cambios de una versión de Windows a la siguiente y, posiblemente, incluso entre los Service Pack de cada versión.</span><span class="sxs-lookup"><span data-stu-id="55aee-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="55aee-108">Para mantener la compatibilidad de la aplicación, debe usar en su lugar las funciones públicas equivalentes.</span><span class="sxs-lookup"><span data-stu-id="55aee-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="55aee-109">Hay más información disponible en el archivo de encabezado, Winternl. h, y en la documentación de cada función.</span><span class="sxs-lookup"><span data-stu-id="55aee-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="55aee-110">Si usa estas funciones, puede tener acceso a ellas a través de la vinculación dinámica en tiempo de ejecución mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="55aee-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="55aee-111">Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="55aee-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="55aee-112">Sin embargo, es posible que los cambios en la firma no se puedan detectar.</span><span class="sxs-lookup"><span data-stu-id="55aee-112">Signature changes, however, may not be detectable.</span></span>

 

 
