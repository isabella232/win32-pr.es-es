---
description: Los paneles pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante una instalación. Normalmente, se usan paneles para crear el efecto visual de una presentación o animación de diapositivas que informa al usuario del progreso de una instalación.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Mostrar paneles en un cuadro de diálogo modeless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badf81e2b6d0131d1224f10b19e8de3c06f173ef91e3b08f3a45f31aef52be11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086175"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Mostrar paneles en un cuadro de diálogo modeless

Los paneles pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante una instalación. Normalmente, se usan paneles para crear el efecto visual de una presentación o animación de diapositivas que informa al usuario del progreso de una instalación.

**Para mostrar paneles de pantalla en un cuadro de diálogo de modelado**

1.  Incluya un registro en la [tabla de diálogos](dialog-table.md) para el cuadro de diálogo modeless que contiene el tablero. Una vez que se muestra un cuadro de diálogo de modelo, devuelve el control al instalador. Esto permite que el instalador procese los mensajes y actualice el cuadro de diálogo y el cuadro de diálogo. Para crear un cuadro de diálogo no modal, no establezca el Bit de estilo de diálogo modal en el campo Atributos de la tabla [de diálogos](dialog-table.md). El siguiente [registro de tabla de](dialog-table.md) diálogos especifica el cuadro de diálogo ActionDialog.

    [Tabla de diálogos](dialog-table.md) (parcial)

    | Diálogo\_     | HCentering | VCentering | Ancho | Alto | Atributos | Título  | Control \_ First | Control \_ predeterminado | Cancelar \_ control |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Acción | Cancelar         | Cancelar           | Cancelar          |

    

     

2.  Agregue un registro a la [tabla de control](control-table.md) para especificar que el cuadro de diálogo muestra un cuadro de diálogo. El registro define el tamaño y la posición de la región en el cuadro de diálogo en el que se van a mostrar los controles de paneles enumerados en la [tabla BBControl.](bbcontrol-table.md) El siguiente [registro de tabla de](control-table.md) control define la posición y el tamaño del tablero en el cuadro de diálogo ActionDialog.

    [Tabla de control](control-table.md) (parcial)

    | Diálogo\_     | Control   | Tipo      | X   | Y   | Ancho | Alto | Atributos |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Cartelera | Cartelera | 0   | 110 | 480   | 130    | 1          |

    

     

3.  En [la tabla Deserción](billboard-table.md) se enumeran los controles de los paneles y se especifica cuándo se muestra un control específico de la ciudad. Agregue un registro a la tabla [Descándalo para](billboard-table.md) cada control de paneles. La [tabla Descándalo](billboard-table.md) busca los mensajes de progreso enviados durante una instalación. Solo se muestra un anuncio cuando se envía un mensaje de progreso por las acciones enumeradas en la columna Acción de la tabla [Desfila,](billboard-table.md)y solo si la característica del campo Característica está seleccionada para la \_ instalación. Una vez que se muestra una pancarla, permanece visible hasta que se cubre con otro cuadro de diálogo o hasta que se cierra el cuadro de diálogo. Si se especifican varios paneles para una acción, se muestran de uno en uno en el orden especificado por el campo Ordering. Por ejemplo, en las siguientes entradas [de Table de Bbs](billboard-table.md) primero se muestra BB1 y, después, los controles [Bb2 Desfiladores](billboard-control.md) cuando se ejecuta la acción [InstallFiles](installfiles-action.md) y se ha seleccionado la característica QuickTest para instalarse.

    [Tabla Descándalo](billboard-table.md) (parcial)

    | Cartelera | Característica   | Acción       | Ordenación |
    |-----------|-----------|--------------|----------|
    | BB1       | Quicktest | InstallFiles | 1        |
    | BB2       | Quicktest | InstallFiles | 2        |

    

     

4.  La [tabla BBControl](bbcontrol-table.md) especifica los controles que pertenecen a los controles [de la lista de controles de la](billboard-control.md) lista de [Paneles.](billboard-table.md) El [control de texto](text-control.md), el control de [mapa](bitmap-control.md)de bits y el [control](icon-control.md) de icono son los únicos tipos de controles que pueden ir en un panel. Se pueden colocar varios controles en cada uno de los paneles. Escriba el nombre de la pantalla en el campo De la tabla \_ [BBControl](bbcontrol-table.md) exactamente como aparece en la tabla de [la ciudad.](billboard-table.md)

    Cada posición del control se especifica como coordenadas de la esquina superior izquierda del control. El origen del sistema de coordenadas se encuentra en la esquina superior izquierda del control de paneles en lugar de en una esquina del cuadro de diálogo. Las coordenadas están en unidades del instalador, no en unidades de diálogo. Una unidad del instalador es igual a una duodécima parte del alto del tamaño de fuente MS Sans Serif de 10 puntos. En la tabla [BBControl siguiente se](bbcontrol-table.md) registra el vínculo de los controles a los paneles.

    [Tabla BBControl](bbcontrol-table.md) (parcial)

    | Cartelera | BBControl | Tipo   | X   | Y   | Ancho | Alto | Atributos | Texto             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texto      | Texto   | 100 | 30  | 280   | 280    | 3          | First Billboard  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Texto      | Texto   | 100 | 30  | 280   | 20     | 3          | Second Billboard |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Para mostrar un panel en el cuadro de diálogo ActionDialog, debe suscribir el control de box a [SetProgress ControlEvent](setprogress-controlevent.md) agregando un registro a [la tabla EventMapping](eventmapping-table.md). Cuando el instalador publica el control SetProgress que se especifica en la columna Evento, el instalador establece el atributo de control especificado en el campo Atributo . El campo Evento contiene el identificador de cadena (sin comillas) del control SetProgress. El campo Atributo contiene el identificador de cadena (sin comillas) del atributo que se va a establecer. Los campos Dialog \_ y Control identifican el control \_ Descontrol y deben coincidir con esos campos de la [tabla de control](control-table.md). Por ejemplo, la tabla [EventMapping siguiente](eventmapping-table.md) suscribe un control a un evento.

    [Tabla EventMapping](eventmapping-table.md) (parcial)

    | Diálogo\_     | control\_ | Evento       | Atributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Cartelera | SetProgress | Progreso  |

    

     

 

 



