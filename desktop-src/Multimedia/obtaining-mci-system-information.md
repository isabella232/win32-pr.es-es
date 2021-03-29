---
title: Obtención de información del sistema MCI
description: Obtención de información del sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Comando MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994130"
---
# <a name="obtaining-mci-system-information"></a>Obtención de información del sistema MCI

El comando [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md)) obtiene información del sistema acerca de los dispositivos MCI. MCI controla este comando sin retransmitirlo a ningún dispositivo MCI. En la interfaz de mensaje de comando, MCI devuelve la información del sistema en la estructura de [**\_ \_ parms de MCI SYSINFO**](mci-sysinfo-parms.md) .

Puede usar el comando **sysinfo** (MCI \_ sysinfo) para recuperar información como el número de dispositivos MCI en un sistema, el número de dispositivos MCI de un tipo determinado, el número de dispositivos MCI abiertos y los nombres de los dispositivos. Este comando a menudo se llama más de una vez para recuperar una parte determinada de la información. Por ejemplo, puede recuperar el número de dispositivos de un tipo determinado en la primera llamada y, a continuación, enumerar los nombres de los dispositivos en el siguiente.

 

 




