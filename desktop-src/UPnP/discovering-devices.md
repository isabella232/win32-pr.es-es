---
title: Detectar dispositivos
description: Puede buscar dispositivos de tres maneras por tipo, por UDN y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4975c14008dcf98b7a9145320f509a3c2bceb245cd54481654ed6548a92348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058082"
---
# <a name="discovering-devices"></a>Detectar dispositivos

Puede buscar dispositivos de tres maneras: por tipo, por UDN y por búsqueda asincrónica (que es una búsqueda por tipo de dispositivo).

![ventana detectar dispositivos](images/ucp-disc.png)

**Para detectar dispositivos**

1.  Seleccione el tipo de búsqueda que desea usar: **Buscar por tipo,** **Buscar por UDN** o **Búsqueda asincrónica.**
2.  Seleccione el tipo de dispositivo o el UDN que desea buscar en la lista (para búsquedas por tipo o por UDN). El contenido de la lista se basa en el contenido de los archivos udn.txt y devtype.txt que editó anteriormente.
3.  Haga clic en **Iniciar detección**. Se inicia la búsqueda. Los resultados se muestran en la **lista Dispositivos encontrados.** Si no se encuentra ningún dispositivo, se muestra un mensaje que indica esta condición. El estado del progreso de la búsqueda se muestra en el **campo** Estado.

Cuando se usa la búsqueda asincrónica, los nuevos  dispositivos que se encuentran se muestran en la lista Dispositivos encontrados y en la **barra Estado.** Una vez finalizada la búsqueda asincrónica, la **barra estado** muestra un mensaje que indica esto. Sin embargo, dado que una búsqueda asincrónica se ejecuta  hasta que se  detiene manualmente, aparecen nuevos dispositivos en la lista Dispositivos encontrados y en la barra Estado a medida que los dispositivos aparecen en la red.

Una vez que haya detectado dispositivos, puede [controlarlos.](controlling-a-device.md)

 

 




