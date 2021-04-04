---
description: Ejemplo de VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Ejemplo de VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908365"
---
# <a name="vmrplayer-sample"></a>Ejemplo de VMRPlayer

## <a name="description"></a>Descripción

Este ejemplo usa el filtro de mezclador de vídeo 9 (VMR-9) para mezclar uno o dos vídeos en ejecución y una imagen estática.

## <a name="usage"></a>Uso

Para abrir el primer vídeo, elija **abrir flujo principal** en el menú **archivo** . Para abrir un segundo vídeo, elija **abrir flujo secundario** en el menú **archivo** (primero debe abrir el flujo principal). Para reproducir el vídeo, haga clic en el botón **reproducir** .

Puede establecer la posición, el tamaño y los valores alfa de los vídeos seleccionando **flujo principal** o **secuencia de Secondard** desde el menú de **propiedades de VMR** .

Para agregar un mapa de bits estático sobre el vídeo, elija **imagen de aplicación estática** en el menú de **propiedades de VMR** y haga clic en el cuadro **Mostrar imagen de aplicación** . Puede usar el mismo cuadro de diálogo para controlar la posición, el tamaño y el valor alfa del mapa de bits.

Para capturar la imagen de vídeo combinada, elija **capturar imagen de mapa de bits** en el menú de **propiedades de VMR** .

También puede especificar la secuencia de imagen principal desde la línea de comandos:

**VMRPlayer** **/p** *nombrearchivo*

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



