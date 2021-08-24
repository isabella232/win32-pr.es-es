---
description: En esta sección se proporciona información general sobre XPS Digital Signature API.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Acerca de XPS Digital Signature API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfbd6000df56d96afbc86a3cd0111c02a128c3c23c0d0de59717da5f4e9ac6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950945"
---
# <a name="about-xps-digital-signature-api"></a>Acerca de XPS Digital Signature API

Los documentos XPS pueden tener firmas digitales para permitir a los usuarios firmar un documento, comprobar la identidad del firmante e indicar si un documento XPS ha cambiado desde que se firmó. Una aplicación Windows nativa puede usar las interfaces de XPS Digital Signature API para realizar operaciones de firma digital en un documento XPS. En esta sección se proporciona información general sobre XPS Digital Signature API.

La [**interfaz IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) administra las operaciones de firma digital en un documento XPS. Para que una aplicación pueda acceder a las firmas digitales de un documento XPS, la aplicación debe llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un **IXpsSignatureManager** y, a continuación, llamar a [**IXpsSignatureManager::LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**IXpsSignatureManager::LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) para cargar el documento XPS. Para obtener más información sobre este proceso de inicialización, vea [Inicializar el Administrador de firmas](initialize-the-signature-manager.md).

Después de cargar un documento XPS en una interfaz [**IXpsSignatureManager,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) una aplicación puede acceder a las firmas digitales y las solicitudes de firma digital del documento. Puede acceder a las firmas digitales mediante una [**interfaz IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) desde la interfaz [**IXpsSignatureCollection del**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) administrador de firmas. Una aplicación también puede agregar y quitar **interfaces IXpsSignature** de la colección. Se accede a las solicitudes de firma mediante [**IXpsSignatureRequest,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) que se recopilan en una [**interfaz IXpsSignatureRequestCollection.**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) **IXpsSignatureRequestCollection** forma parte de una interfaz [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) que se recopila en [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) del administrador de firmas.

Las aplicaciones pueden usar [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) del administrador de firmas para acceder a las opciones de firma digital y establecerla.

Para obtener ejemplos de cómo acceder a las firmas digitales de un documento XPS, vea Tareas comunes de programación de [firmas digitales](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de firma digital XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Referencia de API de firma digital XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[ECMA-376 estándar, Office formatos de archivo OPEN XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
