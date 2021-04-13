---
title: Bluetooth y-i
description: Bluetooth usa la función de la función-to para establecer diversos parámetros asociados con el canal de servidor o la conexión.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth y-i
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359043"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="9e74e-106">Bluetooth y-i</span><span class="sxs-lookup"><span data-stu-id="9e74e-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="9e74e-107">Bluetooth usa la [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función-to para establecer diversos parámetros asociados con el canal de servidor o la conexión.</span><span class="sxs-lookup"><span data-stu-id="9e74e-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="9e74e-108">El uso **de las opciones de la** con Bluetooth tiene los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="9e74e-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="9e74e-109">El parámetro *s* de [**r**](/windows/desktop/api/winsock/nf-winsock-setsockopt) debe ser un Socket Bluetooth válido.</span><span class="sxs-lookup"><span data-stu-id="9e74e-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="9e74e-110">El parámetro *LEVEL* de [**la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de-to debe ser sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="9e74e-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="9e74e-111">Para obtener una lista de las opciones de Socket Bluetooth disponibles, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="9e74e-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e74e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e74e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e74e-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9e74e-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="9e74e-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="9e74e-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 