---
description: Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, y así sucesivamente. Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c36461935c8279e38e09afe9f7802e2f758d1cf45380beaa16d1911f4ed965f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558775"
---
# <a name="graphic-modes"></a>Modos gráficos

Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, y así sucesivamente. Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.



| Modo gráfico | Descripción                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Información previa    | Define cómo se mezclan los colores de fondo con los colores de ventana o pantalla existentes para las operaciones de mapa de bits y texto.              |
| Dibujo       | Define cómo se mezclan los colores de primer plano con los colores de ventana o pantalla existentes para las operaciones de lápiz, pincel, mapa de bits y texto. |
| Asignación       | Define cómo se asigna la salida de gráficos desde el espacio lógico (o el mundo) a la ventana, la pantalla o el papel de la impresora.             |
| Relleno de polígono  | Define cómo se usa el patrón de pincel para rellenar el interior de regiones complejas.                                             |
| Estiramiento    | Define cómo se mezclan los colores de mapa de bits con los colores de ventana o pantalla existentes cuando el mapa de bits se comprime (o se escala verticalmente).  |



 

Al igual que con los objetos gráficos, el sistema inicializa un controlador de dominio con los modos gráficos predeterminados. Una aplicación puede recuperar y examinar estos modos predeterminados llamando a las siguientes funciones.



| Modo gráfico | Función                                       |
|---------------|------------------------------------------------|
| Información previa    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Dibujo       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Asignación       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Relleno de polígono  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Estiramiento    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Una aplicación puede cambiar los modos predeterminados llamando a una de las siguientes funciones.



| Modo gráfico | Función                                       |
|---------------|------------------------------------------------|
| Información previa    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Dibujo       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Asignación       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Relleno de polígono  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Estiramiento    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



