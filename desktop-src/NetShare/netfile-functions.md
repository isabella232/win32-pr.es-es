---
description: Las funciones de archivo de red proporcionan una manera de supervisar y cerrar el archivo, el dispositivo y los recursos de canalización abiertos en un servidor. A continuación se enumeran las funciones de archivo.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funciones de NetFile (administración de recursos compartidos de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678299"
---
# <a name="netfile-functions-network-share-management"></a><span data-ttu-id="d5724-104">Funciones de NetFile (administración de recursos compartidos de red)</span><span class="sxs-lookup"><span data-stu-id="d5724-104">NetFile Functions (Network Share Management)</span></span>

<span data-ttu-id="d5724-105">Las funciones de archivo de red proporcionan una manera de supervisar y cerrar el archivo, el dispositivo y los recursos de canalización abiertos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d5724-105">The network file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="d5724-106">A continuación se enumeran las funciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="d5724-106">The file functions are listed following.</span></span>



| <span data-ttu-id="d5724-107">Función</span><span class="sxs-lookup"><span data-stu-id="d5724-107">Function</span></span>                                 | <span data-ttu-id="d5724-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5724-108">Description</span></span>                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d5724-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="d5724-109">**NetFileClose**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="d5724-110">Fuerza el cierre de un recurso.</span><span class="sxs-lookup"><span data-stu-id="d5724-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="d5724-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="d5724-111">**NetFileEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="d5724-112">Devuelve información acerca de los archivos abiertos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d5724-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="d5724-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d5724-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="d5724-114">Devuelve información sobre una apertura determinada de un recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="d5724-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="d5724-115">Llame a la función [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) cuando el archivo no se pueda cerrar por otros medios.</span><span class="sxs-lookup"><span data-stu-id="d5724-115">Call the [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="d5724-116">Esta función se debe utilizar con precaución, ya que **NetFileClose** no escribe los datos almacenados en caché en el sistema cliente en el archivo antes de cerrar el archivo.</span><span class="sxs-lookup"><span data-stu-id="d5724-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="d5724-117">La función [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) devuelve información acerca de los recursos abiertos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="d5724-117">The [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="d5724-118">Una o varias aplicaciones pueden abrir un archivo una o varias veces.</span><span class="sxs-lookup"><span data-stu-id="d5724-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="d5724-119">Cada apertura de archivo se identifica de forma única.</span><span class="sxs-lookup"><span data-stu-id="d5724-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="d5724-120">La función **NetFileEnum** devuelve una entrada para cada apertura de archivo.</span><span class="sxs-lookup"><span data-stu-id="d5724-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="d5724-121">La función [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) devuelve información acerca de una apertura de un recurso.</span><span class="sxs-lookup"><span data-stu-id="d5724-121">The [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="d5724-122">La información del archivo está disponible en los siguientes niveles.</span><span class="sxs-lookup"><span data-stu-id="d5724-122">File information is available at the following levels.</span></span>

<dl>

[<span data-ttu-id="d5724-123">**Información de archivo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d5724-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[<span data-ttu-id="d5724-124">**Información de archivo \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d5724-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

<span data-ttu-id="d5724-125">No se admiten los niveles 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="d5724-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="d5724-126">El nivel 2 devuelve solo el número de identificación asignado al recurso cuando se abrió.</span><span class="sxs-lookup"><span data-stu-id="d5724-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="d5724-127">El nivel 3 devuelve el número de identificación, los permisos, los bloqueos de archivos y el nombre del usuario que abrió el recurso.</span><span class="sxs-lookup"><span data-stu-id="d5724-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="d5724-128">Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr llamando a las funciones [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) y [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) .</span><span class="sxs-lookup"><span data-stu-id="d5724-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="d5724-129">Para obtener más información, vea [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) y [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="d5724-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
