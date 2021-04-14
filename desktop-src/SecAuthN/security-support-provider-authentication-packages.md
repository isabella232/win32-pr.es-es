---
description: El sistema operativo Windows admite la autenticación mediante paquetes de seguridad que funcionan como proveedores de compatibilidad de seguridad y como paquetes de autenticación.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Paquetes de autenticación/proveedor de compatibilidad de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648367"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="bbb6d-103">Paquetes de autenticación/proveedor de compatibilidad de seguridad</span><span class="sxs-lookup"><span data-stu-id="bbb6d-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="bbb6d-104">El sistema operativo Windows admite la autenticación mediante [*paquetes de seguridad*](../secgloss/s-gly.md) que funcionan como proveedores de compatibilidad de [*seguridad*](../secgloss/s-gly.md) y como paquetes de [*autenticación*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="bbb6d-105">Los paquetes de seguridad proporcionan los servicios de soporte del proceso de inicio de sesión de un paquete de autenticación de Windows y también proporcionan servicios de autenticación a las aplicaciones implementando un conjunto de funciones que se asignan a la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="bbb6d-106">Un paquete de seguridad que funciona como un paquete de autenticación e implementa la funcionalidad requerida por [*SSPI*](../secgloss/s-gly.md) se denomina proveedor de compatibilidad para seguridad/paquete de autenticación (SSP/AP).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="bbb6d-107">Para obtener más información acerca de los paquetes de seguridad, consulte [paquetes SSP proporcionados por Microsoft](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="bbb6d-108">Para obtener información sobre el desarrollo de SSP o AP personalizados, consulte [paquetes de seguridad personalizados](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
