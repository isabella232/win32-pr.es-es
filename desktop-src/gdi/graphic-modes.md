---
description: Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, etc. Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544483"
---
# <a name="graphic-modes"></a>Modos gráficos

Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, etc. Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.



| Modo gráficos | Descripción                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Información previa    | Define cómo se mezclan los colores de fondo con los colores de pantalla o ventana existentes para las operaciones de texto y de mapa de bits.              |
| Dibujo       | Define cómo se mezclan los colores de primer plano con los colores de pantalla o ventana existentes para las operaciones de lápiz, pincel, mapa de bits y texto. |
| Asignación       | Define cómo se asignan los resultados de los gráficos del espacio lógico (o del mundo) en la ventana, la pantalla o el papel de la impresora.             |
| Relleno de polígono  | Define cómo se usa el patrón de pincel para rellenar el interior de regiones complejas.                                             |
| Ajuste    | Define cómo se mezclan los colores de los mapas de bits con los colores de pantalla o ventana existentes cuando el mapa de bits se comprime (o se reduce verticalmente).  |



 

Al igual que con los objetos gráficos, el sistema Inicializa un controlador de dominio con los modos gráficos predeterminados. Una aplicación puede recuperar y examinar estos modos predeterminados llamando a las siguientes funciones.



| Modo gráficos | Función                                       |
|---------------|------------------------------------------------|
| Información previa    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Dibujo       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Asignación       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Relleno de polígono  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Ajuste    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Una aplicación puede cambiar los modos predeterminados mediante una llamada a una de las siguientes funciones.



| Modo gráficos | Función                                       |
|---------------|------------------------------------------------|
| Información previa    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Dibujo       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Asignación       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Relleno de polígono  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Ajuste    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



