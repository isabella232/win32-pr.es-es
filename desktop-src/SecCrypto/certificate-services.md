---
description: Los servicios de servidor de certificados, un servicio que se ejecuta en un sistema operativo Windows Server, reciben solicitudes de certificados digitales nuevos a través de transportes como RPC o HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Servicios de servidor de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688099"
---
# <a name="certificate-services"></a>Servicios de servidor de certificados

Los servicios de servidor de [*certificados*](../secgloss/c-gly.md), un servicio que se ejecuta en un sistema operativo Windows Server, reciben solicitudes de certificados digitales nuevos a través de transportes como RPC o http. Comprueba cada solicitud según las directivas personalizadas o específicas del sitio, establece las propiedades opcionales de un certificado que se va a emitir y emite el certificado. Los servicios de Certificate Server permiten a los administradores agregar elementos a una [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL) y publicar CRL firmadas con regularidad.

Los servicios de Certificate Server incluyen interfaces programables para crear compatibilidad con transportes, directivas y propiedades y formatos de certificado adicionales.

En Windows Server 2003, los servicios de servidor de certificados 2,0 se pueden instalar desde el **Panel de control** ; para ello, haga clic en **Agregar o quitar programas** y, a continuación, haga clic en **Agregar o quitar componentes de Windows** para instalar o desinstalar servicios de Certificate Server.

Los conceptos de servicios de Certificate Server se detallan en las secciones siguientes. El contenido está pensado para ayudarle a desarrollar aplicaciones que interactúen con los servicios de Certificate Server.



| Contenido                                                                                                                                                           | Sección                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Descripción de las características de servicios de Certificate Server                                                                                                               | [Características de servicios de Certificate Server](certificate-services-features.md)         |
| Información general sobre la arquitectura de servicios de certificados                                                                                                                     | [Arquitectura de servicios de certificados](certificate-services-architecture.md) |
| Relación entre un certificado, el sujeto del certificado y la [ *clave pública* del sujeto](../secgloss/p-gly.md) | [Certificados y claves públicas](certificates-and-public-keys.md)           |
| Información acerca de las propiedades de la solicitud de certificado                                                                                                              | [Instrucciones de solicitud de certificado](certificate-request-guidelines.md)       |
| Detalles de cómo procesa un certificado los servicios de Certificate Server                                                                                                 | [Acerca de los certificados](about-certificates.md)                               |
| Descripción del proceso de renovación de la [*entidad de certificación*](../secgloss/c-gly.md)        | [Renovación de la entidad de certificación](certification-authority-renewal.md)     |



 

También se incluyen los siguientes temas útiles adicionales.



| Contenido                                                                                                                                             | Sección                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentación sobre el control de inscripción de certificados, que proporciona servicios para crear solicitudes de certificado, incluidas las solicitudes de usuarios de tarjetas inteligentes. | [Control de inscripción de certificados](certificate-enrollment-control.md) |
| Documentación de la interfaz de programación de aplicaciones criptográficas de Microsoft, que proporciona servicios de seguridad basados en criptografía.                | [Cryptography Essentials](cryptography-essentials.md)               |
| Documentación de la tarjeta inteligente, que proporciona servicios para el desarrollo y el uso de sistemas de tarjeta inteligente.                                                   | [Tarjeta inteligente](../secauthn/smart-card-authentication.md)                     |
| Propiedades de nombre de certificados y solicitudes de certificado.                                                                                           | [Propiedades de nombre](name-properties.md)                               |
| Lista y descripciones de las propiedades del certificado [*X. 509*](../secgloss/x-gly.md) .                                  | [Propiedades de certificado](certificate-properties.md)                 |



 

 

 
