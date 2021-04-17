---
description: Una de las principales características de las funciones de la API de impresión de GDI es su compatibilidad con la independencia del dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Acerca de la API de impresión GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697517"
---
# <a name="about-the-gdi-print-api"></a>Acerca de la API de impresión GDI

Una de las principales características de las funciones de la API de impresión de GDI es su compatibilidad con la independencia del dispositivo. En lugar de emitir comandos específicos del dispositivo para dibujar la salida en una impresora o un trazador determinado, una aplicación llama a funciones de alto nivel desde la interfaz de dispositivo gráfico (GDI). Por ejemplo, para imprimir una imagen de mapa de bits, una aplicación puede llamar a la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) y proporcionar las coordenadas para el mapa de bits, así como los identificadores de los contextos de dispositivos de origen y de destino (DC). A continuación, el controlador de impresora convierte la llamada a **bitblt** en los comandos de dispositivo sin formato. Un controlador de dispositivo es una biblioteca de vínculos dinámicos (DLL) que admite la interfaz de controlador de dispositivo (DDI). Un controlador de dispositivo genera comandos de dispositivo sin formato cuando procesa llamadas a funciones DDI realizadas por el motor de gráficos. La impresora procesa los comandos cuando imprime la imagen. La sintaxis, el número y el tipo de estos comandos varían de un dispositivo a un dispositivo.

En esta información general se proporciona información sobre los temas siguientes.

<dl>

[Interfaz de impresión predeterminada](default-printing-interface.md)  
[Contextos de dispositivo de impresora](printer-output.md)  
[Escapes de impresora](printer-escapes.md)  
[Presentación y salida de WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE por usuario](per-user-devmode.md)  
</dl>

 

 
