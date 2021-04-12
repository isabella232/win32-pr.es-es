---
title: Proporcionar permisos de usuario para dispositivos de grabación de multimedia
description: De forma predeterminada, tanto Windows Vista como Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios registrados directamente en el equipo (usuarios intermedios).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104279725"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Proporcionar permisos de usuario para dispositivos de grabación de multimedia

De forma predeterminada, tanto Windows Vista como Windows Server 2008 conceden acceso de lectura y escritura a los administradores y usuarios registrados directamente en el equipo (usuarios intermedios). Sin embargo, en Windows XP y Windows Server 2003, un administrador debe conceder a estos dispositivos privilegios de lectura y escritura para otros grupos de usuarios.

Un administrador puede ajustar permisos específicos del dispositivo para usuarios avanzados y usuarios interactivos.

Para llegar al panel de permisos de grupo adecuado en Windows XP, haga clic en **Inicio**, haga clic en **Ejecutar**, escriba **gpedit. msc** y, a continuación, haga clic en **Aceptar**. En la interfaz de directiva de grupo, expanda **configuración del equipo**, **configuración de Windows**, **configuración de seguridad**, **Directivas locales** y, a continuación, haga doble clic en **Opciones de seguridad**.

![Captura de pantalla que muestra la ventana ' directiva de grupo ' con una directiva seleccionada en el panel ' Directiva '.](images/gpolpanel.jpg)

En este panel, el administrador debe especificar la configuración de dos opciones de dispositivo para proporcionar los permisos de grupo necesarios:

-   Establecer "dispositivos: restringir el acceso a CD-ROM solo al usuario con sesión iniciada localmente" en **habilitado**
-   Establezca "dispositivos: permitidos para formatear y expulsar medios extraíbles" a **administradores y usuarios avanzados**. También es posible emular los permisos de Windows Vista si se establece esta opción en **administradores y usuarios interactivos**.

Aunque una interfaz de usuario específica no existe en Windows XP o Windows Server 2003 para el uso de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), es posible usar estas API para conceder permisos de dispositivo a los grupos de usuarios personalizados. Por ejemplo, una llamada a **SetSecurityInfo** concederá permisos a los grupos de usuarios. Los cambios de permisos con esta API son temporales y no se conservarán durante un reinicio. Sin embargo, al llamar a [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) se implementarán los cambios de permisos en el registro, que se conservarán en un reinicio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar IMAPi](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 