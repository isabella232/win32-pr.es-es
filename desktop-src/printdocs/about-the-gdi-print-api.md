---
description: Una de las principales características de las funciones de la API de impresión GDI es su compatibilidad con la independencia del dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Acerca de la API de impresión de GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951015"
---
# <a name="about-the-gdi-print-api"></a>Acerca de la API de impresión de GDI

Una de las principales características de las funciones de la API de impresión GDI es su compatibilidad con la independencia del dispositivo. En lugar de emitir comandos específicos del dispositivo para dibujar la salida en una impresora o trazador determinados, una aplicación llama a funciones de alto nivel desde la interfaz de dispositivo gráfico (GDI). Por ejemplo, para imprimir una imagen de mapa de bits, una aplicación puede llamar a la función [**BitBlt,**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) suministrando las coordenadas del mapa de bits, así como identificadores que identifican los contextos de dispositivo (CONTROLADORES) de origen y destino. A continuación, un controlador de impresora convierte la llamada a **BitBlt** en comandos de dispositivo sin formato. Un controlador de dispositivo es una biblioteca de vínculos dinámicos (DLL) que admite la interfaz de controlador de dispositivo (DDI). Un controlador de dispositivo genera comandos de dispositivo sin procesar cuando procesa llamadas a funciones DDI realizadas por el motor de gráficos. La impresora procesa los comandos cuando imprime la imagen. La sintaxis, el número y el tipo de estos comandos varían de un dispositivo a otro.

Esta información general proporciona información sobre los temas siguientes.

<dl>

[Interfaz de impresión predeterminada](default-printing-interface.md)  
[Contextos de dispositivo de impresora](printer-output.md)  
[Escapes de impresora](printer-escapes.md)  
[Presentación y salida de WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE por usuario](per-user-devmode.md)  
</dl>

 

 
