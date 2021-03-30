---
description: El objeto CallHub representa una vista de terceros de una llamada entre partes.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objeto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002320"
---
# <a name="callhub-object"></a><span data-ttu-id="9e6e5-103">Objeto CallHub</span><span class="sxs-lookup"><span data-stu-id="9e6e5-103">CallHub Object</span></span>

<span data-ttu-id="9e6e5-104">El objeto CallHub representa una vista de terceros de una llamada entre partes.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="9e6e5-105">Las interfaces y los métodos asociados obtienen y establecen información relacionada con el concentrador, como, por ejemplo, si está activo.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="9e6e5-106">Con el objeto CallHub, un usuario con la seguridad necesaria puede detectar y potencialmente controlar a otros participantes en una llamada.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="9e6e5-107">Una aplicación no puede crear directamente un objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="9e6e5-108">Un objeto CallHub se crea indirectamente cuando se recibe una llamada entrante a través de TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="9e6e5-109">TAPI 3 se basa en los proveedores de servicios TAPI para proporcionar la información necesaria sobre las llamadas para implementar mediante el objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="9e6e5-110">Dado que no todos los proveedores de servicios proporcionan esta información y no todo el hardware admite el seguimiento del centro de llamadas, la información disponible sobre los demás usuarios de la conexión puede ser limitada o inexistente.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="9e6e5-111">En el ejemplo de creación de un código de [Conferencia simple](create-a-simple-conference.md) se muestra el uso de un objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="9e6e5-112">Vea [interfaces del objeto CallHub](callhub-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto CallHub.</span><span class="sxs-lookup"><span data-stu-id="9e6e5-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



