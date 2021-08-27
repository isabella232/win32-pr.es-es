---
description: Servicios de certificados, un servicio que se ejecuta en un sistema operativo de servidor Windows, recibe solicitudes de nuevos certificados digitales a través de transportes como RPC o HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Servicios de servidor de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaac2e1ee01b588beedbe2e632e52ef41459a885782a7975e460182f8a211bef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126855"
---
# <a name="certificate-services"></a>Servicios de servidor de certificados

[*Servicios de*](../secgloss/c-gly.md)certificados , un servicio que se ejecuta en un sistema operativo de servidor Windows, recibe solicitudes de nuevos certificados digitales a través de transportes como RPC o HTTP. Comprueba cada solicitud con directivas personalizadas o específicas del sitio, establece propiedades opcionales para que se emita un certificado y emite el certificado. Servicios de certificados permite a los administradores agregar elementos a una lista de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y publicar CRL firmadas de forma periódica.

Los servicios de certificado incluyen interfaces programables para crear compatibilidad con transportes adicionales, directivas y propiedades y formatos de certificado.

En Windows Server 2003, Certificate Services 2.0 se puede instalar desde  **Panel de control** haciendo clic en Agregar o quitar programas y, a continuación, haciendo clic en Agregar o quitar **componentes de Windows** para instalar o desinstalar Servicios de certificados.

Los conceptos de Servicios de certificados se detallan en las secciones siguientes. El contenido está pensado para ayudarle a desarrollar aplicaciones que interactuarán con Servicios de certificados.



| Content                                                                                                                                                           | Sección                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Descripción de las características de Servicios de certificados                                                                                                               | [Características de Servicios de certificados](certificate-services-features.md)         |
| Introducción a la arquitectura de Servicios de certificados                                                                                                                     | [Arquitectura de Servicios de certificados](certificate-services-architecture.md) |
| Relación entre un certificado, el asunto del certificado y la clave pública [ *del sujeto*](../secgloss/p-gly.md) | [Certificados y claves públicas](certificates-and-public-keys.md)           |
| Información sobre las propiedades de solicitud de certificado                                                                                                              | [Directrices de solicitud de certificado](certificate-request-guidelines.md)       |
| Detalles de cómo certificate services procesa un certificado                                                                                                 | [Acerca de los certificados](about-certificates.md)                               |
| Descripción del proceso de [*renovación de la entidad de*](../secgloss/c-gly.md) certificación        | [Renovación de la entidad de certificación](certification-authority-renewal.md)     |



 

También se incluyen los siguientes temas útiles adicionales.



| Content                                                                                                                                             | Sección                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentación sobre el control de inscripción de certificados, que proporciona servicios para crear solicitudes de certificado, incluidas las solicitudes para los usuarios de tarjetas inteligentes. | [Control de inscripción de certificados](certificate-enrollment-control.md) |
| Documentación sobre la interfaz de programación de aplicaciones criptográficas de Microsoft, que proporciona servicios de seguridad basados en criptografía.                | [Cryptography Essentials](cryptography-essentials.md)               |
| Documentación sobre tarjeta inteligente, que proporciona servicios para desarrollar y usar sistemas de tarjetas inteligentes.                                                   | [Tarjeta inteligente](../secauthn/smart-card-authentication.md)                     |
| Asigne un nombre a las propiedades de los certificados y las solicitudes de certificado.                                                                                           | [Propiedades de nombre](name-properties.md)                               |
| Lista y descripciones de las propiedades del certificado [*X.509.*](../secgloss/x-gly.md)                                  | [Propiedades del certificado](certificate-properties.md)                 |



 

 

 
