---
description: La API de documentos XPS implementa el modelo de objetos XPS y permite a los desarrolladores crear un OM XPS, manipular el contenido de un documento XPS en programas nativos de Windows \\ \\ y guardar el OM XPS en un archivo o una secuencia como un documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Acerca de la API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697516"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="11e32-103">Acerca de la API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="11e32-103">About XPS Document API</span></span>

<span data-ttu-id="11e32-104">La [API de documentos XPS](documents-xps.md) implementa el modelo de objetos XPS y permite a los desarrolladores crear un OM XPS, manipular el contenido de un documento XPS en programas nativos de Windows \\ \\ y guardar el OM XPS en un archivo o una secuencia como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="11e32-105">Los desarrolladores de módulos de canalización de filtros XPSDrv también pueden usar la API de documentos XPS para manipular el contenido de un documento XPS en un filtro de controlador de impresora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="11e32-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="11e32-106">Introducción a la API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="11e32-106">XPS Document API Overview</span></span>

<span data-ttu-id="11e32-107">El modelo de objetos XPS es el modelo de información de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="11e32-108">El modelo de información del documento XPS es independiente del modelo de marcado que se utiliza dentro de los elementos del documento.</span><span class="sxs-lookup"><span data-stu-id="11e32-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="11e32-109">El modelo de objetos XPS describe la organización de los componentes internos que componen un documento XPS y el modelo de marcado describe el contenido de esos componentes.</span><span class="sxs-lookup"><span data-stu-id="11e32-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="11e32-110">En un programa, se crea una instancia del modelo de objetos XPS como un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="11e32-111">El OM XPS es esencialmente una versión en memoria del contenido de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="11e32-112">Aunque es similar en una organización lógica a un documento XPS, un OM XPS no se considera un documento XPS hasta que se ha serializado a un archivo o una secuencia.</span><span class="sxs-lookup"><span data-stu-id="11e32-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="11e32-113">La estructura exacta del marcado no está disponible para el modelo de objetos XPS cuando se deserializa un documento XPS del marcado a un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="11e32-114">Por ejemplo, si la propiedad se representara como un elemento o un atributo en el marcado, el OM XPS presenta el valor de la propiedad de un objeto de documento exactamente de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="11e32-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="11e32-115">La [API de documento XPS](documents-xps.md) se puede dividir en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="11e32-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="11e32-116">Interfaces troncales de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="11e32-117">Las interfaces de tronco proporcionan acceso a los componentes de nivel superior de la estructura del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="11e32-118">Estas interfaces también proporcionan los medios para serializar un modelo de objetos XPS y deserializar un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="11e32-119">Interfaces de página de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="11e32-120">Las interfaces de página proporcionan acceso al contenido de una página en un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="11e32-121">Las interfaces que describen el contenido de la página también se incluyen con las interfaces de página.</span><span class="sxs-lookup"><span data-stu-id="11e32-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="11e32-122">Firmas digitales de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="11e32-123">El modelo de objetos de XPS admite firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="11e32-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="11e32-124">Sin embargo, puede tener acceso a las firmas digitales en un documento XPS directamente sin crear un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="11e32-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="11e32-125">Para obtener más información sobre cómo acceder a las firmas digitales XPS sin un OM XPS, consulte la [API de firma digital XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="11e32-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="11e32-126">Interfaces de vales de impresión de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="11e32-127">Los documentos XPS admiten la impresión de vales en el nivel de paquete (trabajo), documento y página.</span><span class="sxs-lookup"><span data-stu-id="11e32-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="11e32-128">Los vales de impresión contienen información sobre cómo dar formato al contenido del documento para imprimirlo o verlo.</span><span class="sxs-lookup"><span data-stu-id="11e32-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11e32-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11e32-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="11e32-130">**En esta sección**</span><span class="sxs-lookup"><span data-stu-id="11e32-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="11e32-131">Interfaces troncales de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="11e32-132">Interfaces de página de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="11e32-133">Firmas digitales de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="11e32-134">Interfaces de vales de impresión de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="11e32-135">**Otros temas relacionados**</span><span class="sxs-lookup"><span data-stu-id="11e32-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="11e32-136">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="11e32-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="11e32-137">Firmas digitales de XPS OM</span><span class="sxs-lookup"><span data-stu-id="11e32-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="11e32-138">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="11e32-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="11e32-139">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="11e32-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



