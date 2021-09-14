---
description: Los intermediarios se comunican con las aplicaciones cliente para permitirles enviar solicitudes de certificado y (suponiendo que la solicitud da como resultado un certificado emitido) para descargar el certificado emitido al cliente.
ms.assetid: c696f09e-98d3-4cea-8ea1-cd8f40b74f12
title: intermediarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 040e79abb03bd0363d37fdad79f7311412b0ffe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170989"
---
# <a name="intermediaries"></a>intermediarios

Los intermediarios se comunican con las aplicaciones cliente para [*permitirles*](../secgloss/c-gly.md)enviar solicitudes de certificado y (suponiendo que la solicitud da como resultado un certificado emitido) para descargar el certificado emitido al cliente. Cada protocolo de capa de transporte requiere su propio intermediario.

Microsoft Certificate Services se suministra con un intermediario (las páginas de inscripción web) para HTTP. Otro ejemplo de intermediario es el complemento MMC microsoft Windows certificates (que permite invocar al Asistente para solicitudes de certificado). Si se van a usar otros protocolos de capa de transporte con Certificate Services, un desarrollador puede crear un intermediario para cada protocolo de capa de transporte deseado.

Los intermediarios se comunican con Certificate Services mediante las interfaces [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) proporcionadas por el motor del servidor. El [**método ICertRequest::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) se [](../secgloss/c-gly.md)usa para enviar una solicitud de certificado e [**ICertRequest::GetCertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcertificate) se usa para obtener el certificado emitido resultante. De forma similar, [**se usa ICertConfig::GetConfig para**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig) determinar qué entidad de certificación se puede usar para emitir el certificado.

Un intermediario no depende del lenguaje. Puede ser un programa escrito en C++, Visual Basic, Java, script u otro lenguaje.

Además de recopilar datos del cliente para compilar una solicitud de certificado, un intermediario puede especificar atributos de solicitud. Las solicitudes enviadas [](../secgloss/c-gly.md) a una entidad de certificación que ejecuta el módulo de directivas empresariales deben indicar el tipo de certificado solicitado especificando un atributo "CertificateTemplate" o una extensión de plantilla de certificado en la propia solicitud.

Tenga en cuenta que durante la creación de una solicitud de certificado, los desarrolladores (e intermediarios) son responsables de mantener la confidencialidad de la clave privada. Una vez que se ha puesto en peligro una clave privada (ha perdido su confidencialidad), no sirve de nada.

Las páginas de inscripción web de Servicios de certificados usan las [interfaces](cryptography-interfaces.md)de inscripción de certificados , que protege las claves privadas al generarlas en la estación de trabajo. Además de mantener la confidencialidad de la clave privada, el control de inscripción de certificados permite a un intermediario especificar el proveedor de servicios criptográficos, la especificación de clave, la intensidad de la clave y el algoritmo hash.

El complemento MMC Certificados también usa el control de inscripción de certificados (Xenroll.dll). Sin embargo, cuando las páginas de inscripción web de Servicios de certificados hacen que el recurso control de inscripción de certificados (Xenroll.dll) se descargue en el cliente si es necesario, el complemento MMC Certificados se ejecuta en un entorno donde Xenroll.dll ya es un recurso disponible.

Además de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) e [**ICertConfig,**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)los desarrolladores de intermediarios pueden encontrar útiles las [interfaces](cryptography-interfaces.md) de inscripción de certificados y el [control](certificate-enrollment-control.md) de inscripción de tarjetas inteligentes.

 

 
