---
description: Enumera y explica los pasos necesarios para inicializar un paquete de seguridad.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inicializar el paquete de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156028"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="7392e-103">Inicializar el paquete de seguridad</span><span class="sxs-lookup"><span data-stu-id="7392e-103">Initializing the Security Package</span></span>

<span data-ttu-id="7392e-104">Estos pasos son necesarios antes de usar SSPI:</span><span class="sxs-lookup"><span data-stu-id="7392e-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="7392e-105">Se debe llamar a la función de inicialización para obtener la dirección de la tabla de funciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7392e-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="7392e-106">El cliente y el servidor llaman a [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) para un puntero a una tabla de distribución [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) .</span><span class="sxs-lookup"><span data-stu-id="7392e-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="7392e-107">Esta tabla contiene punteros a las funciones de devolución de llamada declaradas en SSPI. h.</span><span class="sxs-lookup"><span data-stu-id="7392e-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="7392e-108">Estos punteros proporcionan acceso a las implementaciones del archivo DLL de las diversas funciones SSPI.</span><span class="sxs-lookup"><span data-stu-id="7392e-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="7392e-109">Debe obtener información acerca de los paquetes de seguridad admitidos.</span><span class="sxs-lookup"><span data-stu-id="7392e-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="7392e-110">Aunque la mayoría de las aplicaciones usan paquetes de seguridad que admiten funcionalidades predeterminadas o comunes, los paquetes de seguridad pueden tener capacidades únicas de interés para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7392e-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="7392e-111">Una aplicación que necesita funcionalidades especiales puede usar un paquete que ofrezca esas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="7392e-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="7392e-112">Para obtener más información, consulte [obtener información acerca de los paquetes de seguridad](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="7392e-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="7392e-113">En este punto, la aplicación ha inicializado correctamente un SSP y ha elegido un paquete de seguridad con las capacidades suficientes.</span><span class="sxs-lookup"><span data-stu-id="7392e-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="7392e-114">Se puede usar el paquete [*Negotiate*](../secgloss/n-gly.md) si el acuerdo entre el cliente y el servidor sobre qué [*paquete de seguridad*](../secgloss/s-gly.md) se va a usar se realiza en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7392e-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="7392e-115">Si no se utiliza el paquete Negotiate, el cliente y el servidor deben estar de acuerdo en el paquete de seguridad específico que se utilizará antes de realizar los pasos de configuración anteriores.</span><span class="sxs-lookup"><span data-stu-id="7392e-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
