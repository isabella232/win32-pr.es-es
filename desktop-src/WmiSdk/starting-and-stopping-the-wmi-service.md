---
description: WMI se ejecuta como un servicio con el nombre para mostrar &\# 0034;Windows Management Instrumentation&0034; y el nombre del servicio \# \# &0034;winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Iniciar y detener el servicio WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a60d6ed17c6a5524af2a9bb54f386a325f63c10
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880244"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Iniciar y detener el servicio WMI

WMI se ejecuta como un servicio con el nombre para mostrar "Windows Management Instrumentation" y el nombre de servicio "winmgmt". WMI se ejecuta automáticamente al iniciar el sistema en la cuenta LocalSystem. Si WMI no se está ejecutando, se inicia automáticamente cuando la primera aplicación de administración o script solicita la conexión a un espacio de nombres WMI.

Otros servicios dependen del servicio WMI, en función de la versión del sistema operativo que esté ejecutando el sistema.

## <a name="starting-winmgmt-service"></a>Inicio del servicio Winmgmt

En el procedimiento siguiente se describe cómo iniciar el servicio WMI.

**Para iniciar el servicio Winmgmt**

1.  En un símbolo del sistema, escriba **el modificador**   \[ */ &lt; &gt;* net start winmgmt \] .

    Para obtener más información sobre los modificadores que están disponibles, vea [winmgmt](winmgmt.md). Use la cuenta de administrador integrada o una cuenta del grupo Administradores que se ejecuta con derechos elevados para iniciar el servicio WMI. Para obtener más información, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

2.  Otros servicios que dependen del servicio WMI, como el host del Agente SMS o Windows Firewall, no se reiniciarán automáticamente.

## <a name="stopping-winmgmt-service"></a>Detención del servicio Winmgmt

En el procedimiento siguiente se describe cómo detener el servicio WMI.

**Para detener el servicio Winmgmt**

1.  En un símbolo del sistema, escriba **net stop winmgmt**.

2.  Otros servicios que dependen del servicio WMI también se detienen, como el host del agente de SMS o Windows firewall.

## <a name="examples"></a>Ejemplos

La Galería de TechNet contiene el [script watchdog](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)del servicio WMI , que describe cómo apagar y reiniciar mediante programación el servicio winmgmt con PowerShell.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de wmi Command-Line herramientas](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



