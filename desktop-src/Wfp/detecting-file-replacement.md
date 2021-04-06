---
description: Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte de Windows Vista o Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Detección de reemplazo de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817038"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="4a64b-103">Detección de reemplazo de recursos</span><span class="sxs-lookup"><span data-stu-id="4a64b-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="4a64b-104">Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte de Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4a64b-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="4a64b-105">WRP protege archivos, carpetas y claves del registro en Windows Vista o Windows Server 2008 detectando e impidiendo intentos de reemplazar recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="4a64b-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="4a64b-106">Esta protección se basa en una lista de control de acceso discrecional (DACL) de Windows y en las listas de control de acceso (ACL) definidas para los recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="4a64b-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="4a64b-107">El permiso para el acceso completo para modificar los recursos protegidos por WRP está restringido a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="4a64b-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="4a64b-108">Los recursos protegidos por WRP solo pueden cambiarse mediante los [mecanismos de sustitución de recursos admitidos](supported-file-replacement-mechanisms.md) con el servicio de instalador de módulos de Windows.</span><span class="sxs-lookup"><span data-stu-id="4a64b-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="4a64b-109">Las aplicaciones que intentan modificar un recurso protegido por WRP nunca cambian el recurso y pueden recibir un mensaje de error que indica que se denegó el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="4a64b-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="4a64b-110">Las aplicaciones y los instaladores pueden usar las funciones [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) para determinar si un archivo o una clave del registro están protegidos.</span><span class="sxs-lookup"><span data-stu-id="4a64b-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="4a64b-111">\* \* Windows Server 2003 y Windows XP: \* \*</span><span class="sxs-lookup"><span data-stu-id="4a64b-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="4a64b-112">Protección de archivos de Windows (WFP) protege los archivos del sistema mediante la detección de intentos de reemplazar archivos del sistema protegidos.</span><span class="sxs-lookup"><span data-stu-id="4a64b-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="4a64b-113">Esta protección se desencadena después de que WFP reciba una notificación de cambio de directorio para un archivo en un directorio protegido.</span><span class="sxs-lookup"><span data-stu-id="4a64b-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="4a64b-114">Cuando WFP recibe esta notificación, determina qué archivo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4a64b-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="4a64b-115">Si el archivo está protegido, WFP busca la firma de archivo en un archivo de catálogo para determinar si el nuevo archivo es la versión correcta.</span><span class="sxs-lookup"><span data-stu-id="4a64b-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="4a64b-116">Si la versión del archivo no es correcta, el sistema reemplaza el archivo con la versión correcta de la memoria caché o del medio de distribución, dependiendo de si el archivo se encuentra en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="4a64b-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="4a64b-117">WFP busca el archivo correcto en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="4a64b-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="4a64b-118">Busque en el directorio de caché.</span><span class="sxs-lookup"><span data-stu-id="4a64b-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="4a64b-119">Busque la ruta de instalación de red, si el sistema se instaló con la instalación de red.</span><span class="sxs-lookup"><span data-stu-id="4a64b-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="4a64b-120">Busque en un CD-ROM de Windows si el sistema se instaló desde el CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="4a64b-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="4a64b-121">Si WFP no puede encontrar automáticamente el archivo en las dos primeras ubicaciones, muestra el siguiente mensaje:</span><span class="sxs-lookup"><span data-stu-id="4a64b-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![mensaje de WFP mostrado cuando no se encuentra el archivo en el directorio de caché o la ruta de instalación de red](images/wfp-1.png)

<span data-ttu-id="4a64b-123">Si el sistema se instaló con un CD-ROM, WFP muestra el siguiente mensaje:</span><span class="sxs-lookup"><span data-stu-id="4a64b-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![mensaje de WFP que se muestra para solicitar al usuario que inserte el CD-ROM de Windows](images/wfp-2.png)

<span data-ttu-id="4a64b-125">Si un administrador no ha iniciado sesión, WFP no puede mostrar ninguno de estos cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4a64b-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="4a64b-126">WFP mostrará el cuadro de diálogo después de que un administrador inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="4a64b-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="4a64b-127">WFP también registra el intento de reemplazo del archivo en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a64b-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="4a64b-128">Si el administrador canceló la restauración del archivo correcto, WFP registra la cancelación.</span><span class="sxs-lookup"><span data-stu-id="4a64b-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="4a64b-129">Recuperando la lista de archivos protegidos</span><span class="sxs-lookup"><span data-stu-id="4a64b-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="4a64b-130">En el ejemplo siguiente se muestra cómo las aplicaciones y los instaladores pueden usar la función [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) para obtener la lista completa de archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="4a64b-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



