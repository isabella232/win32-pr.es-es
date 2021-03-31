---
description: Una entidad de certificación (CA) se encarga de avalar la identidad de usuarios, equipos y organizaciones.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Entidades de certificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911605"
---
# <a name="certification-authorities"></a>Entidades de certificación

Una [*entidad de certificación*](/windows/desktop/SecGloss/c-gly) (CA) es responsable de atestiguar la identidad de usuarios, equipos y organizaciones. Las CA autentican una entidad y responden por ella emitiendo un certificado firmado digitalmente. Asimismo, administran, revocan y renuevan certificados.

Una CA puede ser pública o privada. Una CA pública proporciona servicios de certificación, normalmente por una cuota, al público a través de Internet. Una CA privada proporciona este servicio a los miembros de un rellenado delimitado, como los empleados de una empresa o los miembros de algún otro grupo privado.

La forma en que una entidad de certificación autentica a un usuario final varía y queda fuera del ámbito de esta documentación. Sin embargo, los métodos de autenticación varían claramente según el tipo de proveedor. Por ejemplo, una CA privada puede establecer la identidad de los usuarios finales mediante una referencia a una lista de grupos, como una base de datos de empleados o un Active Directory. Los métodos de autenticación que realiza una entidad de certificación pública suelen ser más complejos y dependen en parte del nivel de garantía prometido por el certificado.

A medida que crece la población de una infraestructura de clave pública (PKI), puede resultar difícil para una sola CA administrar de forma eficaz todos los certificados que ha emitido. La entidad de certificación puede compensar mediante la autorización de otras CA de la PKI para emitir certificados. La entidad de certificación inicial se denomina raíz y las entidades de certificación que autoriza se denominan subordinadas. Las CA subordinadas también pueden designar sus propias subsidiarias dentro de los límites establecidos por la raíz. La estructura resultante se denomina jerarquía de certificados. Los certificados emitidos para las CA inferiores de la jerarquía contienen suficientes certificados para hacer un seguimiento de una ruta de acceso a la raíz. Esto se denomina cadena de certificados.

El término entidad de certificación puede hacer referencia a la organización que garantiza la identidad de un usuario final y el servidor usado por la organización para emitir y administrar certificados. Un servidor de Windows se puede configurar para que actúe como servidor de CA y esta documentación normalmente hace referencia al servidor cuando se usa el término CA.

La API de inscripción de certificados interactúa principalmente con una entidad de certificación mediante el objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . El método [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) de este objeto puede codificar automáticamente una solicitud de certificado, enviarla a la CA e instalar el certificado emitido. También puede usar un objeto **IX509Enrollment** inicializado para la inscripción fuera de banda o para la inscripción diferida. Además, puede usar el objeto [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) para supervisar el estado de la inscripción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 
