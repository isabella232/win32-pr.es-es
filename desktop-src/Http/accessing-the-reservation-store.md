---
title: Acceso al almacén de reserva
description: La API del servidor HTTP mantiene la lista de reserva de espacio de nombres para todos los usuarios del equipo.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Acceso al almacén de reserva HTTP
- Almacén de reserva HTTP, acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418714"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="0ebc0-105">Acceso al almacén de reserva</span><span class="sxs-lookup"><span data-stu-id="0ebc0-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="0ebc0-106">La API del servidor HTTP mantiene la lista de reserva de espacio de nombres para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="0ebc0-107">Una entrada de reserva consta de un [UrlPrefix](urlprefix-strings.md) y de la ACL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="0ebc0-108">Cada UrlPrefix del almacén tiene una ACL que enumera todos los usuarios que pueden registrarse para recibir solicitudes para el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="0ebc0-109">Los usuarios con privilegios de delegación pueden delegar subárboles del espacio de nombres que les pertenezcan a otros usuarios o eliminar reservas existentes mediante las API de configuración.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="0ebc0-110">Para agregar una reserva al almacén de reserva persistente, la aplicación llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro de identificador de configuración establecido en el valor **HttpServiceConfigUrlAclInfo** .</span><span class="sxs-lookup"><span data-stu-id="0ebc0-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="0ebc0-111">La API del servidor HTTP comprueba la propiedad del espacio de nombres y el ID. de usuario antes de agregar una reserva al almacén.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="0ebc0-112">La API del servidor HTTP también proporciona funciones para consultar y eliminar las configuraciones del servicio para espacios de nombres de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="0ebc0-113">La función [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) llamada con el parámetro de identificador de configuración establecida en las consultas de valor **HttpServiceConfigUrlAclInfo** , y la función [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) elimina en el almacén de espacios de nombres URL.</span><span class="sxs-lookup"><span data-stu-id="0ebc0-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 




