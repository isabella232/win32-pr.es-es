---
description: Los modos de asignación se describen en la tabla siguiente.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modos de asignación y traducciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242ba699a8ec7289495cbcdff33e940460b20bcabffa373d5c792b1aee0fe9d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760162"
---
# <a name="mapping-modes-and-translations"></a>Modos de asignación y traducciones

Los modos de asignación se describen en la tabla siguiente.



| Modo de asignación    | Descripción                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ ANISOTROPIC | Cada unidad del espacio de página se asigna a una unidad especificada por la aplicación en el espacio del dispositivo. El eje puede o no escalarse igual (por ejemplo, un círculo dibujado en el espacio mundial puede parecer una elipse cuando se representa en un dispositivo determinado). La aplicación también especifica la orientación del eje.                  |
| MM \_ HIENGLISH   | Cada unidad del espacio de página se asigna a 0,001 pulgadas de espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                                 |
| MM \_ HIMETRIC    | Cada unidad del espacio de página se asigna a 0,01 milímetros en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                            |
| MM \_ ISOTROPIC   | Cada unidad del espacio de página se asigna a una unidad definida por la aplicación en el espacio del dispositivo. Los ejes siempre se escalan por igual. La aplicación puede especificar la orientación de los ejes.                                                                                                                                     |
| MM \_ LOENGLISH   | Cada unidad del espacio de página se asigna a 0,01 pulgadas de espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                                  |
| MM \_ LOMETRIC    | Cada unidad del espacio de página se asigna a 0,1 milímetros en el espacio del dispositivo. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                                             |
| MM \_ TEXT        | Cada unidad del espacio de página se asigna a un píxel; es decir, no se realiza ningún escalado. Cuando no hay ninguna traducción en vigor (este es el valor predeterminado), el espacio de página en el modo de asignación MM \_ TEXT es equivalente al espacio del dispositivo físico. El valor de x aumenta de izquierda a derecha. El valor de y aumenta de arriba abajo. |
| MM \_ TWIPS       | Cada unidad en el espacio de página se asigna a un desenlaz de punto de una impresora (1/1440 pulgadas). El valor de x aumenta de izquierda a derecha. El valor de y aumenta de abajo a arriba.                                                                                                                                           |



 

Para establecer un modo de asignación, llame a la [**función SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) Recupere el modo de asignación actual para un controlador de dominio mediante una llamada a [**la función GetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)

Las transformaciones de espacio de página a espacio del dispositivo constan de valores calculados a partir de los puntos dados por la ventana y la ventanilla. En este contexto, la ventana hace referencia al sistema de coordenadas lógico del espacio de página, mientras que la ventanilla hace referencia al sistema de coordenadas del dispositivo del espacio del dispositivo. Cada ventana y ventanilla consta de un origen, una extensión horizontal ("x") y una extensión vertical ("y"). Los parámetros de ventana están en coordenadas lógicas; la ventanilla en coordenadas del dispositivo (píxeles). El sistema combina los orígenes y las extensiones de la ventana y la ventanilla para crear la transformación. Esto significa que la ventana y la ventanilla especifican cada uno la mitad de los factores necesarios para definir la transformación utilizada para asignar puntos del espacio de página al espacio del dispositivo. Por lo tanto, el sistema asigna el origen de la ventana al origen de la ventanilla y las extensiones de ventana a las extensiones de la ventanilla, como se muestra en la ilustración siguiente.

![ilustración que muestra un origen de ventana en el espacio de página y un origen de punto de vista en el espacio del dispositivo](images/cstrn-15.png)

Las extensiones de ventana y ventanilla establecen una relación o un factor de escalado que se usa en las transformaciones espacio de página a espacio del dispositivo. Para los seis modos de asignación predefinidos (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC, MM TEXT y MM TWIPS), el sistema establece las extensiones cuando se llama a \_ \_ \_ [**SetMapMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) No se pueden cambiar. Los otros dos modos de asignación (MM \_ ISOTROPIC y MM \_ ANISOTROPIC) requieren que se especifiquen las extensiones. Para ello, llame a **SetMapMode** para establecer el modo adecuado y, a continuación, llame a las funciones [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) y [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) para especificar las extensiones. En el modo de asignación MM ISOTROPIC, es importante llamar a \_ **SetWindowExtEx** antes de llamar a **SetViewportExtEx**.

Los orígenes de ventana y ventanilla establecen la traducción que se usa en las transformaciones de espacio de página a espacio del dispositivo. Establezca los orígenes de ventana y ventanilla mediante las [**funciones SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) [**y SetViewportOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) Los orígenes son independientes de las extensiones y una aplicación puede establecerlas independientemente del modo de asignación actual. Cambiar un modo de asignación no afecta a los orígenes establecidos actualmente (aunque puede afectar a las extensiones). Los orígenes se especifican en unidades absolutas a las que no afecta el modo de asignación actual. Para modificar los orígenes, use las [**funciones OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) [**y OffsetViewportOrgEx.**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)

En la fórmula siguiente se muestran los cálculos matemáticos implicados en la conversión de un punto del espacio de página al espacio del dispositivo.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Las siguientes variables están implicadas.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

La misma ecuación con y reemplazando x transforma el componente yde un punto.

La fórmula desplaza primero el punto desde su origen de coordenada. Este valor, ya no sesgado por el origen, se escala en el sistema de coordenadas de destino por la proporción de las extensiones. Por último, el valor escalado se desplaza por el origen de destino a su asignación final.

Las [**funciones LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) y [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) se pueden usar para convertir de puntos lógicos a puntos de dispositivo y de puntos de dispositivo a puntos lógicos, respectivamente.

 

 



