---
description: 'Las aplicaciones pueden usar las siguientes funciones para recuperar los datos del dispositivo mediante un contexto de dispositivo: GetDeviceCaps y DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recuperación de datos del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984814"
---
# <a name="retrieving-device-data"></a>Recuperación de datos del dispositivo

Las aplicaciones pueden usar las siguientes funciones para recuperar los datos del dispositivo mediante un contexto de dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) y [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera datos de dispositivo generales para los siguientes dispositivos:

-   Tramas, pantallas
-   Impresoras matriciales
-   Impresoras de chorro de tinta
-   Impresoras láser
-   Trazadores gráficos vectoriales
-   Cámaras de tramas

Los datos incluyen las capacidades admitidas del dispositivo, incluida la resolución del dispositivo (para pantallas de vídeo), el formato de color (para pantallas de vídeo y las impresoras de color), el número de objetos gráficos, las capacidades de trama, el dibujo de curva, el dibujo de líneas, el dibujo de polígono y el dibujo de texto. Una aplicación recupera estos datos proporcionando un identificador que identifica el contexto de dispositivo adecuado, así como un índice que especifica el tipo de datos que la función va a recuperar.

La función [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera datos específicos de las impresoras, incluido el número de bandejas de papel disponibles, las capacidades de dúplex de la impresora, las resoluciones admitidas por la impresora, el tamaño de papel máximo y mínimo admitido, etc. Una aplicación recupera estos datos proporcionando cadenas que especifican un dispositivo de impresora y un puerto, así como un índice que especifica el tipo de datos que la función va a recuperar.

 

 
