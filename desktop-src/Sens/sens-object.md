---
description: El servicio de notificación de eventos del sistema (SENS) define la coclase SENS como parte de la biblioteca de tipos SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: SENS (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668305"
---
# <a name="sens-object"></a><span data-ttu-id="b2e69-103">SENS (objeto)</span><span class="sxs-lookup"><span data-stu-id="b2e69-103">SENS Object</span></span>

<span data-ttu-id="b2e69-104">El servicio de notificación de eventos del sistema (SENS) define la coclase SENS como parte de la biblioteca de tipos SENS.</span><span class="sxs-lookup"><span data-stu-id="b2e69-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="b2e69-105">Implementación</span><span class="sxs-lookup"><span data-stu-id="b2e69-105">Implementation</span></span>

<span data-ttu-id="b2e69-106">El sistema operativo proporciona la implementación del objeto SENS.</span><span class="sxs-lookup"><span data-stu-id="b2e69-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="b2e69-107">Funciones de creación/acceso</span><span class="sxs-lookup"><span data-stu-id="b2e69-107">Creation/Access Functions</span></span>



| <span data-ttu-id="b2e69-108">Función</span><span class="sxs-lookup"><span data-stu-id="b2e69-108">Function</span></span>                                      | <span data-ttu-id="b2e69-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2e69-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="b2e69-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b2e69-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="b2e69-111">Crea una instancia del objeto SENS utilizando su CLSID.</span><span class="sxs-lookup"><span data-stu-id="b2e69-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="b2e69-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b2e69-112">Interfaces</span></span>



| <span data-ttu-id="b2e69-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b2e69-113">Interface</span></span>                            | <span data-ttu-id="b2e69-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2e69-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e69-115">**IsensNetwork**</span><span class="sxs-lookup"><span data-stu-id="b2e69-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="b2e69-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b2e69-116">Default.</span></span> <span data-ttu-id="b2e69-117">Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b2e69-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="b2e69-118">**IsensOnNow**</span><span class="sxs-lookup"><span data-stu-id="b2e69-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="b2e69-119">Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b2e69-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="b2e69-120">**IsensLogon**</span><span class="sxs-lookup"><span data-stu-id="b2e69-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="b2e69-121">Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b2e69-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="b2e69-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="b2e69-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="b2e69-123">Interfaz de salida implementada por el objeto receptor en la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b2e69-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="b2e69-124">Disponible con Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2e69-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b2e69-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e69-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e69-126">**ISensLogon**</span><span class="sxs-lookup"><span data-stu-id="b2e69-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="b2e69-127">**ISensNetwork**</span><span class="sxs-lookup"><span data-stu-id="b2e69-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="b2e69-128">**ISensOnNow**</span><span class="sxs-lookup"><span data-stu-id="b2e69-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="b2e69-129">Acerca del servicio de notificación de eventos del sistema</span><span class="sxs-lookup"><span data-stu-id="b2e69-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
