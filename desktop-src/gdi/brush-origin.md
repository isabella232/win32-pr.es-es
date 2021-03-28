---
description: Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al inicio de la operación de pintura y asigna un píxel en el mapa de bits del pincel al área cliente en el origen de la ventana, que es la esquina superior izquierda de la ventana.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origen del pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565733"
---
# <a name="brush-origin"></a>Origen del pincel

Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al inicio de la operación de pintura y asigna un píxel en el mapa de bits del pincel al área cliente en el origen de la *ventana*, que es la esquina superior izquierda de la ventana. Las coordenadas del píxel que asigna el sistema se denominan *origen del pincel*. El origen del pincel predeterminado se encuentra en la esquina superior izquierda del mapa de bits del pincel, en las coordenadas (0,0). Después, el sistema copia el pincel en el área cliente, formando un patrón que es tan alto como el mapa de bits. La operación de copia continúa, fila por fila, hasta que se rellena todo el área cliente. Sin embargo, el patrón Brush solo es visible dentro de los límites de la forma especificada.

Hay instancias cuando no se debe utilizar el origen del pincel predeterminado. Por ejemplo, puede ser necesario que una aplicación use el mismo pincel para pintar los fondos de sus ventanas principales y secundarias y mezclar el fondo de una ventana secundaria con el de la ventana primaria. Para ello, la aplicación debe restablecer el origen del pincel llamando a la función [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) y desplazando el origen el número necesario de píxeles. (Una aplicación puede recuperar el origen del pincel actual llamando a la función [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) ).

En la ilustración siguiente se muestra una estrella de cinco puntas rellenada con un pincel definido por la aplicación. En la ilustración se muestra una imagen ampliada del pincel, así como la ubicación a la que se asignó al principio de la operación de dibujo.

![Ilustración en la que se muestra que el origen del pincel está asignado al origen de la ventana](images/csbru-01.png)

 

 



