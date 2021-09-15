---
description: Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Edición de un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474335"
---
# <a name="editing-an-enhanced-metafile"></a>Edición de un metarchivo mejorado

Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.

**Para editar una imagen almacenada en un metarchivo mejorado**

1.  Use las pruebas de posicionamiento para capturar las coordenadas del cursor y recuperar la posición del objeto (línea, arco, rectángulo, elipse, polígono o forma irregular) que el usuario quiere modificar.
2.  Convierta estas coordenadas en unidades lógicas (o globales).
3.  Llame a [**la función EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) y examine cada registro de metarchivo.
4.  Determine si un registro determinado corresponde a una función de dibujo GDI.
5.  Si es así, determine si las coordenadas almacenadas en el registro corresponden a la línea, arco, elipse u otro elemento gráfico que forma una intersección con las coordenadas especificadas por el usuario.
6.  Al buscar el registro que corresponde a la salida que el usuario desea modificar, borre el objeto en la pantalla correspondiente al registro original.
7.  Elimine el registro correspondiente del metarchivo y guarde un puntero en su ubicación.
8.  Permitir al usuario volver a dibujar o reemplazar el objeto.
9.  Convierta las funciones GDI usadas para dibujar el nuevo objeto en uno o varios registros de metarchivo mejorado.
10. Almacene estos registros en el metarchivo mejorado.

 

 



