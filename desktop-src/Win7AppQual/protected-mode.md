---
description: Modo protegido
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116453"
---
# <a name="protected-mode"></a><span data-ttu-id="59c79-103">Modo protegido</span><span class="sxs-lookup"><span data-stu-id="59c79-103">Protected Mode</span></span>

<span data-ttu-id="59c79-104">La mayoría de las características de seguridad de Windows Internet Explorer 8 están disponibles en Internet Explorer 8 para Windows XP con el sistema operativo Service Pack 2 (SP2) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="59c79-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="59c79-105">El modo protegido solo está disponible para Windows Vista o versiones posteriores porque se basa en las siguientes características de seguridad que son nuevas en Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="59c79-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="59c79-106">[El control de cuentas de usuario (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilita la ejecución sin privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="59c79-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="59c79-107">Cuando los usuarios ejecutan programas con privilegios de usuario limitados, son más seguros de un ataque que cuando se ejecutan con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="59c79-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="59c79-108">El sistema operativo Windows puede impedir que el código malintencionado lleve a cabo acciones perjudiciales.</span><span class="sxs-lookup"><span data-stu-id="59c79-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="59c79-109">Un mecanismo de integridad [](../secauthz/securable-objects.md) restringe el acceso de escritura a objetos protegibles mediante procesos de menor integridad, de la misma manera que la pertenencia a grupos de cuentas de usuario restringe los derechos de los usuarios para acceder a componentes confidenciales del sistema.</span><span class="sxs-lookup"><span data-stu-id="59c79-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="59c79-110">[Interfaz de usuario aislamiento de privilegios de usuario (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impide que los procesos envíen mensajes de ventana seleccionados y otras API DE USUARIO a procesos que se ejecutan con mayor integridad.</span><span class="sxs-lookup"><span data-stu-id="59c79-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="59c79-111">La infraestructura de seguridad del mecanismo de integridad de Windows permite que el modo protegido proporcione a Windows Internet Explorer los privilegios que los usuarios necesitan para examinar la Web, al tiempo que se retienen los privilegios que los usuarios necesitan para instalar programas en modo silencioso o modificar datos confidenciales del sistema.</span><span class="sxs-lookup"><span data-stu-id="59c79-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="59c79-112">Los usuarios pueden deshabilitar esta característica mediante una casilla y los administradores pueden deshabilitarla mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="59c79-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59c79-113">Debe deshabilitar la característica solo como medida temporal durante la solución de problemas para comparar el comportamiento de la aplicación cuando la característica está habilitada o no.</span><span class="sxs-lookup"><span data-stu-id="59c79-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="59c79-114">Se recomienda mantener esta característica habilitada permanentemente.</span><span class="sxs-lookup"><span data-stu-id="59c79-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="59c79-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59c79-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59c79-116">Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="59c79-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
