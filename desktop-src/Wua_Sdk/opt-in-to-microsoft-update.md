---
description: Puede optar por un equipo en el servicio de Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In a Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153823"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In a Microsoft Update

Puede optar por un equipo en el servicio de Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.

En el ejemplo de scripting de este tema se muestra cómo usar Windows Update Agent (WUA) para registrar el servicio de Microsoft Update con Actualizaciones automáticas. Como alternativa, para registrar el servicio, el usuario puede visitar Microsoft Update.

Antes de intentar ejecutar este ejemplo, compruebe que la versión de WUA instalada en el equipo sea la versión 7.0.6000 o una versión posterior. Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea [determinar la versión actual de WUA](determining-the-current-version-of-wua.md).

## <a name="example"></a>Ejemplo

En el ejemplo de scripting siguiente se muestra cómo utilizar el agente de Windows Update (WUA) para registrar el servicio de Microsoft Update con Actualizaciones automáticas. El ejemplo permite el procesamiento diferido o sin conexión si es necesario.

> [!IMPORTANT]
> Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas. Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



En versiones anteriores de WUA (una versión de WUA mínima de 7.0.6000), puede simplificar el proceso de participación mediante una configuración del registro. Una vez configurados los valores y la clave del registro, el proceso de participación en el Microsoft Update se produce la próxima vez que WUA realiza una búsqueda. El proceso de participación puede ser desencadenado por Actualizaciones automáticas o por un llamador de la API.

Por ejemplo, la ruta de acceso completa de la clave del registro y los valores que se establecen para el proceso de participación son los siguientes:

**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = mi aplicación

**RegisterWithAU** = 1

> [!Note]
>
> La clave del registro se respeta una vez solo cuando WUA se actualiza desde una versión anterior a la versión 7.0.6000 a la versión 7.0.6000 o a una versión posterior. Recomendamos que se sobrescriban los valores del registro existentes, ya que si se sobrescriben los valores, se puede cambiar el resultado de una solicitud de registro del servicio anterior.
>
> La creación de esta clave del registro requiere credenciales administrativas. En Windows Vista, el autor de la llamada debe crear la clave del registro en un proceso con privilegios elevados.

 

 

 



