---
description: Las interfaces de paquete representan el nivel superior del OM de XPS, que corresponde a un archivo de documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfaces de paquetes de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908624"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="56574-103">Interfaces de paquetes de XPS OM</span><span class="sxs-lookup"><span data-stu-id="56574-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="56574-104">Las interfaces de paquete representan el nivel superior del OM de XPS, que corresponde a un archivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="56574-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="56574-105">Estas interfaces contienen métodos que serializan un OM XPS en un documento o secuencia XPS y deserializan un paquete XPS para crear un OM XPS que permite a un programa tener acceso al contenido de un documento.</span><span class="sxs-lookup"><span data-stu-id="56574-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="56574-106">Nombre de interfaz</span><span class="sxs-lookup"><span data-stu-id="56574-106">Interface name</span></span>                                                  | <span data-ttu-id="56574-107">Interfaces secundarias lógicas</span><span class="sxs-lookup"><span data-stu-id="56574-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="56574-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="56574-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56574-109">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="56574-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="56574-110">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="56574-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="56574-111">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="56574-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="56574-112">El OM XPS completo que corresponde al paquete que contiene el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="56574-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="56574-113">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="56574-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="56574-114">None</span><span class="sxs-lookup"><span data-stu-id="56574-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="56574-115">Habilita la serialización incremental de las páginas del documento en un paquete.</span><span class="sxs-lookup"><span data-stu-id="56574-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="56574-116">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="56574-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="56574-117">None</span><span class="sxs-lookup"><span data-stu-id="56574-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="56574-118">Obtiene acceso a los metadatos del documento.</span><span class="sxs-lookup"><span data-stu-id="56574-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="56574-119">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="56574-119">Code Examples</span></span>

<span data-ttu-id="56574-120">En los ejemplos de código siguientes se muestra cómo se usan algunas de las interfaces de paquetes en un programa.</span><span class="sxs-lookup"><span data-stu-id="56574-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="56574-121">A menos que se indique lo contrario, todos los elementos en cursiva son nombres de parámetro.</span><span class="sxs-lookup"><span data-stu-id="56574-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="56574-122">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="56574-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="56574-123">Escribir un OM XPS en un archivo de documento XPS</span><span class="sxs-lookup"><span data-stu-id="56574-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="56574-124">Obtener acceso a la secuencia de documentos del OM de XPS</span><span class="sxs-lookup"><span data-stu-id="56574-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="56574-125">Acceder al CoreProperties del documento</span><span class="sxs-lookup"><span data-stu-id="56574-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="56574-126">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="56574-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="56574-127">A partir de un documento XPS existente cuyo nombre de archivo está almacenado en *xpsDocumentFilename*, en este ejemplo de código se crea un OM XPS al que hace referencia *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="56574-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="56574-128">Escribir un OM XPS en un archivo de documento XPS</span><span class="sxs-lookup"><span data-stu-id="56574-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="56574-129">En el ejemplo de código siguiente se escribe el OM XPS al que hace referencia *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="56574-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="56574-130">En el ejemplo se crea un documento XPS en el archivo cuyo nombre se almacena en *filename*.</span><span class="sxs-lookup"><span data-stu-id="56574-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="56574-131">Obtener acceso a la secuencia de documentos del OM de XPS</span><span class="sxs-lookup"><span data-stu-id="56574-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="56574-132">En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , que contiene la secuencia de documento del OM XPS que se representa mediante *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="56574-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="56574-133">Acceder al CoreProperties del documento</span><span class="sxs-lookup"><span data-stu-id="56574-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="56574-134">En el ejemplo de código siguiente se obtiene un puntero a la interfaz [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , lo que permite que el programa tenga acceso al contenido del elemento CoreProperties.</span><span class="sxs-lookup"><span data-stu-id="56574-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="56574-135">En el ejemplo, se supone que se ha leído el documento en un OM XPS representado por *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="56574-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a><span data-ttu-id="56574-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56574-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56574-137">Uso de la interfaz IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="56574-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="56574-138">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="56574-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="56574-139">**Interfaz IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="56574-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="56574-140">**Interfaz IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="56574-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="56574-141">**Interfaz IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="56574-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="56574-142">**Interfaz IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="56574-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




