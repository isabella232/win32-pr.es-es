---
description: Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Edición de un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155629"
---
# <a name="editing-an-enhanced-metafile"></a>Edición de un metarchivo mejorado

Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.

**Para editar una imagen almacenada en un metarchivo mejorado**

1.  Use la prueba de posicionamiento para capturar las coordenadas del cursor y recuperar la posición del objeto (línea, arco, rectángulo, elipse, polígono o forma irregular) que el usuario desea modificar.
2.  Convierta estas coordenadas en unidades lógicas (o universales).
3.  Llame a la función [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) y examine cada registro de metarchivo.
4.  Determinar si un registro determinado corresponde a una función de dibujo de GDI.
5.  Si es así, determine si las coordenadas almacenadas en el registro se corresponden con la línea, el arco, la elipse o cualquier otro elemento de gráficos que intersecte con las coordenadas especificadas por el usuario.
6.  Al buscar el registro que corresponde a la salida que el usuario desea modificar, borre el objeto en la pantalla correspondiente al registro original.
7.  Elimine el registro correspondiente del metarchivo y guarde un puntero en su ubicación.
8.  Permite al usuario volver a dibujar o reemplazar el objeto.
9.  Convierta las funciones GDI utilizadas para dibujar el nuevo objeto en uno o más registros de metarchivo mejorado.
10. Almacene estos registros en el metarchivo mejorado.

 

 



