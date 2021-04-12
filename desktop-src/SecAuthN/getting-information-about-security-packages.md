---
description: Cuando se inicia un cliente, selecciona un paquete de seguridad para sus transacciones con un servidor y, a continuación, se pone en contacto con ese servidor. Un servidor selecciona uno o varios paquetes de seguridad y espera una conexión de cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtención de información acerca de los paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154769"
---
# <a name="getting-information-about-security-packages"></a><span data-ttu-id="bf797-104">Obtención de información acerca de los paquetes de seguridad</span><span class="sxs-lookup"><span data-stu-id="bf797-104">Getting Information About Security Packages</span></span>

<span data-ttu-id="bf797-105">Cuando se inicia un cliente, selecciona un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) para sus transacciones con un servidor y, a continuación, se pone en contacto con ese servidor.</span><span class="sxs-lookup"><span data-stu-id="bf797-105">When a client begins, it selects a [*security package*](/windows/desktop/SecGloss/s-gly) for its transactions with a server and then contacts that server.</span></span> <span data-ttu-id="bf797-106">Un servidor selecciona uno o varios paquetes de seguridad y espera una conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="bf797-106">A server selects one or more security packages and waits for a client connection.</span></span>

<span data-ttu-id="bf797-107">Para obtener información específica sobre los paquetes de seguridad de SSPI disponibles con un SSP determinado, se puede llamar a la función [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) para recuperar una estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="bf797-107">For specific information about the SSPI security packages available with a particular SSP, the [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) function can be called to retrieve a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span>

<span data-ttu-id="bf797-108">Para recuperar la estructura de salida, el llamador pasa a la función la dirección de un puntero al tipo de la estructura devuelta.</span><span class="sxs-lookup"><span data-stu-id="bf797-108">To retrieve the output structure, the caller passes to the function the address of a pointer to the type of the return structure.</span></span> <span data-ttu-id="bf797-109">La función asigna memoria y devuelve los datos al llamador asignando la dirección del búfer de datos devueltos al argumento.</span><span class="sxs-lookup"><span data-stu-id="bf797-109">The function allocates memory and returns the data to the caller by assigning the address of the return data buffer to the argument.</span></span> <span data-ttu-id="bf797-110">La Convención SSPI es que la función asigna memoria a la estructura y la aplicación que realiza la llamada libera esa memoria mediante [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span><span class="sxs-lookup"><span data-stu-id="bf797-110">The SSPI convention is that the function allocates memory for the structure, and the calling application frees that memory using [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).</span></span>

<span data-ttu-id="bf797-111">Al llamar a la función [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) se recuperan los atributos de un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="bf797-111">Calling the [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) function retrieves the attributes of a [*security package*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="bf797-112">Tanto el servidor como el cliente pueden llamar a la función **QuerySecurityPackageInfo** para obtener la longitud máxima del token de seguridad del miembro **cbMaxToken** de la estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="bf797-112">Both server and client can call the **QuerySecurityPackageInfo** function to get the maximum length of the security token from the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="bf797-113">Para obtener un ejemplo, consulte la llamada a la función **QuerySecurityPackageInfo** que se muestra en [usar SSPI con un servidor de Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="bf797-113">For an example, see the call to the **QuerySecurityPackageInfo** function shown in [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span>

<span data-ttu-id="bf797-114">Para obtener más información sobre las funciones de paquete, vea [Administración de paquetes](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="bf797-114">For more information on package functions, see [Package Management](authentication-functions.md).</span></span>

 

 
