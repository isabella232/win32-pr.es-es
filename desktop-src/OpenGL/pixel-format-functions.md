---
title: Funciones de formato de píxel
description: Las siguientes funciones Windows administrar formatos de píxel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funciones WGL, formato de píxel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071449"
---
# <a name="pixel-format-functions"></a>Funciones de formato de píxel

Las siguientes funciones Windows administrar formatos de píxel.



| Windows Función                                               | Descripción                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Obtiene el formato de píxel del contexto del dispositivo que es la coincidencia más cercana a un formato de píxel especificado.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Establece el formato de píxel actual de un contexto de dispositivo en el formato de píxel especificado por un índice de formato de píxel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Obtiene el índice de formato de píxel del formato de píxel actual de un contexto de dispositivo.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Dado un contexto de dispositivo y un índice de formato de píxel, rellena una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) con las propiedades del formato de píxel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Recupera información de formato de píxel para un metarchivo mejorado.                                                                                                          |



 

La [**función ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) devuelve un índice de formato de píxeles basado en uno que identifica la mejor coincidencia a partir de los formatos de píxel admitidos por el contexto del dispositivo.

La [**función SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica el formato deseado mediante un índice de formato de píxeles basado en uno. Normalmente, se llama a **ChoosePixelFormat para** buscar un formato de píxeles que coincida mejor y, a continuación, se llama a **SetPixelFormat con** el resultado **de ChoosePixelFormat**.

Si llama a **SetPixelFormat para un** contexto de dispositivo que hace referencia a una ventana, **SetPixelFormat** también cambia el formato de píxel de la ventana. Establecer el formato de píxel de una ventana más de una vez puede provocar complicaciones significativas para el Administrador de ventanas y para las aplicaciones multiproceso, por lo que no se permite. Puede establecer el formato de píxel de una ventana solo una vez; Después de eso, no se puede cambiar el formato de píxel de la ventana.

La [**función GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) devuelve un índice de formato de píxeles basado en uno.

La [**función DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) toma lo siguiente como parámetros:

-   Identificador de un contexto de dispositivo
-   Índice de formato de píxel
-   Puntero a una [**estructura de datos PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

La [**función DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) devuelve con los miembros de **PIXELFORMATDESCRIPTOR** establecidos correctamente.

La **función GetEnhMetaFilePixelFormat** devuelve el tamaño del formato de píxel de un metarchivo y recupera la información de formato de píxel del metarchivo.

 

 




