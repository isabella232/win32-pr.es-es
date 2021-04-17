---
description: Windows Installer realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Eliminación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652853"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="8b6e7-104">Eliminación de componentes aislados</span><span class="sxs-lookup"><span data-stu-id="8b6e7-104">Removal of Isolated Components</span></span>

<span data-ttu-id="8b6e7-105">Windows Installer realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="8b6e7-106">Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="8b6e7-107">Desinstalación</span><span class="sxs-lookup"><span data-stu-id="8b6e7-107">Uninstall</span></span>

-   <span data-ttu-id="8b6e7-108">Quite los archivos de componentes \_ compartidos de la carpeta que contiene la aplicación de componentes \_ solo si \_ también se está quitando la aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="8b6e7-109">Si el bit msidbComponentAttributesSharedDllRefCount se establece en la [tabla de componentes](component-table.md) , se reduce el recuento de SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="8b6e7-110">Quite el. Archivo de cero bytes LOCAL de la carpeta que contiene la aplicación de componentes \_ .</span><span class="sxs-lookup"><span data-stu-id="8b6e7-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="8b6e7-111">Quite \_ la aplicación de componentes de la lista de clientes de componentes \_ compartidos.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="8b6e7-112">Quite todos los recursos de la aplicación de componentes de la \_ forma habitual.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="8b6e7-113">Si quedan otros productos en la lista de clientes del componente \_ compartido:</span><span class="sxs-lookup"><span data-stu-id="8b6e7-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="8b6e7-114">No se quita ningún archivo de la ubicación compartida del componente \_ compartido.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="8b6e7-115">Si el recuento de SharedDLL del componente \_ compartido es 0 después de haber disminuido, o si no hay otros clientes restantes del componente \_ compartido:</span><span class="sxs-lookup"><span data-stu-id="8b6e7-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="8b6e7-116">Quite los archivos del componente \_ compartido de la ubicación compartida.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="8b6e7-117">Procesa todas las acciones de desinstalación con respecto a este componente.</span><span class="sxs-lookup"><span data-stu-id="8b6e7-117">Process all uninstall actions with respect to this component.</span></span>

 

 



