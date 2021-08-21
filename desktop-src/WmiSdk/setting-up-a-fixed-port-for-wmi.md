---
description: WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada. Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especificar un puerto fijo.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configurar un puerto fijo para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050253"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configurar un puerto fijo para WMI

WMI se ejecuta como parte de un host de servicio compartido con puertos asignados a través de DCOM de forma predeterminada. Sin embargo, puede configurar el servicio WMI para que se ejecute como el único proceso en un host independiente y especificar un puerto fijo.

El siguiente procedimiento es una configuración automatizada para permitir que WMI tenga un puerto fijo. El procedimiento usa la herramienta de línea de comandos [**winmgmt.**](winmgmt.md)

**Para configurar un puerto fijo para WMI**

1.  En el símbolo del sistema, escriba **winmgmt -standalonehost.**
2.  Detenga el servicio WMI escribiendo el comando **net stop "Windows Management Instrumentation"** o use el nombre corto **de net stop winmgmt.**
3.  Reinicie el servicio WMI de nuevo en un nuevo host de servicio escribiendo **net start "Windows Management Instrumentation"** o **net start winmgmt**
4.  Establezca un nuevo número de puerto para el servicio WMI; para lo que debe escribir **netsh firewall, agregue TCP 24158 WMIFixedPort.**

Para deshacer los cambios que realice en WMI, escriba **winmgmt /sharedhost** y, a continuación, detenga e inicie de nuevo el servicio winmgmt.

## <a name="examples"></a>Ejemplos

Para obtener un script que configura un puerto fijo para WMI, vea el siguiente ejemplo de código de la Galería [de scripting](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).

o un ejemplo de código de PowerShell que habilita o deshabilita la configuración del puerto WMI, consulte el ejemplo [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) en la Galería de TechNet.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Solución de problemas de conexiones WMI remotas](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hospedaje y seguridad del proveedor](provider-hosting-and-security.md)
</dt> </dl>

 

 



