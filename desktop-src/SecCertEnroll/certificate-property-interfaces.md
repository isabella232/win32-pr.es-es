---
description: Se pueden usar las siguientes interfaces para crear una propiedad de certificado.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfaces de propiedades de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d0052675436a28438d5f1600a5b0097f8e177a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808335"
---
# <a name="certificate-property-interfaces"></a>Interfaces de propiedades de certificado

Se pueden usar las siguientes interfaces para crear una propiedad de certificado.



| Interfaz                                                                          | Descripción                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Administrar una colección de objetos [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) .                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Asocia una propiedad externa a un certificado.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Representa una propiedad de certificado que identifica si se ha archivado un certificado.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Representa un hash SHA-1 de una clave privada cifrada enviada a una entidad de certificación para el archivado.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Representa una propiedad de certificado que identifica una plantilla que se ha configurado para habilitar la inscripción automática del certificado.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Representa una propiedad de certificado que identifica si se ha realizado una copia de seguridad de un certificado y, en tal caso, la fecha y la hora en que se guardó.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Permite especificar y recuperar una cadena que contiene información descriptiva de un certificado.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Representa una propiedad de certificado que contiene la información del certificado y de la entidad de certificación creada cuando el cliente llama al método [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Representa una propiedad de certificado externo que contiene información sobre un servidor de directiva de inscripción de certificados (CEP) y un servidor de inscripción de certificados (CES).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Permite especificar y recuperar una cadena que contiene el nombre para mostrar de un certificado.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Representa una propiedad de certificado que contiene información sobre una clave privada.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Representa una propiedad de certificado que contiene un hash SHA-1 del nuevo certificado creado cuando se renueva un certificado existente.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa una propiedad de certificado que contiene el nombre del sistema de nombres de dominio (DNS) del equipo en el que se creó la solicitud.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Representa una propiedad de certificado que contiene el nombre del sistema de nombres de dominio (DNS) del equipo en el que se creó la solicitud.                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces CertEnroll](certenroll-interfaces.md)
</dt> </dl>

 

 



