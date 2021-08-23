---
description: Una aplicación puede usar recortes y trazados para crear efectos gráficos especiales. En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Recorte de trazados y efectos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80605f4dc58846f3a9e8440801d46768384c103ff6e3f9df5e3d448d9b12aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038169"
---
# <a name="clip-paths-and-graphic-effects"></a>Recorte de trazados y efectos gráficos

Una aplicación puede usar recortes y trazados para crear efectos gráficos especiales. En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.

![ilustración que muestra texto negro sobre un fondo blanco](images/cspth-02.png)

En la ilustración siguiente se muestra el resultado de seleccionar el texto como una ruta de acceso de recorte y dibujar líneas radiales para un círculo cuyo centro se encuentra encima e izquierda de la cadena.

![ilustración que muestra el mismo texto, pero rellenada con líneas en lugar de negro sólido](images/cspth-03.png)

> [!Note]  
> Antes de que la interfaz de dispositivo gráfico (GDI) agrega texto creado con una fuente de mapa de bits a una ruta de acceso, convierte la fuente en una fuente de esquema o vector.

 

Una aplicación crea una ruta de acceso de recorte generando un corchete de ruta de acceso y, a continuación, llamando a [**la función SelectClipPath.**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) Después de seleccionar una ruta de acceso de recorte en un controlador de dominio, la salida solo aparece dentro de los bordes de la ruta de acceso.

Además de crear efectos gráficos especiales, las rutas de acceso de recorte también son útiles en aplicaciones que guarden imágenes como metarchivos mejorados. Mediante el uso de una ruta de acceso de recorte, una aplicación puede garantizar la independencia del dispositivo porque las unidades usadas para especificar una ruta de acceso son unidades lógicas.

 

 



