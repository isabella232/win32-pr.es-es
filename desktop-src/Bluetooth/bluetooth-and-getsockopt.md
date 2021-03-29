---
title: Bluetooth y getsockopt
description: Bluetooth usa la función getsockopt para consultar varios parámetros asociados con el canal de servidor o la conexión.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth y getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792423"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="2a4e9-106">Bluetooth y getsockopt</span><span class="sxs-lookup"><span data-stu-id="2a4e9-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="2a4e9-107">Bluetooth usa la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar varios parámetros asociados con el canal de servidor o la conexión.</span><span class="sxs-lookup"><span data-stu-id="2a4e9-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="2a4e9-108">El uso de **getsockopt** con Bluetooth tiene los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="2a4e9-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="2a4e9-109">El parámetro *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser un Socket Bluetooth válido.</span><span class="sxs-lookup"><span data-stu-id="2a4e9-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="2a4e9-110">El parámetro *LEVEL* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="2a4e9-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="2a4e9-111">Para obtener una lista de las opciones de Socket Bluetooth disponibles, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="2a4e9-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a4e9-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a4e9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a4e9-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="2a4e9-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="2a4e9-114">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="2a4e9-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 