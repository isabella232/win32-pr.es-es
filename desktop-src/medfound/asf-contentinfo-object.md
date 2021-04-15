---
description: Objeto ContentInfo de ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objeto ContentInfo de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696187"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="a2232-103">Objeto ContentInfo de ASF</span><span class="sxs-lookup"><span data-stu-id="a2232-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="a2232-104">El objeto *ContentInfo* de ASF almacena información del objeto de encabezado ASF de un archivo.</span><span class="sxs-lookup"><span data-stu-id="a2232-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="a2232-105">Una aplicación puede utilizar el objeto ContentInfo para los siguientes fines:</span><span class="sxs-lookup"><span data-stu-id="a2232-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="a2232-106">Lea el objeto de encabezado de un archivo multimedia existente.</span><span class="sxs-lookup"><span data-stu-id="a2232-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="a2232-107">En este caso, el objeto ContentInfo analiza el objeto de encabezado y almacena información sobre el archivo de características.</span><span class="sxs-lookup"><span data-stu-id="a2232-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="a2232-108">Media Foundation expone algunas de estas propiedades a través de atributos e interfaces.</span><span class="sxs-lookup"><span data-stu-id="a2232-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="a2232-109">Se describen en [Media Foundation atributos para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a2232-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="a2232-110">Escribir información de encabezado y construir un objeto de encabezado para un archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="a2232-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="a2232-111">Inicialice otros objetos ASF, como el [separador](asf-splitter.md)ASF, el [multiplexor ASF](asf-multiplexer.md)y el indexador ASF, al leer o escribir un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a2232-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="a2232-112">Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a2232-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="a2232-113">Crear el objeto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="a2232-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="a2232-114">Para crear una nueva instancia del objeto ContentInfo, llame a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="a2232-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="a2232-115">Este método devuelve un puntero a un objeto ContentInfo vacío que se debe inicializar para que funcione con un archivo ASF específico.</span><span class="sxs-lookup"><span data-stu-id="a2232-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="a2232-116">En función de si la aplicación Lee un archivo existente o escribe un nuevo archivo ASF, debe llamar a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) o [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para rellenar el objeto vacío.</span><span class="sxs-lookup"><span data-stu-id="a2232-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="a2232-117">Para obtener más información acerca de estas llamadas a métodos, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a2232-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="a2232-118">Leer el objeto de encabezado ASF de un archivo existente</span><span class="sxs-lookup"><span data-stu-id="a2232-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="a2232-119">Obtener información de los objetos de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="a2232-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="a2232-120">Escribir un objeto de encabezado ASF para un nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="a2232-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="a2232-121">Media Foundation atributos para los objetos de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="a2232-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="a2232-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2232-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2232-123">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="a2232-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



