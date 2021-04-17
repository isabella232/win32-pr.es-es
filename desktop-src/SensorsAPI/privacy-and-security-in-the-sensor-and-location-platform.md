---
description: El sensor de Windows y la plataforma de ubicación incluyen la configuración de privacidad para ayudar a proteger la información personal de los usuarios.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacidad y seguridad en el sensor de Windows y la plataforma de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666370"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>Privacidad y seguridad en el sensor de Windows y la plataforma de ubicación

El sensor de Windows y la plataforma de ubicación incluyen la configuración de privacidad para ayudar a proteger la información personal de los usuarios.

La plataforma ayuda a garantizar que los datos del sensor permanecen privados, cuando se requiere privacidad, de las siguientes maneras:

-   De forma predeterminada, los sensores están desactivados. Dado que el diseño de la plataforma presupone que cualquier sensor puede proporcionar datos personales, cada sensor está deshabilitado hasta que el usuario proporciona consentimiento explícito para acceder a los datos del sensor.
-   Windows proporciona mensajes de divulgación y contenido de ayuda para el usuario. Este contenido ayuda a los usuarios a entender cómo los sensores pueden afectar a la privacidad de sus datos personales y ayudan a los usuarios a tomar decisiones informadas.
-   El suministro de permisos para un sensor requiere derechos de administrador.
-   Cuando está habilitada, un dispositivo de sensor funciona para todos los programas que se ejecutan en una cuenta de usuario determinada (o para todas las cuentas de usuario). Esto incluye a los usuarios y servicios no interactivos, como ASPNET o SYSTEM. Por ejemplo, si habilita un sensor GPS para su cuenta de usuario, solo los programas que se ejecutan en su cuenta de usuario tienen acceso al GPS. Si habilita el GPS para todos los usuarios, cualquier programa que se ejecute en cualquier cuenta de usuario tendrá acceso al GPS.
-   Los programas que utilizan sensores pueden llamar a un método para abrir un cuadro de diálogo de sistema que solicita a los usuarios que habiliten los dispositivos de sensor necesarios. Esta característica facilita a los desarrolladores y usuarios la seguridad de que los sensores funcionan cuando los programas los necesiten, a la vez que se mantiene el control del usuario de la divulgación de los datos del sensor.
-   Los controladores de sensor usan un objeto especial que procesa todas las solicitudes de e/s. Este objeto garantiza que solo los programas que tienen permiso de usuario pueden tener acceso a los datos del sensor.

 

 



