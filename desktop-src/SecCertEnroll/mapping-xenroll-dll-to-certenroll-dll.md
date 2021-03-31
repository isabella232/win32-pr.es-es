---
description: La biblioteca de Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Asignación Xenroll.dll a CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815771"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Asignación Xenroll.dll a CertEnroll.dll

Antes de Windows Vista, el control de inscripción de certificados se implementaba en Xenroll.dll. La biblioteca de Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.

XENROLL intentó implementar dos conjuntos paralelos de interfaces. [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)y [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) eran compatibles con la automatización y eran compatibles con los lenguajes de scripting. Las interfaces correspondientes ([**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)y [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)) no se pudieron incluir en el script, pero eran más cómodas para los programadores de C++. A medida que evolucionen, los dos conjuntos de interfaces no estaban sincronizados. En concreto, el conjunto de interfaces duales representadas más recientemente por **ICEnroll4** define solo un subconjunto de la funcionalidad definida por **IEnroll4**.

CertEnroll.dll implementa un conjunto mayor y más estructurado de interfaces COM conformes a automatización. En los temas siguientes se describe cómo se asignan Xenroll.dll a CertEnroll.dll para distintos tipos de funcionalidad.

-   [Funciones de solicitud de certificado](certificate-request-functions.md)
-   [Funciones de respuesta de certificado](certificate-response-functions.md)
-   [Funciones de atributo](attribute-functions.md)
-   [Funciones de extensión](extension-functions.md)
-   [Funciones de propiedad externa](external-property-functions.md)
-   [Funciones de clave pública y privada](private-and-public-key-functions.md)
-   [Funciones de proveedor de servicios criptográficos](cryptographic-service-provider-functions.md)
-   [Funciones del almacén de certificados](certificate-store-functions.md)
-   [Funciones de intercambio de información personal](personal-information-exchange-functions.md)
-   [Funciones auxiliares](helper-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
