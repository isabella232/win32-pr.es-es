---
title: Convertir formatos de nombre de cuenta de dominio
description: Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan el \ 0034; el \\ formato de dominio nombre de usuario \ 0034; para las cuentas de servicio.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789604"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="410f0-103">Convertir formatos de nombre de cuenta de dominio</span><span class="sxs-lookup"><span data-stu-id="410f0-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="410f0-104">Las funciones de Microsoft Win32 para trabajar con el administrador de control de servicios (SCM) en un servidor host usan el <domain> \\ <username> formato "" para las cuentas de servicio.</span><span class="sxs-lookup"><span data-stu-id="410f0-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="410f0-105">Por ejemplo, si llama a la función [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar la cuenta de usuario en la que se ejecuta el servicio, la función devuelve el nombre en formato "fabrikam \\ juanpérez".</span><span class="sxs-lookup"><span data-stu-id="410f0-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="410f0-106">Para enlazar con la cuenta de usuario en el directorio, por ejemplo, para cambiar la contraseña de la cuenta, se requiere el nombre distintivo de la cuenta, que tiene el formato "CN = Jeff Smith, CN = users, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="410f0-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="410f0-107">Para realizar la conversión entre los distintos formatos de nombre, utilice la función [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) , que puede convertir un nombre a otros formatos, como un nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="410f0-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 