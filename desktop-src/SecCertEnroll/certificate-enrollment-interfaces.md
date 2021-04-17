---
description: Se pueden usar las siguientes interfaces para inscribir un usuario o un equipo en una jerarquía de certificados.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfaces de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688629"
---
# <a name="certificate-enrollment-interfaces"></a>Interfaces de inscripción de certificados

Se pueden usar las siguientes interfaces para inscribir un usuario o un equipo en una jerarquía de certificados.



| Interfaz                                              | Descripción                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Inscribe un equipo o usuario en una jerarquía de certificados.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Extiende la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para habilitar la inicialización desde una plantilla.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Define métodos que permiten a una aplicación web inscribir un certificado, almacenar credenciales del servidor de directivas en la caché de credenciales y registrar servidores de directivas y servidores de inscripción. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Recupera información detallada del error sobre una transacción de inscripción de certificado.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Interfaz de Protocolo simple de inscripción de equipos X. 509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 




