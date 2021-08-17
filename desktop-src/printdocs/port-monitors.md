---
description: Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se vuelve a pasar al administrador de trabajos en cola.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de puerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470935"
---
# <a name="port-monitors"></a>Monitores de puerto

Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se vuelve a pasar al administrador de trabajos en cola. El colador envía estos comandos de bajo nivel a un monitor. Un monitor de puerto es un .dll que pasa los comandos de dispositivo sin procesar a través de la red, a través de un puerto paralelo o a través de un puerto serie al dispositivo de impresora. Se pueden instalar monitores de puerto personalizados para admitir el paso de datos del dispositivo a través de otros puertos de comunicación.

Use las siguientes funciones para trabajar con monitores de puerto.



| Función                               | Descripción                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión. |
| [**DeleteMonitor**](deletemonitor.md) | Quita un monitor de puerto agregado por la [**función AddMonitor.**](addmonitor.md)      |
| [**EnumMonitors**](enummonitors.md)   | Enumera los monitores de puerto instalados en un servidor especificado.                       |



 

 

 



