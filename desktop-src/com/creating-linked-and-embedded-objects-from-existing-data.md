---
title: Crear objetos vinculados e incrustados a partir de datos existentes
description: Crear objetos vinculados e incrustados a partir de datos existentes
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779801"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="e7f5b-103">Crear objetos vinculados e incrustados a partir de datos existentes</span><span class="sxs-lookup"><span data-stu-id="e7f5b-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="e7f5b-104">Normalmente, un usuario ensambla un documento compuesto con el portapapeles o con arrastrar y colocar para copiar un objeto de datos de su aplicación de servidor en la aplicación contenedora del usuario.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="e7f5b-105">Con las aplicaciones que admiten OLE, el usuario puede iniciar la transferencia desde el servidor o el contenedor.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="e7f5b-106">Por ejemplo, el servidor puede copiar datos en el portapapeles en la aplicación de servidor, cambiar a la aplicación contenedora y elegir pegar un objeto especial o incrustado o un comando de menú equivalente para crear un nuevo objeto incrustado a partir de los datos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="e7f5b-107">O bien, el usuario puede arrastrar los datos de una aplicación al otro.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="e7f5b-108">El proceso es similar para crear un objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="e7f5b-109">Una aplicación que funciona como servidor OLE y como contenedor puede utilizar una selección de sus propios datos para crear un objeto incrustado o vinculado en una nueva ubicación dentro del mismo documento.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="e7f5b-110">La transferencia de datos entre el servidor OLE y las aplicaciones de contenedor se basa en la transferencia de datos uniforme, como se describe en [transferencia de datos](data-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="e7f5b-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="e7f5b-111">Los servidores OLE y los controladores de objetos implementan [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) para que sus datos estén disponibles para las transferencias mediante el portapapeles o arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="e7f5b-112">Los objetos OLE admiten todos los formatos de Portapapeles habituales.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="e7f5b-113">Además, admiten seis formatos del portapapeles que admiten la creación de objetos vinculados e incrustados a partir de un objeto de datos seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="e7f5b-114">Los formatos del portapapeles OLE describen objetos de datos que, al colocarse o pegarse en contenedores OLE, se convertirán en objetos de documento compuesto incrustados o vinculados.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="e7f5b-115">El objeto de datos presenta estos formatos a las aplicaciones de contenedor en orden de fidelidad como descripciones de los datos.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="e7f5b-116">En otras palabras, el objeto presenta primero el formato que mejor lo representa, seguido del siguiente formato mejor, etc.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="e7f5b-117">Esta ordenación intencional fomenta que una aplicación contenedora use el mejor formato posible.</span><span class="sxs-lookup"><span data-stu-id="e7f5b-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7f5b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7f5b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f5b-119">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="e7f5b-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="e7f5b-120">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="e7f5b-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




