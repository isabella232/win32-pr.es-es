---
description: WIA representa un dispositivo de cámara como un árbol jerárquico de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de cámara WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275449"
---
# <a name="wia-camera-devices"></a>Dispositivos de cámara WIA

WIA representa un dispositivo de cámara como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . El elemento raíz, devuelto desde una llamada al método [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) del administrador de dispositivos de adquisición de imágenes de Windows (WIA), se usa para obtener y establecer la información del dispositivo, para controlar el dispositivo y para iniciar la enumeración de elementos de dispositivo.

> [!Note]  
> WIA no admite cámaras en Windows Vista o posterior. En el caso de las versiones de Windows, use la API de dispositivo portátil de Windows (WPD) que se describe en el kit de desarrollo de controladores de Windows (DDK) para adquirir imágenes de cámaras.

 

En el diagrama siguiente se muestra una implementación de cámara de ejemplo. El elemento raíz de la cámara tiene tres elementos secundarios, dos imágenes y una carpeta. La carpeta tiene dos elementos secundarios, ambas imágenes.

![implementación de la cámara de ejemplo](images/wihierar.gif)

 

 



