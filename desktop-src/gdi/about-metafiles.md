---
description: Internamente, un metarchivo es una matriz de estructuras de longitud variable llamadas registros de metarchivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Acerca de los metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811347"
---
# <a name="about-metafiles"></a>Acerca de los metaarchivos

Internamente, un metarchivo es una matriz de estructuras de longitud variable llamadas *registros de metarchivo*. Los primeros registros del metarchivo especifican información general, como la resolución del dispositivo en el que se creó la imagen, las dimensiones de la imagen, etc. Los registros restantes, que constituyen la mayor parte de los metarchivos, corresponden a las funciones de la interfaz de dispositivo gráfico (GDI) necesarias para dibujar la imagen. Estos registros se almacenan en el metarchivo una vez que se crea un contexto de dispositivo de metarchivo especial. Este contexto de dispositivo de metarchivo se utiliza para todas las operaciones de dibujo necesarias para crear la imagen. Cuando el sistema procesa una función GDI asociada a un DC de metarchivo, convierte la función en los datos adecuados y almacena estos datos en un registro anexado al metarchivo.

Una vez completada una imagen y almacenada en el metarchivo el último registro, puede pasar el metarchivo a otra aplicación:

-   Usar el portapapeles
-   Incrustarlo en otro archivo
-   Almacenar en disco
-   Reproducción repetida

Se *reproduce* un metarchivo cuando sus registros se convierten en comandos de dispositivo y se procesan mediante el dispositivo adecuado.

Hay dos tipos de metaarchivos:

-   [Metaarchivos con formato mejorado](enhanced-format-metafiles.md)
-   [Metaarchivos con formato de Windows](windows-format-metafiles.md)

 

 



