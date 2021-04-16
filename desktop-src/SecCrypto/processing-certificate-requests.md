---
description: Explica cómo los servicios de Certificate Server procesan las solicitudes de certificados.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Procesar solicitudes de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557039"
---
# <a name="processing-certificate-requests"></a>Procesar solicitudes de certificado

Servicios de Certificate Server realiza los siguientes pasos al procesar una [*solicitud de certificado*](../secgloss/c-gly.md):

1.  Solicitar recepción.

    El cliente envía la [*solicitud de certificado*](../secgloss/c-gly.md) a una aplicación intermediario, que la da formato a una solicitud de \# formato PKCS 10 y la envía al motor del servidor.

2.  Solicitar aprobación.

    El motor del servidor llama al [módulo de directivas](policy-modules.md)de, que consulta las propiedades de la solicitud, decide si la solicitud está autorizada o no, y establece las propiedades opcionales del certificado.

3.  Formación de certificados.

    Si se aprueba la solicitud, el motor del servidor toma la solicitud y todas las propiedades solicitadas por el módulo de directivas, y crea un certificado completo.

4.  Publicación de certificado.

    El motor del servidor almacena el certificado completado en la base de datos de servicios de certificados y notifica a la aplicación intermediario el estado de la solicitud. Si el [módulo de salida](exit-modules.md) lo ha solicitado, el motor del servidor le notificará un evento de emisión de certificado. Esto permite que el módulo de salida realice otras operaciones, como publicar el certificado en un repositorio de certificados externos (por ejemplo, un servicio de directorio). Mientras tanto, el intermediario obtiene el certificado publicado de los servicios de servidor de certificados y lo devuelve al cliente.

La siguiente ilustración muestra el modo en que los servicios de Certificate Server procesan una [*solicitud de certificado*](../secgloss/c-gly.md) .

![procesar una solicitud de certificado](images/certflow.png)

 

 
