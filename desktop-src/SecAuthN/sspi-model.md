---
description: La interfaz del proveedor de compatibilidad para seguridad (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o una red sin cambiar la interfaz al sistema de seguridad.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423620"
---
# <a name="sspi-model"></a><span data-ttu-id="03cee-103">Modelo SSPI</span><span class="sxs-lookup"><span data-stu-id="03cee-103">SSPI Model</span></span>

<span data-ttu-id="03cee-104">La [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o una red sin cambiar la interfaz al sistema de seguridad.</span><span class="sxs-lookup"><span data-stu-id="03cee-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="03cee-105">SSPI no establece [*las credenciales*](../secgloss/c-gly.md) de inicio de sesión porque normalmente es una operación privilegiada administrada por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03cee-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="03cee-106">Un [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) se incluye en una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll) que implementa SSPI al hacer que uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md) estén disponibles para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="03cee-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="03cee-107">Cada paquete de seguridad proporciona asignaciones entre las llamadas a funciones SSPI de una aplicación y las funciones de un modelo de seguridad real.</span><span class="sxs-lookup"><span data-stu-id="03cee-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="03cee-108">Los paquetes de seguridad admiten [*protocolos de seguridad*](../secgloss/s-gly.md) , como la autenticación [*Kerberos*](../secgloss/k-gly.md) y LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="03cee-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="03cee-109">La interfaz SSPI está disponible en modo kernel y en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="03cee-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="03cee-110">Para usar la funcionalidad SSPI en modo kernel, debe instalar el DDK del sistema de archivos instalables de Windows.</span><span class="sxs-lookup"><span data-stu-id="03cee-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="03cee-111">El modelo de llamada sigue siendo el mismo, pero las consideraciones sobre el modo kernel se indican en las páginas de referencia de la función.</span><span class="sxs-lookup"><span data-stu-id="03cee-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="03cee-112">Para obtener más información, vea [funciones de SSPI](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="03cee-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
