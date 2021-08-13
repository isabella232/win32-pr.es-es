---
description: Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al principio de la operación de dibujo y asigna un píxel del mapa de bits del pincel al área cliente en el origen de la ventana, que es la esquina superior izquierda de la ventana.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origen del pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccdc1dfa370ceb84216c89d562ef56dd206ce744b3be4fd38deb87175c1cf73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400395"
---
# <a name="brush-origin"></a>Origen del pincel

Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al principio de la operación de dibujo y asigna un píxel en el mapa de bits del pincel al área cliente en el origen de la *ventana,* que es la esquina superior izquierda de la ventana. Las coordenadas del píxel que asigna el sistema se denominan el *origen del pincel.* El origen de pincel predeterminado se encuentra en la esquina superior izquierda del mapa de bits del pincel, en las coordenadas (0,0). A continuación, el sistema copia el pincel en el área de cliente, formando un patrón que es tan alto como el mapa de bits. La operación de copia continúa, fila por fila, hasta que se rellena todo el área de cliente. Sin embargo, el patrón de pincel solo es visible dentro de los límites de la forma especificada.

Hay instancias en las que no se debe usar el origen de pincel predeterminado. Por ejemplo, puede ser necesario que una aplicación use el mismo pincel para pintar los fondos de sus ventanas primarias y secundarias y combinar el fondo de una ventana secundaria con el de la ventana primaria. Para ello, la aplicación debe restablecer el origen del pincel llamando a la función [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) y desplazando el origen el número necesario de píxeles. (Una aplicación puede recuperar el origen de pincel actual llamando a la [**función GetBrushOrgEx).**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)

En la ilustración siguiente se muestra una estrella de cinco puntas rellenada mediante un pincel definido por la aplicación. En la ilustración se muestra una imagen ampliada del pincel, así como la ubicación a la que se asignó al principio de la operación de pintura.

![ilustración que muestra que el origen del pincel se asigna al origen de la ventana](images/csbru-01.png)

 

 



