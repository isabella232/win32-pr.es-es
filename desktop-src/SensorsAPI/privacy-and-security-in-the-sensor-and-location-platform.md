---
description: La plataforma Windows sensor y ubicación incluye la configuración de privacidad para ayudar a proteger la información personal de los usuarios.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacidad y seguridad en la plataforma Windows sensor y ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068957"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a>Privacidad y seguridad en la plataforma Windows sensor y ubicación

La plataforma Windows sensor y ubicación incluye la configuración de privacidad para ayudar a proteger la información personal de los usuarios.

La plataforma ayuda a garantizar que los datos del sensor permanecen privados, cuando se requiere privacidad, de las maneras siguientes:

-   De forma predeterminada, los sensores están desactivados. Dado que el diseño de la plataforma supone que cualquier sensor puede proporcionar datos personales, cada sensor se deshabilita hasta que el usuario proporciona consentimiento explícito para acceder a los datos del sensor.
-   Windows proporciona mensajes de divulgación y contenido de Ayuda para el usuario. Este contenido ayuda a los usuarios a comprender cómo los sensores pueden afectar a la privacidad de sus datos personales y ayuda a los usuarios a tomar decisiones informadas.
-   Proporcionar permiso para un sensor requiere derechos de administrador.
-   Cuando está habilitado, un dispositivo de sensor funciona para todos los programas que se ejecutan en una cuenta de usuario determinada (o para todas las cuentas de usuario). Esto incluye usuarios y servicios no inactivos, como ASPNET o SYSTEM. Por ejemplo, si habilita un sensor GPS para su cuenta de usuario, solo los programas que se ejecutan en su cuenta de usuario tienen acceso al GPS. Si habilita el GPS para todos los usuarios, cualquier programa que se ejecute en cualquier cuenta de usuario tiene acceso al GPS.
-   Los programas que usan sensores pueden llamar a un método para abrir un cuadro de diálogo del sistema que solicita a los usuarios que habiliten los dispositivos de sensor necesarios. Esta característica facilita a los desarrolladores y usuarios la seguridad de que los sensores funcionan cuando los programas los necesitan, al tiempo que se mantiene el control del usuario de la divulgación de datos del sensor.
-   Los controladores de sensor usan un objeto especial que procesa todas las solicitudes de E/S. Este objeto se asegura de que solo los programas que tienen permiso de usuario pueden acceder a los datos del sensor.

 

 



