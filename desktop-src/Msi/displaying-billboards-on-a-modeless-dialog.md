---
description: Los paneles pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante una instalación. Normalmente, los paneles de color se usan para crear el efecto visual de una presentación o animación de diapositivas que informa al usuario del progreso de una instalación.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Mostrar paneles en un cuadro de diálogo no modelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158523"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Mostrar paneles en un cuadro de diálogo no modelo

Los paneles pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante una instalación. Normalmente, los paneles de color se usan para crear el efecto visual de una presentación o animación de diapositivas que informa al usuario del progreso de una instalación.

**Para mostrar paneles en un cuadro de diálogo no modelo**

1.  Incluya un registro en la [tabla de diálogos](dialog-table.md) para el cuadro de diálogo modeless que contiene el cuadro de diálogo. Una vez que se muestra un cuadro de diálogo no modelo, devuelve el control al instalador. Esto permite que el instalador procese los mensajes y actualice el cuadro de diálogo y el cuadro de diálogo. Para crear un cuadro de diálogo no modal, no establezca el Bit de estilo de diálogo modal en el campo Atributos de la [tabla de diálogos](dialog-table.md). El siguiente [registro de tabla de](dialog-table.md) diálogo especifica el cuadro de diálogo ActionDialog.

    [Tabla de diálogos](dialog-table.md) (parcial)

    | Diálogo\_     | HCentering | VCentering | Ancho | Alto | Atributos | Título  | Control \_ First | Control \_ predeterminado | Cancelar \_ control |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Acción | Cancelar         | Cancelar           | Cancelar          |

    

     

2.  Agregue un registro a la [tabla de control](control-table.md) para especificar que el cuadro de diálogo muestra un cuadro de diálogo. El registro define el tamaño y la posición de la región en el cuadro de diálogo en el que se van a mostrar los controles de cuadros enumerados en la tabla [BBControl.](bbcontrol-table.md) El siguiente [registro de tabla de](control-table.md) control define la posición y el tamaño de los paneles en el cuadro de diálogo ActionDialog.

    [Tabla de control](control-table.md) (parcial)

    | Diálogo\_     | Control   | Tipo      | X   | Y   | Ancho | Alto | Atributos |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Cartelera | Cartelera | 0   | 110 | 480   | 130    | 1          |

    

     

3.  En [la tabla Deserción](billboard-table.md) se enumeran los controles de los paneles y se especifica cuándo se muestra un control de velocidad específico. Agregue un registro a la tabla [Deón para](billboard-table.md) cada control de velocidad. La [tabla Deón](billboard-table.md) busca mensajes de progreso enviados durante una instalación. Solo se muestra un mensaje de progreso cuando las acciones que aparecen en la columna Acción de la tabla [DeÓn,](billboard-table.md)y solo si la característica del campo Característica está seleccionada para la \_ instalación. Una vez que se muestra un cuadro de diálogo, permanece visible hasta que está cubierto por otro cuadro de diálogo o hasta que se cierra el cuadro de diálogo. Si se especifican varios paneles para una acción, se muestran de uno en uno en el orden especificado por el campo Ordering. Por ejemplo, las siguientes entradas [de table deOnes](billboard-table.md) muestran primero los controles BB1 y BB2 [Controls](billboard-control.md) cuando se ejecuta la acción [InstallFiles](installfiles-action.md) y la característica QuickTest se ha seleccionado para instalarse.

    [Tabla Descaro](billboard-table.md) (parcial)

    | Cartelera | Característica   | Acción       | Ordenación |
    |-----------|-----------|--------------|----------|
    | BB1       | Quicktest | InstallFiles | 1        |
    | BB2       | Quicktest | InstallFiles | 2        |

    

     

4.  La [tabla BBControl](bbcontrol-table.md) especifica los controles que pertenecen a los controles [Deserción](billboard-control.md) que se enumeran en la [tabla Deón.](billboard-table.md) Los [controles Control de texto,](text-control.md)Control [de](bitmap-control.md)mapa de bits y [Control](icon-control.md) de iconos son los únicos tipos de controles que pueden ir en un cuadro de texto. Se pueden colocar varios controles en cada uno de ellos. Escriba el nombre del cuadro en el campo Desenlace de la tabla \_ [BBControl](bbcontrol-table.md) exactamente como aparece en [la tabla Deón.](billboard-table.md)

    Cada posición del control se especifica como coordenadas de la esquina superior izquierda del control. El origen del sistema de coordenadas se encuentra en la esquina superior izquierda del control de velocidad en lugar de en una esquina del cuadro de diálogo. Las coordenadas están en unidades del instalador, no en unidades de diálogo. Una unidad del instalador es igual a la duodécima altura del tamaño de fuente MS Sans Serif de 10 puntos. En la tabla [BBControl siguiente se](bbcontrol-table.md) registra la vinculación de los controles a los discos.

    [Tabla BBControl](bbcontrol-table.md) (parcial)

    | Cartelera | BBControl | Tipo   | X   | Y   | Ancho | Alto | Atributos | Texto             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texto      | Texto   | 100 | 30  | 280   | 280    | 3          | First First(First), First First (  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Texto      | Texto   | 100 | 30  | 280   | 20     | 3          | SecondÓn |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Para mostrar un evento en el cuadro de diálogo ActionDialog, debe suscribir el control de box a [SetProgress ControlEvent](setprogress-controlevent.md) agregando un registro a [la tabla EventMapping](eventmapping-table.md). Cuando el instalador publica el objeto SetProgress ControlEvent que se especifica en la columna Evento, el instalador establece el atributo de control especificado en el campo Atributo. El campo Event contiene el identificador de cadena (sin comillas) de SetProgress ControlEvent. El campo Atributo contiene el identificador de cadena (sin comillas) del atributo que se va a establecer. Los campos \_ Cuadro de diálogo y Control identifican el control \_ Descontrol y deben coincidir con esos campos de la [tabla de control](control-table.md). Por ejemplo, la tabla [EventMapping siguiente](eventmapping-table.md) suscribe un control a un evento.

    [Tabla EventMapping](eventmapping-table.md) (parcial)

    | Diálogo\_     | control\_ | Evento       | Atributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Cartelera | SetProgress | Progreso  |

    

     

 

 



