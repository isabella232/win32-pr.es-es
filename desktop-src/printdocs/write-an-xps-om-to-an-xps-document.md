---
description: Describe cómo escribir el contenido de un OM XPS en un programa en un archivo de documento XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Escribir un OM XPS en un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277674"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="b889e-103">Escribir un OM XPS en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="b889e-104">Describe cómo escribir el contenido de un OM XPS en un programa en un archivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b889e-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="b889e-105">Si un programa tiene un OM XPS que contiene un documento completo, el programa puede escribir el OM XPS en un archivo como un documento XPS, llamando al método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de la interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="b889e-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="b889e-106">Antes de usar estos ejemplos de código en un programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b889e-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="b889e-107">Escribir un OM XPS completo en un documento XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="b889e-108">Después de establecer el contenido de un OM XPS, puede guardar el OM XPS en un archivo como un documento XPS, llamando al método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) de la interfaz [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="b889e-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="b889e-109">Al escribir un OM XPS en un archivo o una secuencia, no se crea automáticamente una miniatura para el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b889e-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="b889e-110">Para crear una miniatura del documento XPS, use la interfaz [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b889e-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="b889e-111">Escritura incremental de un documento XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="b889e-112">La interfaz [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) se puede utilizar para escribir los elementos de un documento XPS de forma incremental. por ejemplo, cuando los elementos del documento se crean o procesan en secuencia.</span><span class="sxs-lookup"><span data-stu-id="b889e-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="b889e-113">Al escribir un OM XPS en un archivo o una secuencia, no se crea automáticamente una miniatura para el documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b889e-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="b889e-114">Para crear una miniatura del documento XPS, use la interfaz [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b889e-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b889e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b889e-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b889e-116">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="b889e-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="b889e-117">Imprimir un OM XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="b889e-118">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="b889e-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="b889e-119">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="b889e-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="b889e-120">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="b889e-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="b889e-121">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="b889e-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="b889e-122">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="b889e-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="b889e-123">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="b889e-124">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="b889e-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b889e-125">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b889e-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
