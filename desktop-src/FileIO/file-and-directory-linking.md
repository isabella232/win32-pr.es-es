---
description: 'En el sistema de archivos NTFS se admiten dos tipos de vínculos: vínculos físicos y uniones.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Vinculación de archivos y directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002866"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="dcbb8-103">Vinculación de archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="dcbb8-103">File and Directory Linking</span></span>

<span data-ttu-id="dcbb8-104">El sistema de archivos NTFS proporciona la capacidad de crear una representación del sistema de un archivo o un directorio en una ubicación de la estructura de directorios diferente del objeto de archivo o directorio al que se está vinculando.</span><span class="sxs-lookup"><span data-stu-id="dcbb8-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="dcbb8-105">Este proceso se denomina vinculación.</span><span class="sxs-lookup"><span data-stu-id="dcbb8-105">This process is called linking.</span></span> <span data-ttu-id="dcbb8-106">En el sistema de archivos NTFS se admiten dos tipos de vínculos: [vínculos físicos y uniones](hard-links-and-junctions.md).</span><span class="sxs-lookup"><span data-stu-id="dcbb8-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="dcbb8-107">El sistema de archivos NTFS también proporciona el [servicio de seguimiento de vínculos distribuido](distributed-link-tracking-and-object-identifiers.md), que realiza un seguimiento automático de los vínculos a medida que se mueven.</span><span class="sxs-lookup"><span data-stu-id="dcbb8-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dcbb8-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dcbb8-108">In this section</span></span>



| <span data-ttu-id="dcbb8-109">Tema</span><span class="sxs-lookup"><span data-stu-id="dcbb8-109">Topic</span></span>                                                                                                               | <span data-ttu-id="dcbb8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcbb8-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcbb8-111">Vínculos físicos y uniones</span><span class="sxs-lookup"><span data-stu-id="dcbb8-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="dcbb8-112">Describe los vínculos físicos y las uniones.</span><span class="sxs-lookup"><span data-stu-id="dcbb8-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="dcbb8-113">Seguimiento de vínculos distribuidos e identificadores de objetos</span><span class="sxs-lookup"><span data-stu-id="dcbb8-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="dcbb8-114">El **servicio de seguimiento de vínculos distribuidos** permite a las aplicaciones cliente realizar un seguimiento de los orígenes de vínculos que se han despasado.</span><span class="sxs-lookup"><span data-stu-id="dcbb8-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




