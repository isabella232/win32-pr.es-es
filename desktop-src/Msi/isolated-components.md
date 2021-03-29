---
description: Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos dll compartidos normalmente) de una aplicación en la carpeta de la aplicación en lugar de en una ubicación compartida.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808738"
---
# <a name="isolated-components"></a><span data-ttu-id="4d93d-103">Componentes aislados</span><span class="sxs-lookup"><span data-stu-id="4d93d-103">Isolated Components</span></span>

<span data-ttu-id="4d93d-104">Los autores de paquetes de instalación pueden especificar que el instalador copie los archivos compartidos (archivos dll compartidos normalmente) de una aplicación en la carpeta de la aplicación en lugar de en una ubicación compartida.</span><span class="sxs-lookup"><span data-stu-id="4d93d-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="4d93d-105">Este conjunto privado de archivos (dll) solo se usa en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d93d-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="4d93d-106">El aislamiento de la aplicación junto con sus componentes compartidos de esta manera presenta las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="4d93d-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="4d93d-107">La aplicación siempre usa las versiones de los archivos compartidos con los que se implementó.</span><span class="sxs-lookup"><span data-stu-id="4d93d-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="4d93d-108">La instalación de la aplicación no sobrescribe otras versiones de los archivos compartidos por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d93d-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="4d93d-109">Las instalaciones posteriores de otras aplicaciones que usan versiones diferentes de los archivos compartidos no pueden sobrescribir los archivos usados por esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d93d-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="4d93d-110">Dado que la implementación actual de COM mantiene una única ruta de acceso completa en el registro para cada par de CLSID/contexto, obliga a todas las aplicaciones a usar la misma versión de un archivo DLL compartido.</span><span class="sxs-lookup"><span data-stu-id="4d93d-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="4d93d-111">Para permitir que una aplicación mantenga una copia privada de un servidor COM, el cargador del sistema de Windows 2000 comprueba la presencia de un. Archivo LOCAL en la carpeta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d93d-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="4d93d-112">Si el cargador del sistema detecta un. Archivo LOCAL, modifica la lógica de búsqueda para preferir archivos dll ubicados en la misma carpeta que la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d93d-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="4d93d-113">Cuando Windows Installer ejecuta la [acción IsolateComponents](isolatecomponents-action.md) , copia los archivos del componente (normalmente, un archivo dll compartido) especificados en la \_ columna compartida componente de la [tabla IsolatedComponent](isolatedcomponent-table.md) en la misma carpeta que el componente (normalmente, un archivo. exe) que se especifica en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="4d93d-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="4d93d-114">El instalador crea un archivo en este directorio, de cero bytes de longitud y tiene el nombre corto de archivo del archivo de clave de la aplicación de componentes \_ (normalmente, el nombre es el mismo que el. exe de la aplicación) anexado con. Localizar.</span><span class="sxs-lookup"><span data-stu-id="4d93d-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="4d93d-115">El instalador usa el registro para el componente en su ubicación compartida y no escribe información de registro para la copia del componente en la ubicación privada.</span><span class="sxs-lookup"><span data-stu-id="4d93d-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="4d93d-116">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="4d93d-116">For more information, see:</span></span>

-   [<span data-ttu-id="4d93d-117">Instalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="4d93d-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="4d93d-118">Reinstalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="4d93d-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="4d93d-119">Eliminación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="4d93d-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="4d93d-120">Usar componentes aislados</span><span class="sxs-lookup"><span data-stu-id="4d93d-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



