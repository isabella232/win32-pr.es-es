---
description: Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones VSS. Tenga en cuenta que estas herramientas se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso de diagnósticos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696484"
---
# <a name="using-vss-diagnostics"></a>Uso de diagnósticos de VSS

Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones VSS.

> [!Note]  
> Estas herramientas se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. Puede descargar la Windows SDK desde [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

En la instalación de Windows SDK, estas herramientas se pueden encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).

## <a name="gathering-data"></a>Recopilación de datos

Puede recopilar datos mediante el comando Vssagent.

**Para recopilar datos mediante Vssagent**

1.  Para recopilar datos desde la línea de comandos, use el comando Vssagent de la siguiente manera:

    **vssagent-Gather** *XmlFileName * * *. XML**

2.  Para ver el archivo de salida, vea la sección siguiente visualización de datos.

## <a name="viewing-data"></a>Ver datos

La aplicación Vsdiagview se puede usar para ver los datos que se recopilaron con el comando Vssagent. Vsdiagview muestra la siguiente información acerca del equipo:

-   Información sobre el equipo, como la versión del sistema operativo, la memoria total disponible y la velocidad de la CPU
-   Los nombres y números de versión de los archivos binarios de VSS
-   Los nombres y las propiedades de los dispositivos de disco y volumen
-   Los nombres y las propiedades de las aplicaciones COM+
-   Los nombres de los registros de eventos que se pueden usar para diagnosticar problemas de VSS
-   Los nombres de los escritores de VSS y los eventos que controlan
-   Información sobre otros archivos del sistema operativo

**Para ver los datos mediante Vsdiagview**

1.  En el menú Archivo, elija **abrir** para buscar un archivo. (La ubicación predeterminada es C: \\ vssdiag).
2.  Haga clic en **abrir** para ver los datos.

 

 



