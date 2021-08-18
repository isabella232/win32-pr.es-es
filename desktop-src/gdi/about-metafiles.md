---
description: Internamente, un metarchivo es una matriz de estructuras de longitud variable denominadas registros de metarchivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Acerca de metarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc573d54f1f89e2dfe06edb8e225516fe8f0946485592d7d6aaea1faa651de85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779465"
---
# <a name="about-metafiles"></a>Acerca de metarchivos

Internamente, un metarchivo es una matriz de estructuras de longitud variable *denominadas registros de metarchivo.* Los primeros registros del metarchivo especifican información general, como la resolución del dispositivo en el que se creó la imagen, las dimensiones de la imagen, y así sucesivamente. Los registros restantes, que constituyen la mayor parte de cualquier metarchivo, corresponden a las funciones de interfaz de dispositivo gráfico (GDI) necesarias para dibujar la imagen. Estos registros se almacenan en el metarchivo después de crear un contexto de dispositivo de metarchivo especial. A continuación, este contexto de dispositivo de metarchivo se usa para todas las operaciones de dibujo necesarias para crear la imagen. Cuando el sistema procesa una función GDI asociada a un controlador de dominio de metarchivo, convierte la función en los datos adecuados y almacena estos datos en un registro anexado al metarchivo.

Una vez completada una imagen y almacenado el último registro en el metarchivo, puede pasar el metarchivo a otra aplicación mediante:

-   Uso del Portapapeles
-   Insertarlo dentro de otro archivo
-   Almacenarlo en disco
-   Reproducirlo repetidamente

Un metarchivo *se reproduce* cuando sus registros se convierten en comandos de dispositivo y los procesa el dispositivo adecuado.

Hay dos tipos de metarchivos:

-   [Metarchivos de formato mejorado](enhanced-format-metafiles.md)
-   [Windows metarchivos con formato de archivo](windows-format-metafiles.md)

 

 



