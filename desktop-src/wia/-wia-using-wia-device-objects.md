---
description: Un dispositivo de imagen se representa en la adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Usar objetos de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154381"
---
# <a name="using-wia-device-objects"></a>Usar objetos de dispositivo WIA

Un dispositivo de imagen se representa en la adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ). Normalmente, la raíz de este árbol de elementos representa el propio dispositivo, mientras que los demás elementos del árbol representan imágenes, para una cámara o regiones de digitalización, para un escáner.

Las aplicaciones usan el administrador de dispositivos WIA para crear y enumerar dispositivos WIA. En las secciones siguientes se explica cómo crear y usar dispositivos WIA:

-   [Selección de un dispositivo](-wia-selecting-a-device.md)
-   [Dispositivos de cámara WIA](-wia-wia-camera-devices.md)
-   [Dispositivos WIA Scanner](-wia-wia-scanner-devices.md)

 

 



