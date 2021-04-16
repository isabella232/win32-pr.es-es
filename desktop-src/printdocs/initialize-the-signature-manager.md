---
description: En este tema se describe cómo inicializar el administrador de firmas para su uso con un documento XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Inicializar el administrador de firmas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720730"
---
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="5d180-103">Inicializar el administrador de firmas</span><span class="sxs-lookup"><span data-stu-id="5d180-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="5d180-104">En este tema se describe cómo inicializar el administrador de firmas para su uso con un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5d180-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="5d180-105">Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5d180-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="5d180-106">Para usar las características de Windows 7 de Crypto API, defina el símbolo de **\_ \_ \_ \_ \_ campos de cifrado información de OID** como sigue:</span><span class="sxs-lookup"><span data-stu-id="5d180-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="5d180-107">A continuación, cree una instancia de una interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5d180-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



<span data-ttu-id="5d180-108">La interfaz creada por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) solo puede ser utilizada por un documento XPS, que se debe cargar llamando a [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) antes de llamar a cualquier otro método.</span><span class="sxs-lookup"><span data-stu-id="5d180-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="5d180-109">Una vez que se ha creado una instancia de la interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) y se ha cargado un documento XPS, el administrador de firmas está listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="5d180-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d180-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d180-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5d180-111">**Pasos siguientes**</span><span class="sxs-lookup"><span data-stu-id="5d180-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5d180-112">Firmar un documento</span><span class="sxs-lookup"><span data-stu-id="5d180-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="5d180-113">Agregar una solicitud de firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="5d180-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="5d180-114">Comprobar las firmas del documento</span><span class="sxs-lookup"><span data-stu-id="5d180-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="5d180-115">**Se usa en esta sección**</span><span class="sxs-lookup"><span data-stu-id="5d180-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="5d180-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="5d180-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="5d180-117">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="5d180-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="5d180-118">**Para obtener más información**</span><span class="sxs-lookup"><span data-stu-id="5d180-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5d180-119">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="5d180-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="5d180-120">Errores de documento XPS</span><span class="sxs-lookup"><span data-stu-id="5d180-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="5d180-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5d180-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
