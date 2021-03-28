---
description: Una aplicación puede utilizar el recorte y las rutas de acceso para crear efectos gráficos especiales. En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Trazados de clips y efectos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544547"
---
# <a name="clip-paths-and-graphic-effects"></a>Trazados de clips y efectos gráficos

Una aplicación puede utilizar el recorte y las rutas de acceso para crear efectos gráficos especiales. En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.

![Ilustración en la que se muestra el texto negro sobre un fondo blanco](images/cspth-02.png)

En la ilustración siguiente se muestra el resultado de seleccionar el texto como una ruta de recorte y dibujar líneas radiales para un círculo cuyo centro se encuentra encima y a la izquierda de la cadena.

![Ilustración que muestra el mismo texto, pero rellenado con líneas en lugar de negro sólido](images/cspth-03.png)

> [!Note]  
> Antes de que la interfaz de dispositivo gráfico (GDI) agregue texto creado con una fuente de mapa de imágenes a un trazado, convierte la fuente en una fuente de esquema o de vector.

 

Una aplicación crea una ruta de acceso de clip generando un corchete de ruta de acceso y llamando a la función [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) . Después de seleccionar una ruta de acceso de recorte en un controlador de dominio, la salida solo aparece dentro de los bordes de la ruta de acceso.

Además de crear efectos de gráficos especiales, las rutas de acceso de clip también son útiles en aplicaciones que guardan imágenes como metaarchivos mejorados. Mediante el uso de una ruta de acceso de clip, una aplicación puede garantizar la independencia del dispositivo porque las unidades utilizadas para especificar una ruta de acceso son unidades lógicas.

 

 



