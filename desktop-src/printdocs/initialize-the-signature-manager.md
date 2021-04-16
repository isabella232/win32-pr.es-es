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
# <a name="initialize-the-signature-manager"></a>Inicializar el administrador de firmas

En este tema se describe cómo inicializar el administrador de firmas para su uso con un documento XPS.

Antes de usar los siguientes ejemplos de código en el programa, lea la declinación de responsabilidades en [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).

Para usar las características de Windows 7 de Crypto API, defina el símbolo de **\_ \_ \_ \_ \_ campos de cifrado información de OID** como sigue:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



A continuación, cree una instancia de una interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), tal y como se muestra en el ejemplo de código siguiente.


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



La interfaz creada por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) solo puede ser utilizada por un documento XPS, que se debe cargar llamando a [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) antes de llamar a cualquier otro método.

Una vez que se ha creado una instancia de la interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) y se ha cargado un documento XPS, el administrador de firmas está listo para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Firmar un documento](sign-a-document.md)
</dt> <dt>

[Agregar una solicitud de firma a un documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Comprobar las firmas del documento](verify-document-signatures.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Errores de la API de firma digital XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errores de documento XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
