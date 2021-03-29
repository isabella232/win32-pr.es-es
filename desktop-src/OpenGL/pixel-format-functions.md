---
title: Funciones de formato de píxeles
description: Las siguientes funciones de Windows administran formatos de píxeles.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funciones de WGL, formato de píxel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903844"
---
# <a name="pixel-format-functions"></a>Funciones de formato de píxeles

Las siguientes funciones de Windows administran formatos de píxeles.



| Función de Windows                                               | Descripción                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Obtiene el formato de píxel del contexto del dispositivo, que es la coincidencia más cercana a un formato de píxel especificado.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Establece el formato de píxel actual del contexto del dispositivo en el formato de píxel especificado por un índice de formato de píxel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Obtiene el índice de formato de píxel del formato de píxel actual de un contexto de dispositivo.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Dado un contexto de dispositivo y un índice de formato de píxel, rellena una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) con las propiedades del formato de píxel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Recupera información de formato de píxel para un metarchivo mejorado.                                                                                                          |



 

La función [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) devuelve un índice de formato de píxel basado en uno que identifica la mejor coincidencia de los formatos de píxel admitidos del contexto del dispositivo.

La función [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica el formato deseado mediante un índice de formato de píxel basado en uno. Normalmente, se llama a **ChoosePixelFormat** para buscar un formato de píxel de mejor coincidencia y, a continuación, se llama a **SetPixelFormat** con el resultado de **ChoosePixelFormat**.

Si llama a **SetPixelFormat** para un contexto de dispositivo que haga referencia a una ventana, **SetPixelFormat** también cambiará el formato de píxel de la ventana. Establecer el formato de píxel de una ventana más de una vez puede provocar complicaciones significativas para el administrador de ventanas y para las aplicaciones multiproceso, por lo que no se permite. Puede establecer el formato de píxel de una ventana solo una vez; después de eso, no se puede cambiar el formato de píxel de la ventana.

La función [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) devuelve un índice de formato de píxel basado en uno.

La función [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) toma los siguientes parámetros:

-   Identificador de un contexto de dispositivo
-   Índice de formato de píxel
-   Puntero a una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

La función [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) devuelve con los miembros de **PIXELFORMATDESCRIPTOR** establecidos correctamente.

La función **GetEnhMetaFilePixelFormat** devuelve el tamaño del formato de píxel de un metarchivo y recupera la información del formato de píxel del metarchivo.

 

 




