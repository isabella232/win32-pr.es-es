---
description: Las cartelera pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante la instalación. Normalmente, las cartelera se utilizan para crear el efecto visual de una presentación o animación que informa al usuario del progreso de una instalación.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Mostrar las cartelera en un cuadro de diálogo no modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155536"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Mostrar las cartelera en un cuadro de diálogo no modal

Las cartelera pueden mostrar una secuencia de imágenes y texto en un cuadro de diálogo durante la instalación. Normalmente, las cartelera se utilizan para crear el efecto visual de una presentación o animación que informa al usuario del progreso de una instalación.

**Para mostrar las cartelera en un cuadro de diálogo no modal**

1.  Incluya un registro en la [tabla de diálogo](dialog-table.md) para el cuadro de diálogo no modal que contiene la cartelera. Una vez que se muestra una cartelera, un cuadro de diálogo no modal devuelve el control al instalador. Esto permite que el instalador procese los mensajes y actualice el cuadro de diálogo y la cartelera. Para crear un cuadro de diálogo no modal, no establezca el bit de estilo del cuadro de diálogo modal en el campo atributos de la [tabla del cuadro de diálogo](dialog-table.md). El siguiente registro de la tabla de cuadro de [diálogo](dialog-table.md) especifica el cuadro de diálogo ActionDialog.

    [Tabla de cuadro de diálogo](dialog-table.md) (parcial)

    | Diálogo\_     | HCentering | VCentering | Ancho | Alto | Atributos | Title  | Controlar \_ primero | \_Valor predeterminado del control | \_Cancelar control |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Acción | Cancelar         | Cancelar           | Cancelar          |

    

     

2.  Agregue un registro a la [tabla de control](control-table.md) para especificar que el cuadro de diálogo muestra una cartelera. El registro define el tamaño y la posición de la región en el cuadro de diálogo donde se mostrarán los controles de la cartelera enumerados en la [tabla BBControl](bbcontrol-table.md) . El siguiente registro de [tabla de control](control-table.md) define la posición y el tamaño de la cartelera en el cuadro de diálogo ActionDialog.

    [Tabla de control](control-table.md) (parcial)

    | Diálogo\_     | Control   | Tipo      | X   | Y   | Ancho | Alto | Atributos |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Valla | Valla | 0   | 110 | 480   | 130    | 1          |

    

     

3.  En la [tabla](billboard-table.md) de la cartelera se enumeran los controles de la cartelera y se especifica cuándo se muestra un control de la cartelera específico. Agregue un registro a la [tabla](billboard-table.md) de la cartelera de cada control de la cartelera. La [tabla](billboard-table.md) de la cartelera vigila los mensajes de progreso enviados durante una instalación. Una cartelera solo se muestra cuando un mensaje de progreso se envía por las acciones enumeradas en la columna Acción de la [tabla cartelera](billboard-table.md)y solo si la característica del \_ campo característica está seleccionada para la instalación. Una vez que se muestra una cartelera, permanece visible hasta que se cubra por otra cartelera o hasta que se cierre el cuadro de diálogo. Si se especifican varias cartelera para una acción, se muestran de una en una en el orden especificado por el campo de ordenación. Por ejemplo, las siguientes entradas de la tabla de la [cartelera](billboard-table.md) muestran primero el BB1 y, a continuación, los controles de la [cartelera](billboard-control.md) de BB2 cuando se ejecuta la acción [InstallFiles](installfiles-action.md) y se ha seleccionado la característica QuickTest para instalarse.

    [Tabla](billboard-table.md) de la cartelera (parcial)

    | Valla | Característica   | Acción       | Ordenación |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  La [tabla BBControl](bbcontrol-table.md) especifica los controles que pertenecen a los [controles](billboard-control.md) de la cartelera que se enumeran en la tabla de la [cartelera](billboard-table.md). El control de [texto](text-control.md), el [control de mapa de bits](bitmap-control.md)y el control de [icono](icon-control.md) son los únicos tipos de controles que pueden ir en una cartelera. Se pueden colocar varios controles en cada cartelera. Escriba el nombre de la cartelera en el \_ campo de la cartelera de la [tabla BBControl](bbcontrol-table.md) exactamente como aparece en la tabla de la [cartelera](billboard-table.md).

    Cada posición del control se especifica como las coordenadas de la esquina superior izquierda del control. El origen del sistema de coordenadas se encuentra en la esquina superior izquierda del control de la cartelera en lugar de en una esquina del cuadro de diálogo. Las coordenadas están en unidades de instalador, no en unidades de cuadro de diálogo. Una unidad de instalador es igual a una duodécima el alto del tamaño de fuente MS Sans Serif de 10 puntos. Los registros de la [tabla BBControl](bbcontrol-table.md) siguiente vinculan los controles a las cartelera.

    [Tabla BBControl](bbcontrol-table.md) (parcial)

    | Valla | BBControl | Tipo   | X   | Y   | Ancho | Alto | Atributos | Texto             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texto      | Texto   | 100 | 30  | 280   | 280    | 3          | Primera cartelera  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Texto      | Texto   | 100 | 30  | 280   | 20     | 3          | Segunda cartelera |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Para mostrar una cartelera en el cuadro de diálogo ActionDialog, debe suscribir el control de la cartelera a [SetProgress ControlEvent,](setprogress-controlevent.md) mediante la adición de un registro a la [tabla EventMapping](eventmapping-table.md). Cuando el instalador publica el SetProgress ControlEvent, que se especifica en la columna de eventos, el instalador establece el atributo de control que se especifica en el campo de atributo. El campo de evento contiene el identificador de cadena (sin comillas) de SetProgress ControlEvent,. El campo de atributo contiene el identificador de cadena (sin comillas) del atributo que se va a establecer. Los \_ campos de cuadro de diálogo y control \_ identifican el control de la cartelera y deben coincidir con los campos de la [tabla de control](control-table.md). Por ejemplo, la siguiente [tabla EventMapping](eventmapping-table.md) suscribe un control a un evento.

    [Tabla EventMapping](eventmapping-table.md) (parcial)

    | Diálogo\_     | control\_ | Evento       | Atributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Valla | SetProgress | Progreso  |

    

     

 

 



