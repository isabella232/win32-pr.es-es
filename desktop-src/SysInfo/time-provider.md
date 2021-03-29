---
description: El sistema operativo Microsoft Windows proporciona compatibilidad con una variedad de dispositivos de hardware y protocolos de tiempo de red que usan la arquitectura de proveedor de hora.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911998"
---
# <a name="time-provider"></a><span data-ttu-id="3dd33-103">Proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="3dd33-103">Time Provider</span></span>

<span data-ttu-id="3dd33-104">El sistema operativo Microsoft Windows proporciona compatibilidad con una variedad de dispositivos de hardware y protocolos de tiempo de red que usan la arquitectura de *proveedor de hora* .</span><span class="sxs-lookup"><span data-stu-id="3dd33-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="3dd33-105">Los proveedores de hora de entrada recuperan las marcas de tiempo precisas del hardware o la red, y los proveedores de tiempo de salida proporcionan marcas de tiempo a otros clientes de la red.</span><span class="sxs-lookup"><span data-stu-id="3dd33-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="3dd33-106">Los proveedores de hora se administran mediante el *Administrador de proveedores de hora*.</span><span class="sxs-lookup"><span data-stu-id="3dd33-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="3dd33-107">Es responsable de cargar, iniciar y detener los proveedores de hora según lo indicado por el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="3dd33-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="3dd33-108">Esta interfaz facilita la escritura de un proveedor de hora que escribir un servicio completo.</span><span class="sxs-lookup"><span data-stu-id="3dd33-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="3dd33-109">Creación de un proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="3dd33-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="3dd33-110">Registrar un proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="3dd33-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="3dd33-111">Proveedor de tiempo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3dd33-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="3dd33-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dd33-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd33-113">Servicio de hora de Windows</span><span class="sxs-lookup"><span data-stu-id="3dd33-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



