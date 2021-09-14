---
description: La interfaz del dispositivo gráfico (GDI) mantiene siete pinceles de existencias lógicos predefinidos. También hay 21 pinceles de existencias lógicos predefinidos que mantiene la interfaz de administración de ventanas (USER).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pincel de existencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170297"
---
# <a name="stock-brush"></a>Pincel de existencias

La interfaz del dispositivo gráfico (GDI) mantiene siete pinceles de existencias lógicos predefinidos. También hay 21 pinceles de existencias lógicos predefinidos que mantiene la interfaz de administración de ventanas (USER).

En la ilustración siguiente se muestran rectángulos dibujados mediante los siete pinceles estándar predefinidos.

![ilustración que muestra siete cuadros: uno negro, tres tonos de gris y tres que aparecen vacíos](images/csbru-03.png)

Una aplicación puede recuperar un identificador que identifique uno de los siete pinceles estándar llamando a la [**función GetStockObject,**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) especificando el tipo de pincel.

Los 21 pinceles estándar que mantiene la interfaz de administración de ventanas corresponden a los colores de los elementos de la ventana, como menús, barras de desplazamiento y botones. Una aplicación puede obtener un identificador que identifique uno de estos pinceles llamando a la función [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) y especificando un valor de color del sistema. Una aplicación puede recuperar el color correspondiente a un elemento de ventana determinado llamando a la [**función GetSysColor.**](/windows/win32/api/winuser/nf-winuser-getsyscolor) Una aplicación puede establecer el color correspondiente a un elemento de ventana llamando a la [**función SetSysColors.**](/windows/win32/api/winuser/nf-winuser-setsyscolors)

 

 
