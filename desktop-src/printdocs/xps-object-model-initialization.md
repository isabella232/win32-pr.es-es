---
description: Describe cómo inicializar un OM de XPS, que permite a un programa crear un documento XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Inicializar un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360565"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="943a3-103">Inicializar un OM XPS</span><span class="sxs-lookup"><span data-stu-id="943a3-103">Initialize an XPS OM</span></span>

<span data-ttu-id="943a3-104">Describe cómo inicializar un OM de XPS, que permite a un programa crear un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="943a3-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="943a3-105">Las interfaces de la API de documento XPS se crean mediante una interfaz [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) .</span><span class="sxs-lookup"><span data-stu-id="943a3-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="943a3-106">Para obtener un puntero a un **IXpsOMObjectFactory** que se pueda usar en el programa, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="943a3-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="943a3-107">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="943a3-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="943a3-108">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="943a3-108">Code Example</span></span>

<span data-ttu-id="943a3-109">En el ejemplo siguiente se crea el generador de objetos que se utilizará para crear interfaces XPS OM en otros ejemplos.</span><span class="sxs-lookup"><span data-stu-id="943a3-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="943a3-110">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="943a3-110">Best Practices</span></span>

<span data-ttu-id="943a3-111">Puede hacer que el programa sea más eficaz si obtiene un puntero a una interfaz [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la primera vez que necesita llamar a **IXpsOMObjectFactory** para crear una interfaz y, a continuación, guarda el puntero para usarlo en otras áreas del programa.</span><span class="sxs-lookup"><span data-stu-id="943a3-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="943a3-112">Cuando el programa ya no necesita el generador de objetos o no lo necesita durante un tiempo, se puede liberar el puntero.</span><span class="sxs-lookup"><span data-stu-id="943a3-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="943a3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="943a3-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="943a3-114">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="943a3-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="943a3-115">Crear un OM XPS en blanco</span><span class="sxs-lookup"><span data-stu-id="943a3-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="943a3-116">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="943a3-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="943a3-117">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="943a3-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="943a3-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="943a3-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="943a3-119">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="943a3-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="943a3-120">Packaging</span><span class="sxs-lookup"><span data-stu-id="943a3-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="943a3-121">Referencia de la API de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="943a3-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="943a3-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="943a3-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
