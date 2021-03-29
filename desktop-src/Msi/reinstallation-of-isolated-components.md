---
description: Windows Installer realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909446"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="e7f90-104">Reinstalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="e7f90-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="e7f90-105">Windows Installer realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados.</span><span class="sxs-lookup"><span data-stu-id="e7f90-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="e7f90-106">Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.</span><span class="sxs-lookup"><span data-stu-id="e7f90-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="e7f90-107">Reinstalación</span><span class="sxs-lookup"><span data-stu-id="e7f90-107">Reinstallation</span></span>

-   <span data-ttu-id="e7f90-108">Vuelva a instalar los archivos de componentes \_ compartidos en la misma carpeta que la aplicación de componentes \_ solo si \_ también se está reinstalando la aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="e7f90-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="e7f90-109">No incremente la lista de cliente del componente \_ compartido y no aumente el número de SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="e7f90-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="e7f90-110">Vuelva a crear el archivo de cero bytes con el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ .</span><span class="sxs-lookup"><span data-stu-id="e7f90-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="e7f90-111">Este archivo debe estar ubicado en la misma carpeta que \_ la aplicación de componentes y tener la extensión. Localizar.</span><span class="sxs-lookup"><span data-stu-id="e7f90-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="e7f90-112">Vuelva a instalar todos los recursos de la aplicación de componentes de la \_ forma habitual.</span><span class="sxs-lookup"><span data-stu-id="e7f90-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="e7f90-113">Si el recuento de SharedDLL del componente \_ compartido es mayor que 1, o si otros productos permanecen en la lista de clientes \_ compartida:</span><span class="sxs-lookup"><span data-stu-id="e7f90-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="e7f90-114">Reinstalar ningún archivo en la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="e7f90-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="e7f90-115">Si el recuento de SharedDLL del componente \_ compartido es igual a 1, o si no hay otros clientes restantes del componente \_ compartido:</span><span class="sxs-lookup"><span data-stu-id="e7f90-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="e7f90-116">Vuelva a instalar los archivos de componentes \_ compartidos en la ubicación compartida con las [reglas de control de versiones de archivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e7f90-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="e7f90-117">Procesa todas las acciones de reinstalación del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="e7f90-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="e7f90-118">Si \_ el componente compartido es un componente com, registre la ruta de acceso completa de com de forma que las sintaxis del instalador \[ $Component \] y \[ \# FileKey \] señalen a la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="e7f90-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



