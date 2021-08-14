---
description: Una entidad de certificación (CA) se encarga de avalar la identidad de usuarios, equipos y organizaciones.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Entidades de certificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5f48c897c74e5f0bf7d4d3b1e21b8f89d33e72cdfa46aefe726f714fbc267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904504"
---
# <a name="certification-authorities"></a>Entidades de certificación

Una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) es responsable de dar fe de la identidad de usuarios, equipos y organizaciones. Las CA autentican una entidad y responden por ella emitiendo un certificado firmado digitalmente. Asimismo, administran, revocan y renuevan certificados.

Una entidad de certificación puede ser pública o privada. Una entidad de certificación pública proporciona servicios de certificación, normalmente por un precio, al público a través de Internet. Una entidad de certificación privada proporciona este servicio a los miembros de una población delimitada, como los empleados de una empresa o miembros de algún otro grupo privado.

Los medios por los que una entidad de certificación autentica a un usuario final varían y van más allá del ámbito de esta documentación. Sin embargo, claramente, los métodos de autenticación varían según el tipo de proveedor. Por ejemplo, una entidad de certificación privada puede establecer la identidad de los usuarios finales haciendo referencia a una lista de grupos, como una base de datos de empleados o Active Directory. Los métodos de autenticación que realiza una entidad de certificación pública suelen ser más complejos y dependen en parte del nivel de garantía que el certificado garantiza.

A medida que crece la población de una infraestructura de clave pública (PKI), puede ser difícil que una sola ENTIDAD de certificación administre eficazmente todos los certificados que ha emitido. La ENTIDAD de certificación puede compensar mediante la autorización de otras CA de la PKI para emitir certificados. La CA inicial se denomina raíz y las CA que autoriza se denominan subordinadas. Las CA subordinadas también pueden designar sus propias subsidiarias dentro de los límites establecidos por la raíz. La estructura resultante se denomina jerarquía de certificados. Los certificados emitidos a las CA inferiores de la jerarquía contienen suficientes certificados para hacer un seguimiento de una ruta de acceso a la raíz. Esto se denomina cadena de certificados.

El término entidad de certificación puede hacer referencia tanto a la organización que busca la identidad de un usuario final como al servidor utilizado por la organización para emitir y administrar certificados. Un Windows servidor se puede configurar para que actúe como un servidor de CA y esta documentación normalmente hace referencia al servidor cuando se usa el término CA.

La API de inscripción de certificados interactúa con una entidad de certificación principalmente mediante el [**objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) El [**método Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) de este objeto puede codificar automáticamente una solicitud de certificado, enviarla a la entidad de certificación e instalar el certificado emitido. También puede usar un objeto **IX509Enrollment** inicializado para la inscripción fuera de banda o para la inscripción retrasada. Además, puede usar el objeto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) para supervisar el estado de inscripción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 
