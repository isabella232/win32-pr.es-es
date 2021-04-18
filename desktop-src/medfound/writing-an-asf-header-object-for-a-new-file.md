---
description: Escribir un objeto de encabezado ASF para un nuevo archivo
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Escribir un objeto de encabezado ASF para un nuevo archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707012"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="65eb8-103">Escribir un objeto de encabezado ASF para un nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="65eb8-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="65eb8-104">El objeto ContentInfo de ASF almacena la información del objeto de encabezado ASF para un archivo.</span><span class="sxs-lookup"><span data-stu-id="65eb8-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="65eb8-105">Cuando se crea o modifica un archivo ASF, debe generarse el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="65eb8-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="65eb8-106">Para ello, la aplicación debe proporcionar el perfil de codificación del contenido al objeto ContentInfo para que conozca las características del archivo multimedia que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="65eb8-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="65eb8-107">Para escribir un nuevo archivo, puede usar el objeto ContentInfo para:</span><span class="sxs-lookup"><span data-stu-id="65eb8-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="65eb8-108">Recopile información de encabezado del objeto de perfil del archivo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="65eb8-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="65eb8-109">Rellene los distintos objetos de encabezado de la biblioteca ASF que mantiene internamente Media Foundation,</span><span class="sxs-lookup"><span data-stu-id="65eb8-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="65eb8-110">Inicialice el [multiplexor ASF](asf-multiplexer.md) para la generación de paquetes de datos ASF y</span><span class="sxs-lookup"><span data-stu-id="65eb8-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="65eb8-111">Construya el objeto de encabezado de nivel superior en formato binario que se puede escribir en un archivo.</span><span class="sxs-lookup"><span data-stu-id="65eb8-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="65eb8-112">Para obtener información acerca de los perfiles, consulte [ASF Profile](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="65eb8-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="65eb8-113">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="65eb8-113">This section contains the following topics:</span></span>



| <span data-ttu-id="65eb8-114">Tema</span><span class="sxs-lookup"><span data-stu-id="65eb8-114">Topic</span></span>                                                                                                              | <span data-ttu-id="65eb8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="65eb8-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65eb8-116">Inicializar el objeto ContentInfo de un nuevo archivo ASF</span><span class="sxs-lookup"><span data-stu-id="65eb8-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="65eb8-117">Describe el método [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) que inicializa el objeto ContentInfo con la información de encabezado almacenada en un objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="65eb8-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="65eb8-118">Establecer propiedades en el objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="65eb8-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="65eb8-119">Información sobre las distintas propiedades de configuración que se deben establecer en el objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="65eb8-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="65eb8-120">Generar un nuevo objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="65eb8-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="65eb8-121">Cómo generar un búfer multimedia, que contiene el objeto de encabezado ASF real del nuevo archivo, del objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="65eb8-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="65eb8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65eb8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65eb8-123">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="65eb8-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="65eb8-124">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="65eb8-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="65eb8-125">Estructura de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="65eb8-125">ASF File Structure</span></span>
</dt> </dl>

 

 



