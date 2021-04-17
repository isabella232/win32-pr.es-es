---
description: Autenticación mediante tarjeta inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticación mediante tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652937"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="e51b5-103">Autenticación mediante tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e51b5-103">Smart Card Authentication</span></span>

<span data-ttu-id="e51b5-104">Las partes básicas del [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) se basan en los estándares PC/SC (consulte las especificaciones en [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ).</span><span class="sxs-lookup"><span data-stu-id="e51b5-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="e51b5-105">Estas partes básicas incluyen:</span><span class="sxs-lookup"><span data-stu-id="e51b5-105">These basic parts include:</span></span>

-   <span data-ttu-id="e51b5-106">Un [*Administrador de recursos*](../secgloss/r-gly.md) que usa una API de Windows.</span><span class="sxs-lookup"><span data-stu-id="e51b5-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="e51b5-107">Una [*interfaz de usuario*](../secgloss/u-gly.md) (IU) que funciona con el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b5-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="e51b5-108">Varios [*proveedores de servicios*](../secgloss/s-gly.md) base que proporcionan acceso a servicios específicos.</span><span class="sxs-lookup"><span data-stu-id="e51b5-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="e51b5-109">A diferencia de la API de Windows de Resource Manager, los proveedores de servicios usan un modelo de interfaz COM para proporcionar servicios de [*tarjetas inteligentes*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e51b5-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="e51b5-110">En la ilustración siguiente se muestran las relaciones de estos elementos en la arquitectura general de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e51b5-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![arquitectura de tarjeta inteligente](images/smartovr2a.png)

<span data-ttu-id="e51b5-112">Para obtener información acerca de cómo funciona el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) con otros servicios disponibles en Microsoft Internet Security Framework, consulte [relación con otros servicios](relation-to-other-services.md).</span><span class="sxs-lookup"><span data-stu-id="e51b5-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="e51b5-113">Para obtener información acerca de la autenticación mediante tarjeta inteligente, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e51b5-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="e51b5-114">Temas</span><span class="sxs-lookup"><span data-stu-id="e51b5-114">Topics</span></span>                                                                      | <span data-ttu-id="e51b5-115">Contenido</span><span class="sxs-lookup"><span data-stu-id="e51b5-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e51b5-116">Conceptos de tarjetas inteligentes</span><span class="sxs-lookup"><span data-stu-id="e51b5-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="e51b5-117">Conceptos básicos y descripción de la interacción entre los usuarios y las tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e51b5-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="e51b5-118">Administrador de recursos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e51b5-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="e51b5-119">Información acerca de la API de Resource Manager, que administra el acceso a los [*lectores*](../secgloss/r-gly.md) y a las [*tarjetas inteligentes*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e51b5-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="e51b5-120">Interfaz de usuario de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e51b5-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="e51b5-121">Información sobre el [*cuadro de diálogo común de tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e51b5-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="e51b5-122">Proveedores de servicios de tarjetas inteligentes</span><span class="sxs-lookup"><span data-stu-id="e51b5-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="e51b5-123">Información acerca de las interfaces, los comandos y los contenedores que proporcionan capacidades de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e51b5-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="e51b5-124">Además, los desarrollos actuales de tarjetas inteligentes de Microsoft se pueden encontrar en [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="e51b5-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
