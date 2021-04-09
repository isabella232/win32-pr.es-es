---
title: Detección de dispositivos
description: Puede buscar dispositivos de tres maneras por tipo, por UDN, y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055d08db76edd5bcc5591d3254613462c00fc974
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903777"
---
# <a name="discovering-devices"></a>Detección de dispositivos

Puede buscar dispositivos de tres maneras: por tipo, por UDN, y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).

![ventana detectar dispositivos](images/ucp-disc.png)

**Para detectar dispositivos**

1.  Seleccione el tipo de búsqueda que quiere usar: **Buscar por tipo**, **Buscar por UDN** o **Async Find**.
2.  Seleccione el tipo de dispositivo o UDN que desea buscar en la lista (para búsquedas por tipo o por UDN). El contenido de la lista se basa en el contenido de los archivos udn.txt y devtype.txt que editó anteriormente.
3.  Haga clic en **Iniciar detección**. La búsqueda se ha iniciado. Los resultados se muestran en la lista **dispositivos encontrados** . Si no se encuentra ningún dispositivo, se muestra un mensaje que indica esta condición. El estado del progreso de la búsqueda se muestra en el campo **Estado** .

Cuando se usa la búsqueda asincrónica, los nuevos dispositivos encontrados se muestran en la lista **dispositivos encontrados** y en la barra de **Estado** . Una vez finalizada la búsqueda asincrónica, la barra de **Estado** muestra un mensaje que indica esto. Sin embargo, dado que una búsqueda asincrónica se ejecuta hasta que se detiene manualmente, aparecen nuevos dispositivos en la lista **dispositivos encontrados** y en la barra de **Estado** a medida que los dispositivos aparecen en la red.

Una vez que haya detectado dispositivos, puede [controlarlos](controlling-a-device.md).

 

 




