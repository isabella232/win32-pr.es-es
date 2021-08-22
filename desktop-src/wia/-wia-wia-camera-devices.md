---
description: WIA representa un dispositivo de cámara como un árbol jerárquico de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de cámara WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592734"
---
# <a name="wia-camera-devices"></a>Dispositivos de cámara WIA

WIA representa un dispositivo de cámara como un árbol jerárquico de [**objetos IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) El elemento raíz, devuelto por una llamada al método [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) del administrador de dispositivos de adquisición de imágenes (WIA) de Windows, se usa para obtener y establecer la información del dispositivo, controlar el dispositivo y comenzar la enumeración de elementos de dispositivo.

> [!Note]  
> WIA no admite cámaras en Windows Vista o versiones posteriores. Para esas versiones de Windows, use la API Windows Portable Device (WPD) descrita en el Kit de desarrollo de controladores (DDK) de Windows para adquirir imágenes de las cámaras.

 

En el diagrama siguiente se muestra una implementación de la cámara de ejemplo. El elemento raíz de la cámara tiene tres elementos secundarios, dos imágenes y una carpeta. La carpeta tiene dos elementos secundarios, ambas imágenes.

![implementación de la cámara de ejemplo](images/wihierar.gif)

 

 



