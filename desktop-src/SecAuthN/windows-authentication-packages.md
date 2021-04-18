---
description: Los paquetes de autenticación de Windows proporcionan servicios de autenticación implementando la funcionalidad específica del paquete para las funciones LsaLogonUser y LsaCallAuthenticationPackage proporcionadas por la LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Paquetes de autenticación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541150"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="7dc44-103">Paquetes de autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="7dc44-103">Windows Authentication Packages</span></span>

<span data-ttu-id="7dc44-104">Los paquetes de autenticación de Windows proporcionan servicios de autenticación implementando la funcionalidad específica del paquete para las funciones [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) y [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) proporcionadas por la LSA.</span><span class="sxs-lookup"><span data-stu-id="7dc44-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="7dc44-105">MSV1 \_ 0 es un ejemplo de un [*paquete de autenticación*](../secgloss/a-gly.md)de Windows.</span><span class="sxs-lookup"><span data-stu-id="7dc44-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="7dc44-106">El \_ paquete MSV1 0 acepta un nombre de usuario y una contraseña con [*hash*](../secgloss/h-gly.md) , que busca en la base de datos del administrador de [*cuentas de seguridad*](../secgloss/s-gly.md) (SAM).</span><span class="sxs-lookup"><span data-stu-id="7dc44-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="7dc44-107">En función de los resultados de la búsqueda, el \_ paquete de autenticación MSV1 0 acepta o rechaza el intento de autenticación.</span><span class="sxs-lookup"><span data-stu-id="7dc44-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="7dc44-108">Para obtener una lista de las funciones de soporte que LSA proporciona para que las usen los paquetes de autenticación de Windows que requieren servicios del sistema, consulte [funciones de LSA llamadas por paquetes de autenticación](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7dc44-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="7dc44-109">Los paquetes de autenticación de Windows deben implementar un conjunto de funciones a las que llama la LSA.</span><span class="sxs-lookup"><span data-stu-id="7dc44-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="7dc44-110">Para obtener la lista completa de funciones, consulte [funciones implementadas por paquetes de autenticación](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7dc44-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
