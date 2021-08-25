---
title: Obtención de MCI Información del sistema
description: Obtención de MCI Información del sistema
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fa6cc0757bc09aa16216f2f20385bf31b44bb88e27ea64e091ff3909d8d57e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893225"
---
# <a name="obtaining-mci-system-information"></a>Obtención de MCI Información del sistema

El [comando sysinfo](sysinfo.md) ([**MCI \_ SYSINFO**](mci-sysinfo.md)) obtiene información del sistema sobre los dispositivos MCI. MCI controla este comando sin retransmitirlo a ningún dispositivo MCI. Para la interfaz de mensaje de comando, MCI devuelve la información del sistema en la estructura [**\_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

Puede usar el comando **sysinfo** (MCI SYSINFO) para recuperar información como el número de dispositivos MCI en un sistema, el número de dispositivos MCI de un tipo determinado, el número de dispositivos MCI abiertos y los nombres de los \_ dispositivos. A menudo se llama a este comando más de una vez para recuperar un fragmento de información determinado. Por ejemplo, puede recuperar el número de dispositivos de un tipo determinado en la primera llamada y, a continuación, enumerar los nombres de los dispositivos en la siguiente.

 

 




