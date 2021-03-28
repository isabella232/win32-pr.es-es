---
description: En la tabla siguiente se describen los modos de asignación.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modos de asignación y traducciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219bfe2f587ef9bc66f53d6f08404a0448180512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275998"
---
# <a name="mapping-modes-and-translations"></a>Modos de asignación y traducciones

En la tabla siguiente se describen los modos de asignación.



| Modo de asignación    | Descripción                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ | Cada unidad en el espacio de la página se asigna a una unidad especificada por la aplicación en el espacio del dispositivo. Es posible que el eje se escale o no (por ejemplo, un círculo dibujado en un espacio universal puede aparecer como una elipse cuando se represente en un dispositivo determinado). La aplicación también especifica la orientación del eje.                  |
| MM \_ HIENGLISH   | Cada unidad en el espacio de la página se asigna a 0,001 pulgadas en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                                 |
| MM \_ HIMETRIC    | Cada unidad en el espacio de la página se asigna a 0,01 milímetros en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                            |
| MM \_ anisotrópico   | Cada unidad en el espacio de la página se asigna a una unidad definida por la aplicación en el espacio del dispositivo. Los ejes siempre se escalan uniformemente. La aplicación puede especificar la orientación de los ejes.                                                                                                                                     |
| MM \_ LOENGLISH   | Cada unidad en el espacio de la página se asigna a 0,01 pulgadas en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                                  |
| MM \_ LOMETRIC    | Cada unidad en el espacio de la página se asigna a 0,1 milímetros en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                             |
| \_texto mm        | Cada unidad en el espacio de la página se asigna a un píxel. es decir, no se realiza ningún ajuste de escala. Cuando no hay ninguna traducción en vigor (este es el valor predeterminado), el espacio de página en el \_ modo de asignación de texto mm es equivalente al espacio físico del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de arriba a abajo. |
| MM \_ TWIPS       | Cada unidad en el espacio de la página se asigna a un vigésimo del punto de la impresora (1/1440 pulgadas). El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                           |



 

Para establecer un modo de asignación, llame a la función [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Recupere el modo de asignación actual para un controlador de dominio mediante una llamada a la función [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) .

Las transformaciones espacio de página a espacio de dispositivo constan de valores que se calculan a partir de los puntos especificados por la ventana y la ventanilla. En este contexto, la ventana hace referencia al sistema de coordenadas lógico del espacio de la página, mientras que la ventanilla hace referencia al sistema de coordenadas del dispositivo del espacio del dispositivo. La ventana y la ventanilla están compuestas por un origen, una extensión horizontal ("x") y una extensión vertical ("y"). Los parámetros de ventana están en coordenadas lógicas. la ventanilla en coordenadas de dispositivo (píxeles). El sistema combina los orígenes y las extensiones de la ventana y de la ventanilla para crear la transformación. Esto significa que la ventana y la ventanilla especifican la mitad de los factores necesarios para definir la transformación utilizada para asignar puntos en el espacio de la página al espacio del dispositivo. Por lo tanto, el sistema asigna el origen de la ventana al origen de la ventanilla y las extensiones de la ventana a las extensiones de la ventanilla, tal como se muestra en la siguiente ilustración.

![Ilustración que muestra el origen de una ventana en el espacio de la página y un origen de Viewpoint en el espacio del dispositivo](images/cstrn-15.png)

Las extensiones de ventanilla y ventana establecen una relación o un factor de escala que se usa en el espacio de página para las transformaciones de espacio de dispositivo. Para los seis modos de asignación predefinidos (MM \_ HIENGLISH, mm \_ LOENGLISH, mm \_ HIMETRIC, mm \_ LOMETRIC, \_ texto mm y mm \_ TWIPS), el sistema establece las extensiones cuando se llama a [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . No se pueden cambiar. Los otros dos modos de asignación (MM \_ anisotrópico y mm \_ ) requieren que se especifiquen las extensiones. Esto se hace llamando a **SetMapMode** para establecer el modo adecuado y, a continuación, llamar a las funciones [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) y [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) para especificar las extensiones. En el \_ modo de asignación anisotrópico de mm, es importante llamar a **SetWindowExtEx** antes de llamar a **SetViewportExtEx**.

Los orígenes de ventanilla y ventana establecen la traducción utilizada en el espacio de página para las transformaciones de espacio de dispositivo. Establezca los orígenes de ventana y ventanilla mediante las funciones [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) y [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . Los orígenes son independientes de las extensiones y una aplicación puede establecerlos independientemente del modo de asignación actual. Cambiar un modo de asignación no afecta a los orígenes establecidos actualmente (aunque puede afectar a las extensiones). Los orígenes se especifican en unidades absolutas a las que no afecta el modo de asignación actual. Para modificar los orígenes, use las funciones [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) y [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) .

La fórmula siguiente muestra las matemáticas implicadas en la conversión de un punto del espacio de página al espacio del dispositivo.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Están implicadas las siguientes variables.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

La misma ecuación con y reemplazando x transforma el componente y de un punto.

En primer lugar, la fórmula desplaza el punto desde su origen de coordenadas. Este valor, que ya no se sesga por el origen, se escala en el sistema de coordenadas de destino por la relación de las extensiones. Por último, el valor escalado se desplaza por el origen de destino a su asignación final.

Las funciones [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) y [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) se pueden usar para convertir de puntos lógicos a puntos de dispositivo y desde puntos de dispositivo a puntos lógicos, respectivamente.

 

 



