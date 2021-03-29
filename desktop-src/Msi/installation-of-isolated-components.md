---
description: Windows Installer realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811474"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="7727d-104">Instalación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="7727d-104">Installation of Isolated Components</span></span>

<span data-ttu-id="7727d-105">Windows Installer realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados.</span><span class="sxs-lookup"><span data-stu-id="7727d-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="7727d-106">Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.</span><span class="sxs-lookup"><span data-stu-id="7727d-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="7727d-107">Instalación</span><span class="sxs-lookup"><span data-stu-id="7727d-107">Installation</span></span>

-   <span data-ttu-id="7727d-108">Copie los archivos de componentes \_ compartidos en la misma carpeta que la aplicación de componentes \_ solo si \_ también se está instalando la aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="7727d-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="7727d-109">Cree un archivo de cero bytes con el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ .</span><span class="sxs-lookup"><span data-stu-id="7727d-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="7727d-110">Busque este archivo en la misma carpeta que la \_ aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="7727d-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="7727d-111">Anexe la extensión. LOCAL a este nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7727d-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="7727d-112">Incremente el recuento de SharedDLL si el bit msidbComponentAttributesSharedDllRefCount se establece en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7727d-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="7727d-113">Registre \_ la aplicación de componentes como un cliente del componente \_ compartido y registre una ruta de acceso de clave que apunte a la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="7727d-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="7727d-114">Instale todos los recursos de la aplicación de componentes de la \_ forma habitual.</span><span class="sxs-lookup"><span data-stu-id="7727d-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="7727d-115">Si \_ el componente compartido o su archivo de clave ya está instalado en el equipo, no copie los archivos en la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="7727d-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="7727d-116">Si \_ el componente compartido o su archivo de clave todavía no está instalado en el equipo:</span><span class="sxs-lookup"><span data-stu-id="7727d-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="7727d-117">Copie los archivos del componente \_ compartido en la ubicación compartida.</span><span class="sxs-lookup"><span data-stu-id="7727d-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="7727d-118">Procesa todas las acciones de instalación del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="7727d-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="7727d-119">Si \_ el componente compartido es un componente com, registre la ruta de acceso completa de com de forma que la sintaxis \[ $Component \] y \[ \# FileKey \] señalen a la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="7727d-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



