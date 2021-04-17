---
description: El reemplazo de recursos protegidos se admite a través de los siguientes mecanismos.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de sustitución de recursos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706990"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="dd484-103">Mecanismos de sustitución de recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="dd484-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="dd484-104">El reemplazo de recursos protegidos se admite a través de los siguientes mecanismos.</span><span class="sxs-lookup"><span data-stu-id="dd484-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="dd484-105">El permiso para el acceso completo para modificar los recursos protegidos por WRP en Windows Vista y Windows Server 2008 está restringido a TrustedInstaller con el servicio de instalador de módulos de Windows mediante los siguientes mecanismos:</span><span class="sxs-lookup"><span data-stu-id="dd484-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="dd484-106">Los Service Pack de Windows instalados por TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="dd484-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="dd484-107">Revisiones instaladas por TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="dd484-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="dd484-108">Actualizaciones del sistema operativo instaladas por TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="dd484-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="dd484-109">Windows Update instala por TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="dd484-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="dd484-110">Las aplicaciones y los instaladores que intentan reemplazar un recurso protegido por WRP por medio de otros métodos especificados tienen denegado el acceso para cambiar el recurso y generar un mensaje de error de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dd484-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="dd484-111">En el caso de los instaladores conocidos que intentan reemplazar recursos protegidos por WRP, se puede suprimir el error de acceso denegado y el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="dd484-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="dd484-112">En este caso, la operación se devuelve correctamente, se suprime el error y el mensaje de error, pero no se aplica ningún cambio al recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="dd484-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="dd484-113">El error se puede suprimir para un instalador conocido solo cuando se cumplen todos los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd484-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="dd484-114">Se trata de una aplicación heredada.</span><span class="sxs-lookup"><span data-stu-id="dd484-114">This is a legacy application.</span></span> <span data-ttu-id="dd484-115">La aplicación no incluye un manifiesto con un requestedExecutionlevel que identifique la aplicación tal y como se diseñó para Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dd484-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="dd484-116">El error de acceso denegado se debe a que solo se intenta modificar un recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="dd484-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="dd484-117">Un administrador está instalando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd484-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="dd484-118">Para obtener información acerca del uso del Windows Installer con WRP, consulte [uso de Windows Installer y protección de recursos de Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) en el SDK de [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .</span><span class="sxs-lookup"><span data-stu-id="dd484-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="dd484-119">**Windows Server 2003 y Windows XP:** El reemplazo de archivos del sistema protegidos por WFP solo se admite a través de los siguientes mecanismos:</span><span class="sxs-lookup"><span data-stu-id="dd484-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="dd484-120">Instalación de Windows Service Pack mediante Update.exe</span><span class="sxs-lookup"><span data-stu-id="dd484-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="dd484-121">Revisiones instaladas mediante Hotfix.exe</span><span class="sxs-lookup"><span data-stu-id="dd484-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="dd484-122">Actualizaciones del sistema operativo con Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="dd484-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="dd484-123">Windows Update</span><span class="sxs-lookup"><span data-stu-id="dd484-123">Windows Update</span></span>

<span data-ttu-id="dd484-124">Reemplazar archivos protegidos por medio de otros métodos especificados hace que WFP restaure los archivos originales.</span><span class="sxs-lookup"><span data-stu-id="dd484-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
