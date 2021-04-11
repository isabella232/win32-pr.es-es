---
description: WMI se ejecuta como un servicio con el nombre para mostrar &\# 0034; Instrumental de administración de Windows&\# 0034 y el nombre del servicio &\# 0034; winmgmt&\# 0034;.
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
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276131"
---
# <a name="starting-and-stopping-the-wmi-service"></a>Iniciar y detener el servicio WMI

WMI se ejecuta como un servicio con el nombre para mostrar "Instrumental de administración de Windows" y el nombre de servicio "WinMgmt". WMI se ejecuta automáticamente al iniciar el sistema en la cuenta LocalSystem. Si WMI no se está ejecutando, se inicia automáticamente cuando la primera aplicación de administración o el script solicita la conexión a un espacio de nombres WMI.

Otros servicios dependen del servicio WMI, en función de la versión del sistema operativo que esté ejecutando el sistema.

## <a name="starting-winmgmt-service"></a>Iniciando el servicio WinMgmt

En el procedimiento siguiente se describe cómo iniciar el servicio WMI.

**Para iniciar el servicio WinMgmt**

1.  En un símbolo del sistema, escriba **net** **Start** **WinMgmt** \[ */<switch>* \] .

    Para obtener más información acerca de los modificadores que están disponibles, vea [WinMgmt](winmgmt.md). Use la cuenta predefinida Administrador o una cuenta en el grupo administradores que se ejecuta con permisos elevados para iniciar el servicio WMI. Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

2.  Otros servicios que dependen del servicio WMI, como el host de agente de SMS o el Firewall de Windows, no se reiniciarán automáticamente.

## <a name="stopping-winmgmt-service"></a>Deteniendo el servicio WinMgmt

En el procedimiento siguiente se describe cómo detener el servicio WMI.

**Para detener el servicio WinMgmt**

1.  En un símbolo del sistema, escriba **net stop WinMgmt**.

2.  Otros servicios que dependen del servicio WMI también se detienen, como el host de agente de SMS o el Firewall de Windows.

## <a name="examples"></a>Ejemplos

La galería de TechNet contiene el [script de vigilancia del servicio WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), que describe cómo cerrar y reiniciar el servicio WinMgmt mediante programación con PowerShell.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de las herramientas de Command-Line WMI](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



