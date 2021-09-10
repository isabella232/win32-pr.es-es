---
title: Obtención de MCI Información del sistema
description: Obtención de MCI Información del sistema
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371647"
---
# <a name="obtaining-mci-system-information"></a>Obtención de MCI Información del sistema

El [comando sysinfo](sysinfo.md) ([**MCI \_ SYSINFO**](mci-sysinfo.md)) obtiene información del sistema sobre los dispositivos MCI. MCI controla este comando sin retransmitirlo a ningún dispositivo MCI. Para la interfaz de mensaje de comando, MCI devuelve la información del sistema en la estructura [**\_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

Puede usar el comando **sysinfo** (MCI SYSINFO) para recuperar información como el número de dispositivos MCI en un sistema, el número de dispositivos MCI de un tipo determinado, el número de dispositivos MCI abiertos y los nombres de los \_ dispositivos. A menudo se llama a este comando más de una vez para recuperar un fragmento de información determinado. Por ejemplo, puede recuperar el número de dispositivos de un tipo determinado en la primera llamada y, a continuación, enumerar los nombres de los dispositivos en la siguiente.

 

 




