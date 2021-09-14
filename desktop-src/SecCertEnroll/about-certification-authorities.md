---
description: Una entidad de certificación (CA) se encarga de avalar la identidad de usuarios, equipos y organizaciones.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Entidades de certificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173346"
---
# <a name="certification-authorities"></a>Entidades de certificación

Una [*entidad de*](/windows/desktop/SecGloss/c-gly) certificación (CA) es responsable de dar fe de la identidad de usuarios, equipos y organizaciones. Las CA autentican una entidad y responden por ella emitiendo un certificado firmado digitalmente. Asimismo, administran, revocan y renuevan certificados.

Una entidad de certificación puede ser pública o privada. Una entidad de certificación pública proporciona servicios de certificación, normalmente por un precio, al público a través de Internet. Una entidad de certificación privada proporciona este servicio a los miembros de una población delimitada, como los empleados de una empresa o miembros de algún otro grupo privado.

Los medios por los que una ENTIDAD de certificación autentica a un usuario final varían y están fuera del ámbito de esta documentación. Sin embargo, claramente, los métodos de autenticación varían según el tipo de proveedor. Por ejemplo, una entidad de certificación privada puede establecer la identidad de los usuarios finales haciendo referencia a una lista de grupos, como una base de datos de empleados o Active Directory. Los métodos de autenticación que realiza una CA pública suelen ser más complejos y dependen en parte del nivel de garantía que garantiza el certificado.

A medida que crece la población de una infraestructura de clave pública (PKI), puede ser difícil que una sola CA administre eficazmente todos los certificados que ha emitido. La ENTIDAD de certificación puede compensar mediante la autorización de otras CA de la PKI para emitir certificados. La CA inicial se denomina raíz y las CA que autoriza se denominan subordinadas. Las CA subordinadas también pueden designar sus propias subsidiarias dentro de los límites establecidos por la raíz. La estructura resultante se denomina jerarquía de certificados. Los certificados emitidos a las CA inferiores de la jerarquía contienen suficientes certificados para hacer un seguimiento de una ruta de acceso a la raíz. Esto se denomina cadena de certificados.

El término entidad de certificación puede hacer referencia tanto a la organización que busca la identidad de un usuario final como al servidor utilizado por la organización para emitir y administrar certificados. Un Windows servidor se puede configurar para que actúe como un servidor de CA y esta documentación normalmente hace referencia al servidor cuando se usa el término CA.

La API de inscripción de certificados interactúa con una entidad de certificación principalmente mediante el [**objeto IX509Enrollment.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) El [**método Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) de este objeto puede codificar automáticamente una solicitud de certificado, enviarla a la entidad de certificación e instalar el certificado emitido. También puede usar un objeto **IX509Enrollment** inicializado para la inscripción fuera de banda o para la inscripción retrasada. Además, puede usar el objeto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) para supervisar el estado de inscripción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 
