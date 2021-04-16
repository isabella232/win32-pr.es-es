---
description: Los intermediarios se comunican con las aplicaciones cliente para permitirles enviar solicitudes de certificado y (suponiendo que la solicitud dé como resultado un certificado emitido) para descargar el certificado emitido al cliente.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: intermediarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670061"
---
# <a name="intermediaries"></a>intermediarios

Los intermediarios se comunican con las aplicaciones cliente para permitirles enviar [*solicitudes de certificado*](../secgloss/c-gly.md)y (suponiendo que la solicitud dé como resultado un certificado emitido) para descargar el certificado emitido al cliente. Cada protocolo de nivel de transporte requiere su propio intermediario.

Los servicios de Certificate Server de Microsoft se distribuyen con un intermediario (las páginas de inscripción Web) para HTTP. Otro ejemplo de intermediario es el complemento MMC certificados de Microsoft Windows (que permite invocar el Asistente para solicitud de certificados). Si se van a utilizar otros protocolos de capa de transporte con los servicios de Certificate Server, un programador puede crear un intermediario para cada protocolo de capa de transporte deseado.

Los intermediarios se comunican con los servicios de Certificate Server mediante las interfaces [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) proporcionadas por el motor de servidor. El método [**ICertRequest:: submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) se usa para enviar una [*solicitud de certificado*](../secgloss/c-gly.md)y [**ICertRequest:: GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) se utiliza para obtener el certificado emitido resultante. De forma similar, [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) se usa para determinar qué entidad de certificación se puede usar para emitir el certificado.

Un intermediario no depende del idioma. Puede tratarse de un programa escrito en C++, Visual Basic, Java, script u otro lenguaje.

Además de recopilar datos del cliente para crear una solicitud de certificado, un intermediario puede especificar atributos de solicitud. Las solicitudes enviadas a una [*entidad de certificación*](../secgloss/c-gly.md) que ejecute el módulo de directivas empresariales deben indicar el tipo de certificado solicitado especificando un atributo "CertificateTemplate" o una extensión de plantilla de certificado en la propia solicitud.

Tenga en cuenta que durante la creación de una solicitud de certificado, los desarrolladores (y los intermediarios) son responsables de mantener la confidencialidad de la clave privada. Una vez que una clave privada se ha puesto en peligro (se ha perdido su confidencialidad), no sirve de nada.

Las páginas de inscripción Web de servicios de Certificate Server utilizan las [interfaces de inscripción de certificados](cryptography-interfaces.md), que protege las claves privadas mediante su generación en la estación de trabajo. Además de mantener la confidencialidad de la clave privada, el control de inscripción de certificados permite a un intermediario especificar el proveedor de servicios de cifrado, la especificación de claves, el nivel de clave y el algoritmo hash.

El complemento MMC de certificados también usa el control de inscripción de certificados (Xenroll.dll). Sin embargo, si las páginas de inscripción Web de servicios de Certificate Server hacen que el recurso de control de inscripción de certificados (Xenroll.dll) se descargue en el cliente, si es necesario, el complemento MMC de certificados se ejecuta en un entorno en el que Xenroll.dll ya es un recurso disponible.

Además de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) y [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig), los desarrolladores de intermediarios pueden encontrar las interfaces de [inscripción de certificados](cryptography-interfaces.md) y el control de [inscripción de tarjeta inteligente](certificate-enrollment-control.md) para que resulte útil.

 

 
