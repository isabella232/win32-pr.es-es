---
description: 'Las aplicaciones pueden usar las siguientes funciones para recuperar datos del dispositivo mediante un contexto de dispositivo: GetDeviceCaps y DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recuperar datos del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717995"
---
# <a name="retrieving-device-data"></a>Recuperar datos del dispositivo

Las aplicaciones pueden usar las siguientes funciones para recuperar datos del dispositivo mediante un contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) [**y DeviceCapabilities.**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)

[**GetDeviceCaps recupera**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) datos generales del dispositivo para los dispositivos siguientes:

-   Pantallas de trama
-   Impresoras de matriz de puntos
-   Impresoras ink-jet
-   Impresoras láser
-   Trazadores vectoriales
-   Cámaras de trama

Los datos incluyen las funcionalidades admitidas del dispositivo, incluida la resolución de dispositivos (para las pantallas de vídeo), el formato de color (para las pantallas de vídeo y las impresoras de color), el número de objetos gráficos, las funcionalidades de trama, el dibujo de curva, el dibujo de línea, el dibujo de polígono y el dibujo de texto. Una aplicación recupera estos datos al proporcionar un identificador que identifica el contexto de dispositivo adecuado, así como un índice que especifica el tipo de datos que la función va a recuperar.

La función [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera datos específicos de las impresoras, incluido el número de papeleras de papel disponibles, las funcionalidades dúplex de la impresora, las resoluciones admitidas por la impresora, el tamaño máximo y mínimo de papel admitido, y así sucesivamente. Una aplicación recupera estos datos mediante el suministro de cadenas que especifican un puerto y un dispositivo de impresora, así como un índice que especifica el tipo de datos que va a recuperar la función.

 

 
