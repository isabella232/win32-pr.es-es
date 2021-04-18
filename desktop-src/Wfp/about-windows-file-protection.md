---
description: Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Acerca de Protección de recursos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706992"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="7b2fa-103">Acerca de Protección de recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="7b2fa-103">About Windows Resource Protection</span></span>

<span data-ttu-id="7b2fa-104">Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="7b2fa-105">Estuvo disponible a partir de Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="7b2fa-106">El permiso para el acceso completo para modificar los recursos protegidos por WRP está restringido a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="7b2fa-107">Los recursos protegidos por WRP solo pueden cambiarse mediante los [mecanismos de sustitución de recursos admitidos](supported-file-replacement-mechanisms.md) con el servicio de instalador de módulos de Windows.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="7b2fa-108">La protección de estos recursos evita errores en la aplicación y en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="7b2fa-109">Las aplicaciones no deben intentar modificar los recursos protegidos por WRP porque Windows y otras aplicaciones las utilizan.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="7b2fa-110">Si una aplicación intenta modificar un recurso protegido por WRP, puede tener los siguientes resultados.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="7b2fa-111">Es posible que los instaladores de aplicaciones que intenten reemplazar, modificar o eliminar claves de registro o archivos críticos de Windows no puedan instalar la aplicación y reciban un mensaje de error que indica que se denegó el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="7b2fa-112">Las aplicaciones que intentan agregar o quitar las subclaves o cambiar los valores de las claves del registro protegidas pueden producir un error y recibirán un mensaje de error que indica que se denegó el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="7b2fa-113">Se puede producir un error en las aplicaciones que se basan en la escritura de información en claves, carpetas o archivos protegidos del registro.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="7b2fa-114">WRP es el nuevo nombre de protección de archivos de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="7b2fa-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="7b2fa-115">WRP protege las claves del registro y las carpetas, así como los archivos esenciales del sistema.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="7b2fa-116">WFP estaba disponible en Microsoft Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7b2fa-117">WRP reemplaza WFP en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b2fa-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="7b2fa-118">En los temas siguientes se describe WRP:</span><span class="sxs-lookup"><span data-stu-id="7b2fa-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="7b2fa-119">Lista de recursos protegidos</span><span class="sxs-lookup"><span data-stu-id="7b2fa-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="7b2fa-120">Detección de reemplazo de recursos</span><span class="sxs-lookup"><span data-stu-id="7b2fa-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="7b2fa-121">Mecanismos de sustitución de recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="7b2fa-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="7b2fa-122">Comprobador de archivos de sistema</span><span class="sxs-lookup"><span data-stu-id="7b2fa-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="7b2fa-123">Consideraciones de administración remota</span><span class="sxs-lookup"><span data-stu-id="7b2fa-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



