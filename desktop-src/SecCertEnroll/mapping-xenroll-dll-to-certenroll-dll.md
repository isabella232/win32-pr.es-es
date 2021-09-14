---
description: La biblioteca Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Asignación Xenroll.dll a CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171218"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Asignación Xenroll.dll a CertEnroll.dll

Antes de Windows Vista, el control de inscripción de certificados se implementó en Xenroll.dll. La biblioteca Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.

Xenroll intentó implementar dos conjuntos paralelos de interfaces. [**ICEnroll,**](/windows/desktop/api/xenroll/nn-xenroll-icenroll) [**ICEnroll2,**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2) [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)y [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) eran compatibles con Automation y compatibles con lenguajes de scripting. Las interfaces correspondientes,[**IEnroll,**](/windows/desktop/api/xenroll/nn-xenroll-ienroll) [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4,**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)no se pudieron incluir en scripts, pero eran más convenientes para los programadores de C++. A medida que evolucionaban, los dos conjuntos de interfaces no permanecen sincronizados. En concreto, el conjunto de interfaces duales representadas más recientemente por **ICEnroll4** define solo un subconjunto de la funcionalidad definida por **IEnroll4**.

CertEnroll.dll implementa un conjunto más grande y estructurado de interfaces COM compatibles con Automation. En los temas siguientes se describe Xenroll.dll asignación a CertEnroll.dll para diferentes tipos de funcionalidad.

-   [Funciones de solicitud de certificado](certificate-request-functions.md)
-   [Funciones de respuesta de certificado](certificate-response-functions.md)
-   [Funciones de atributo](attribute-functions.md)
-   [Funciones de extensión](extension-functions.md)
-   [Funciones de propiedad externas](external-property-functions.md)
-   [Funciones de clave privada y pública](private-and-public-key-functions.md)
-   [Funciones del proveedor de servicios criptográficos](cryptographic-service-provider-functions.md)
-   [Funciones del almacén de certificados](certificate-store-functions.md)
-   [Funciones de información Exchange personales](personal-information-exchange-functions.md)
-   [Funciones auxiliares](helper-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
