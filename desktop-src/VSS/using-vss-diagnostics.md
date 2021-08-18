---
description: Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones de VSS. Nota Estas herramientas se incluyen en el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso de diagnósticos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7742bf706da0bb8fdd377960a597a61b6592b772df98982cec500434f66c7579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590808"
---
# <a name="using-vss-diagnostics"></a>Uso de diagnósticos de VSS

Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones de VSS.

> [!Note]  
> Estas herramientas se incluyen en el Kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores. Puede descargar el SDK Windows desde [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

En la instalación del SDK de Windows, estas herramientas se pueden encontrar en (para archivos de 64 Windows) y (para archivos de `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 Windows).

## <a name="gathering-data"></a>Recopilación de datos

Puede recopilar datos mediante el comando Vssagent.

**Para recopilar datos mediante Vssagent**

1.  Para recopilar datos de la línea de comandos, use el comando Vssagent como se muestra a continuación:

    **vssagent -gather** *XmlFileName,.xml**

2.  Para ver el archivo de salida, consulte la siguiente sección Visualización de datos.

## <a name="viewing-data"></a>Ver datos

La aplicación Vsdiagview se puede usar para ver los datos recopilados mediante el comando Vssagent. Vsdiagview muestra la siguiente información sobre el equipo:

-   Información sobre el equipo, como la versión del sistema operativo, la memoria total disponible y la velocidad de CPU
-   Nombres y números de versión de los archivos binarios de VSS
-   Nombres y propiedades de los dispositivos de disco y volumen
-   Nombres y propiedades de cualquier aplicación COM+
-   Los nombres de los registros de eventos que se pueden usar para diagnosticar problemas de VSS
-   Los nombres de los escritores de VSS y los eventos que controlan
-   Información sobre otros archivos del sistema operativo

**Para ver datos mediante Vsdiagview**

1.  En el menú Archivo, elija **Abrir** para buscar un archivo. (La ubicación predeterminada es C: \\ vssdiag).
2.  Haga **clic en** Abrir para ver los datos.

 

 



