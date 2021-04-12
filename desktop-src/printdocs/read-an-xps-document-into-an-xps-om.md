---
description: Describe cómo leer un documento XPS existente de un archivo en un OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Leer un documento XPS en un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361243"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="06f13-103">Leer un documento XPS en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="06f13-104">Describe cómo leer un documento XPS existente de un archivo en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="06f13-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="06f13-105">Para crear un OM XPS a partir de un documento XPS, llame al método [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .</span><span class="sxs-lookup"><span data-stu-id="06f13-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="06f13-106">Antes de usar estos ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="06f13-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="06f13-107">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="06f13-107">Code Example</span></span>

<span data-ttu-id="06f13-108">En el ejemplo de código siguiente se da por supuesto que la inicialización descrita en [Initialize an XPS OM](xps-object-model-initialization.md) se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="06f13-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="06f13-109">Para crear un OM XPS a partir de un documento XPS que está almacenado como un flujo, llame a [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span><span class="sxs-lookup"><span data-stu-id="06f13-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="06f13-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06f13-110">Remarks</span></span>

<span data-ttu-id="06f13-111">Si escribe un OM XPS inmediatamente después de haber leído un paquete XPS en él, es posible que se pierda o cambie parte del contenido original.</span><span class="sxs-lookup"><span data-stu-id="06f13-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="06f13-112">En la tabla siguiente se enumeran algunos de los cambios que se pueden producir en este caso:</span><span class="sxs-lookup"><span data-stu-id="06f13-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="06f13-113">Característica de documento</span><span class="sxs-lookup"><span data-stu-id="06f13-113">Document feature</span></span>                      | <span data-ttu-id="06f13-114">Acción</span><span class="sxs-lookup"><span data-stu-id="06f13-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="06f13-115">Firmas digitales</span><span class="sxs-lookup"><span data-stu-id="06f13-115">Digital signatures</span></span><br/>         | <span data-ttu-id="06f13-116">Quitado del documento</span><span class="sxs-lookup"><span data-stu-id="06f13-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="06f13-117">Elemento DiscardControl</span><span class="sxs-lookup"><span data-stu-id="06f13-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="06f13-118">Quitado del documento</span><span class="sxs-lookup"><span data-stu-id="06f13-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="06f13-119">Partes de documentos externos</span><span class="sxs-lookup"><span data-stu-id="06f13-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="06f13-120">Quitado del documento</span><span class="sxs-lookup"><span data-stu-id="06f13-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="06f13-121">Marcado de FixedPage</span><span class="sxs-lookup"><span data-stu-id="06f13-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="06f13-122">Modificado desde el original</span><span class="sxs-lookup"><span data-stu-id="06f13-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="06f13-123">Marcado del Diccionario de recursos</span><span class="sxs-lookup"><span data-stu-id="06f13-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="06f13-124">Modificado desde el original, si se establece la marca de optimización</span><span class="sxs-lookup"><span data-stu-id="06f13-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="06f13-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06f13-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06f13-126">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="06f13-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="06f13-127">Navegar por el OM de XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="06f13-128">Escribir texto en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="06f13-129">Dibujar gráficos en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="06f13-130">Colocar imágenes en un OM XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="06f13-131">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="06f13-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="06f13-132">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="06f13-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="06f13-133">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="06f13-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="06f13-134">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="06f13-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="06f13-135">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="06f13-136">API de empaquetado</span><span class="sxs-lookup"><span data-stu-id="06f13-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="06f13-137">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="06f13-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="06f13-138">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="06f13-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

