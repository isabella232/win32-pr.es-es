---
description: En esta sección se proporciona información general sobre la API de firma digital XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Acerca de la API de firma digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156448"
---
# <a name="about-xps-digital-signature-api"></a>Acerca de la API de firma digital XPS

Los documentos XPS pueden tener firmas digitales para permitir que los usuarios firmen un documento, comprobar la identidad del firmante e indicar si un documento XPS ha cambiado desde que se firmó. Una aplicación nativa de Windows puede usar las interfaces de la API de firma digital XPS para realizar operaciones de firma digital en un documento XPS. En esta sección se proporciona información general sobre la API de firma digital XPS.

La interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) administra las operaciones de firma digital en un documento XPS. Para que una aplicación pueda acceder a las firmas digitales de un documento XPS, la aplicación debe llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un **IXpsSignatureManager** y, a continuación, llamar a [**IXpsSignatureManager:: LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) o [**IXpsSignatureManager:: LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) para cargar el documento XPS. Para obtener más información acerca de este proceso de inicialización, consulte [inicializar el administrador de firmas](initialize-the-signature-manager.md).

Una vez que se ha cargado un documento XPS en una interfaz [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , una aplicación puede acceder a las firmas digitales del documento y a las solicitudes de firma digital. Puede tener acceso a las firmas digitales mediante una interfaz [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) desde la interfaz [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) del administrador de firmas. Una aplicación también puede Agregar y quitar interfaces de **IXpsSignature** de la colección. Se tiene acceso a las solicitudes de firma mediante [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) , que se recopilan en una interfaz [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) . **IXpsSignatureRequestCollection** forma parte de una interfaz [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) que se recopila en el [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) del administrador de firmas.

Las aplicaciones pueden usar el [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) del administrador de firmas para obtener acceso y establecer las opciones de firma digital.

Para obtener ejemplos de cómo obtener acceso a las firmas digitales de un documento XPS, vea [tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de firma digital XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Referencia de la API de firma digital XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Estándar ECMA-376, formatos de archivo XML abierto de Office](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
