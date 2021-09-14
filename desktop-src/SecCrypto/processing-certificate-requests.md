---
description: Explica cómo Certificate Services procesa las solicitudes de certificado.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Procesamiento de solicitudes de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170866"
---
# <a name="processing-certificate-requests"></a>Procesamiento de solicitudes de certificado

Servicios de certificados realiza los pasos siguientes al procesar una [*solicitud de certificado*](../secgloss/c-gly.md):

1.  Recepción de solicitudes.

    El [*cliente envía*](../secgloss/c-gly.md) la solicitud de certificado a una aplicación intermediaria, que la da formato a una solicitud de formato PKCS 10 y la envía al motor de \# servidor.

2.  Solicitar aprobación.

    El motor de servidor llama al módulo [de](policy-modules.md)directivas , que consulta las propiedades de solicitud, decide si la solicitud está autorizada o no y establece propiedades de certificado opcionales.

3.  Formación de certificados.

    Si se aprueba la solicitud, el motor del servidor toma la solicitud y las propiedades solicitadas por el módulo de directivas, y compila un certificado completo.

4.  Publicación de certificados.

    El motor de servidor almacena el certificado completado en la base de datos de Servicios de certificados y notifica a la aplicación intermediaria el estado de la solicitud. Si el [módulo de salida](exit-modules.md) lo ha solicitado, el motor del servidor le notificará de un evento de emisión de certificados. Esto permite que el módulo de salida realice más operaciones, como la publicación del certificado en un repositorio de certificados externo (por ejemplo, un servicio de directorio). Mientras tanto, el intermediario obtiene el certificado publicado de Servicios de certificados y lo vuelve a pasar al cliente.

En la ilustración siguiente se muestra cómo [*los servicios de*](../secgloss/c-gly.md) certificado procesan una solicitud de certificado.

![procesar una solicitud de certificado](images/certflow.png)

 

 
