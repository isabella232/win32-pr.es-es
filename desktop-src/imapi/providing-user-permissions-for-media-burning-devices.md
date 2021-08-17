---
title: Proporcionar permisos de usuario para dispositivos de protección de medios
description: De forma predeterminada, Windows Vista y Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios que han iniciado sesión directamente en la máquina (usuarios intermedios).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758571"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Proporcionar permisos de usuario para dispositivos de protección de medios

De forma predeterminada, Windows Vista y Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios que han iniciado sesión directamente en la máquina (usuarios intermedios). Sin embargo, en Windows XP y Windows Server 2003, un administrador debe conceder estos privilegios de lectura y escritura de dispositivos a otros grupos de usuarios.

Un administrador puede ajustar permisos específicos relacionados con el dispositivo para usuarios avanzados y usuarios interactivos.

Para llegar al panel de permisos de grupo adecuado en Windows XP, haga clic en Iniciar **,** haga clic en Ejecutar **,** escriba **gpedit.msc** y, a continuación, haga clic **en Aceptar.** En la interfaz directiva de grupo, expanda Configuración del equipo **,** expanda Windows Configuración **,** expanda Seguridad Configuración **,** expanda Directivas locales **y** haga doble clic en **Opciones de seguridad**.

![Captura de pantalla que muestra la ventana "directiva de grupo" con una directiva seleccionada en el panel "Directiva".](images/gpolpanel.jpg)

En este panel, un administrador debe especificar la configuración de dos opciones de dispositivo para proporcionar los permisos de grupo necesarios:

-   Establezca "Devices: Restrict CD-ROM access to locally logged-on user only" (Dispositivos: restringir el acceso de CD-ROM solo al usuario que inició sesión localmente) en **Habilitado.**
-   Establezca "Dispositivos: permitido para dar formato y expulsar medios **extraíbles" en Administradores y usuarios avanzados.** También es posible emular los permisos Windows Vista estableciendo esta opción en **Administradores y usuarios interactivos.**

Aunque no existe una interfaz de usuario específica en Windows XP o Windows Server 2003 para usar [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty,](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)es posible usar estas API para conceder permisos de dispositivo a grupos de usuarios personalizados. Por ejemplo, una llamada a **SetSecurityInfo** concederá permisos a los grupos de usuarios. Los cambios de permisos con esta API son temporales y no se conservarán durante un reinicio. Sin embargo, al llamar a [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) se implementarán los cambios de permisos en el Registro, que se conservarán durante un reinicio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de IMAPI](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 