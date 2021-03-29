---
title: Otra información de conexión
description: Los miembros de la estructura RASDIALPARAMS también pueden especificar la siguiente información de conexión.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995362"
---
# <a name="other-connection-information"></a><span data-ttu-id="956f9-103">Otra información de conexión</span><span class="sxs-lookup"><span data-stu-id="956f9-103">Other Connection Information</span></span>

<span data-ttu-id="956f9-104">Los miembros de la estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) también pueden especificar la siguiente información de conexión.</span><span class="sxs-lookup"><span data-stu-id="956f9-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="956f9-105">Un número de teléfono para invalidar el número en la entrada de la libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="956f9-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="956f9-106">Un número de teléfono de [devolución](callback-connections.md) de llamada al que el servidor remoto puede volver a llamar para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="956f9-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="956f9-107">Nombre del dominio de red remoto en el que se va a producir la autenticación.</span><span class="sxs-lookup"><span data-stu-id="956f9-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="956f9-108">En el caso del número de devolución de llamada y el dominio, los miembros de [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) pueden indicar que ras debe usar la información de la entrada de la libreta de teléfonos, o bien puede proporcionar información que invalide los datos del libro de teléfono.</span><span class="sxs-lookup"><span data-stu-id="956f9-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="956f9-109">Un cliente RAS puede usar el parámetro *lpRasDialExtensions* de la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para controlar si ras usa un prefijo o sufijo de número de teléfono especificado en una entrada de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="956f9-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 