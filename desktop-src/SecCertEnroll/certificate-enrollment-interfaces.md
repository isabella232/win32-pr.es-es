---
description: Las interfaces siguientes se pueden usar para inscribir un usuario o un equipo en una jerarquía de certificados.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb71c1240791e26781797b547b0a62aaad1612a2bce06738cecfa02c8173b215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902746"
---
# <a name="certificate-enrollment-interfaces"></a>Interfaces de inscripción de certificados

Las interfaces siguientes se pueden usar para inscribir un usuario o un equipo en una jerarquía de certificados.



| Interfaz                                              | Descripción                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Inserción**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Inscribe un equipo o usuario en una jerarquía de certificados.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Extiende la interfaz [**IX509Enrollment para**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) habilitar la inicialización desde una plantilla.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Define métodos que permiten a una aplicación web inscribir un certificado, almacenar las credenciales del servidor de directivas en la caché de credenciales y registrar servidores de directivas y servidores de inscripción. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Recupera información de error detallada sobre una transacción de inscripción de certificados.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Interfaz del protocolo de inscripción de equipos simple X.509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 




