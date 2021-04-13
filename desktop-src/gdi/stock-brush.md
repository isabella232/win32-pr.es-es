---
description: La interfaz de dispositivo gráfico (GDI) mantiene siete pinceles de cotización lógica predefinidos. También hay 21 pinceles de cotización lógica predefinidos mantenidos por la interfaz de administración de ventanas (usuario).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pincel bursátil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985923"
---
# <a name="stock-brush"></a>Pincel bursátil

La interfaz de dispositivo gráfico (GDI) mantiene siete pinceles de cotización lógica predefinidos. También hay 21 pinceles de cotización lógica predefinidos mantenidos por la interfaz de administración de ventanas (usuario).

En la ilustración siguiente se muestran los rectángulos pintados con los siete pinceles de cotización predefinidos.

![Ilustración que muestra siete cuadros: uno negro, tres tonos de gris y tres que aparecen vacíos](images/csbru-03.png)

Una aplicación puede recuperar un identificador que identifique uno de los siete pinceles bursátiles mediante una llamada a la función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , especificando el tipo de pincel.

Los 21 pinceles de bolsa que mantiene la interfaz de administración de ventanas se corresponden con los colores de los elementos de ventana, como los menús, las barras de desplazamiento y los botones. Una aplicación puede obtener un identificador que identifique uno de estos pinceles llamando a la función [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) y especificando un valor de color del sistema. Una aplicación puede recuperar el color correspondiente a un elemento de ventana determinado mediante una llamada a la función [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) . Una aplicación puede establecer el color correspondiente a un elemento de ventana mediante una llamada a la función [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .

 

 
