---
description: Puede optar por un equipo en el servicio Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In a Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d034f0b224d8170a52ce359589693c601cb9598d716e9663493e8ac99edf2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994285"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In a Microsoft Update

Puede optar por un equipo en el servicio Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.

En el ejemplo de scripting de este tema se muestra cómo usar Windows Update Agent (WUA) para registrar el servicio Microsoft Update con Actualizaciones automáticas. Como alternativa, para registrar el servicio, el usuario puede visitar Microsoft Update.

Antes de intentar ejecutar este ejemplo, compruebe que la versión de WUA instalada en el equipo es la versión 7.0.6000 o una versión posterior. Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea Determinar la [versión actual de WUA.](determining-the-current-version-of-wua.md)

## <a name="example"></a>Ejemplo

En el ejemplo de scripting siguiente se muestra cómo usar Windows Update Agent (WUA) para registrar el servicio Microsoft Update con Actualizaciones automáticas. El ejemplo permite el procesamiento aplazado o sin conexión si es necesario.

> [!IMPORTANT]
> Este script está pensado para mostrar el uso de las API del agente de actualización de Windows y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para solucionar problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API Windows update agent subyacentes).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



En versiones anteriores de WUA (una versión de WUA mínima de 7.0.6000), puede simplificar el proceso de suscripción mediante una configuración del Registro. Una vez configurados la clave y los valores del Registro, Microsoft Update proceso de suscripción se produce la próxima vez que WUA realice una búsqueda. El proceso de suscripción se puede desencadenar mediante un Actualizaciones automáticas o por un llamador de API.

Por ejemplo, la ruta de acceso completa de la clave del Registro y los valores que se van a establecer para el proceso de suscripción son los siguientes:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsUpdate** \\ **PendingServiceRegistration** \\ **7971f918-a847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = Mi aplicación

**RegisterWithAU** = 1

> [!Note]
>
> La clave del Registro solo se respeta una vez cuando WUA se actualiza desde una versión anterior a la 7.0.6000 a la versión 7.0.6000 o a una versión posterior. Se recomienda discrer al sobrescribir los valores del Registro existentes, ya que sobrescribir los valores puede cambiar el resultado de una solicitud de registro de servicio anterior.
>
> La creación de esta clave del Registro requiere credenciales administrativas. Para Windows Vista, el autor de la llamada debe crear la clave del Registro en un proceso con privilegios elevados.

 

 

 



