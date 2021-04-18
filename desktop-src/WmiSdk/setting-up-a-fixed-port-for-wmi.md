---
description: WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada. Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especifique un puerto fijo.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configuración de un puerto fijo para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717035"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configuración de un puerto fijo para WMI

WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada. Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especifique un puerto fijo.

El siguiente procedimiento es una configuración automatizada que permite a WMI tener un puerto fijo. El procedimiento usa la herramienta de línea de comandos [**WinMgmt**](winmgmt.md) .

**Para configurar un puerto fijo para WMI**

1.  En el símbolo del sistema, escriba **WinMgmt-standalonehost**
2.  Detenga el servicio WMI escribiendo el comando **net stop "instrumental de administración de Windows"** o use el nombre corto de **net stop WinMgmt**
3.  Vuelva a reiniciar el servicio WMI en un nuevo host de servicio escribiendo **net start "instrumental de administración de Windows"** o **net start WinMgmt**
4.  Establezca un nuevo número de puerto para el servicio WMI escribiendo **netsh firewall Add PORTOPENING TCP 24158 WMIFixedPort**

Para deshacer los cambios que realice en WMI, escriba **WinMgmt/sharedhost** y, a continuación, detenga e inicie de nuevo el servicio WinMgmt.

## <a name="examples"></a>Ejemplos

Para obtener un script que configure un puerto fijo para WMI, vea el siguiente ejemplo de [código](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )de la galería de scripting.

o un ejemplo de código de PowerShell que habilita o deshabilita la configuración del puerto WMI, vea el ejemplo [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) en la galería de TechNet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Solución de problemas de conexiones WMI remotas](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hospedaje y seguridad de proveedores](provider-hosting-and-security.md)
</dt> </dl>

 

 



