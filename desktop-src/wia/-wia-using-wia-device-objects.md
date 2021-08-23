---
description: Un dispositivo de creación de imágenes se representa en Windows Adquisición de imágenes (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Uso de objetos de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f9ec9fd4a3fc4746b1908863ae6afcdcc60b54aa7f9f8f73c769d52ad08688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813485"
---
# <a name="using-wia-device-objects"></a>Uso de objetos de dispositivo WIA

Un dispositivo de creación de imágenes se representa Windows adquisición de imágenes (WIA) como un árbol jerárquico de objetos de elementos WIA (interfaces [**IWiaItem).**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Normalmente, la raíz de este árbol de elementos representa el propio dispositivo, mientras que los demás elementos del árbol representan imágenes, para una cámara o regiones de examen, para un escáner.

Las aplicaciones usan el administrador de dispositivos WIA para crear y enumerar dispositivos WIA. En las secciones siguientes se explica cómo crear y usar dispositivos WIA:

-   [Selección de un dispositivo](-wia-selecting-a-device.md)
-   [Dispositivos de cámara WIA](-wia-wia-camera-devices.md)
-   [Dispositivos WIA Scanner](-wia-wia-scanner-devices.md)

 

 



