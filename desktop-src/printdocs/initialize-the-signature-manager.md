---
description: En este tema se describe cómo inicializar el administrador de firmas para usarlo con un documento XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Inicializar el Administrador de firmas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9a9f960c639e20c6c7d4debbfd2276553d3ba90b7af083d39a97f887ee81ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948775"
---
# <a name="initialize-the-signature-manager"></a>Inicializar el Administrador de firmas

En este tema se describe cómo inicializar el administrador de firmas para usarlo con un documento XPS.

Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Para usar las Windows 7 características de Crypto API, defina el símbolo **\_ CRYPT OID \_ INFO HAS EXTRA \_ \_ \_ FIELDS** como se muestra a continuación:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



A continuación, cree una instancia de [**una interfaz IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) mediante una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), como se muestra en el ejemplo de código siguiente.


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



Solo un documento XPS puede usar la interfaz de la que [**cocreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) que debe cargarse llamando a [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) antes de llamar a cualquier otro método.

Después de crear una instancia de la interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) y de cargar un documento XPS, el administrador de firmas está listo para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Firmar un documento](sign-a-document.md)
</dt> <dt>

[Agregar una solicitud de firma a un documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Comprobar firmas de documento](verify-document-signatures.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Errores de API de firma digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errores del documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
