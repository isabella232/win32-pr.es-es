---
description: Este control permite a un usuario cambiar el estado de selección de las características enumeradas en la tabla de características.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Control SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5287736c3293c736d6d392ce8532b76ee7b62ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913454"
---
# <a name="selectiontree-control"></a>Control SelectionTree

Este control permite a un usuario cambiar el estado de selección de las características enumeradas en la [tabla de características](feature-table.md). El control está asociado a una propiedad con valores de cadena que el usuario puede establecer mediante un [cuadro de diálogo de exploración](browse-dialog.md). Puede asociar el control a una propiedad escribiendo el nombre de la propiedad en la columna de propiedades de la [tabla de control](control-table.md).

El control SelectionTree publica automáticamente los siguientes [eventos de control](control-events.md) en Windows XP o sistemas operativos anteriores. El control SelectionTree publica estos eventos cuando se cambia el elemento seleccionado de un nodo a otro. Si el árbol de selección no tiene ningún nodo, el control publica estos eventos y borra el contenido de los controles que se suscriben al evento. No es necesario que estos ControlEvents aparezcan en la [tabla ControlEvent,](controlevent-table.md).



| Evento de control                                                 | Descripción                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Publica una cadena de la [tabla UIText](uitext-table.md) que describe el elemento resaltado.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Genera un cuadro de diálogo de exploración que se usa para modificar la ruta de acceso del elemento resaltado.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Publica una cadena de la [tabla de características](feature-table.md) que describe el elemento resaltado.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Elimina el texto descriptivo o deshabilita los botones de un elemento obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Publica la ruta de acceso del elemento resaltado.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Publica si hay o no una ruta de acceso de selección asociada a la característica seleccionada actualmente. |
| [SelectionSize](selectionsize-controlevent.md)               | Publica el tamaño del elemento resaltado.                                                        |



 

A partir de los sistemas Windows Server 2003, los controles SelectionTree publican todos los eventos de la tabla anterior y, además, publican una [acción ControlEvent,](doaction-controlevent.md) o una [ControlEvent, SetProperty](setproperty-controlevent.md). Los registros se deben agregar a la [tabla ControlEvent,](controlevent-table.md) para publicar OnAction o SetProperty ControlEvents.



| Evento de control                               | Descripción                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Notifica al instalador que ejecute una acción personalizada. |
| [SetProperty](setproperty-controlevent.md) | Establece una propiedad en un nuevo valor.                    |



 

A partir de Windows Installer versión 3,0, los controles SelectionTree publican un evento que ejecuta [acciones personalizadas](custom-actions.md) enumeradas en la [tabla ControlEvent,](controlevent-table.md). El control SelectionTree publica este evento cada vez que se cambia la selección de características en el control o cuando se elige un estado de selección diferente para la característica actual. Las acciones personalizadas se ejecutan cada vez que se publica el evento. El control SelectionTree envía información a la acción personalizada estableciendo los valores de las siguientes propiedades. Todas estas propiedades se borran cuando el control SelectionTree está cerrado.

**Windows Installer 2,0:** No compatible. El control SelectionTree no publica el evento y no establece las siguientes propiedades.



| Propiedad                                | Descripción                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Nombre de la característica seleccionada en el campo de característica de la [tabla de características](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | El estado de la acción de instalación de la característica seleccionada. El valor puede ser INSTALLSTATE \_ ausente, installstate \_ local, installstate \_ Source o installstate \_ anunciado. |
| MsiSelectonTreeChildrenCount            | Número de nodos secundarios directos.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Número de nodos secundarios directos que son INSTALLSTATE \_ local, installstate \_ Source o installstate \_ anunciado.                                                    |
| MsiSelectionTreeSelectedCost            | Costo de instalar la característica seleccionada en unidades de 512 bytes.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Costo de instalar todas las características secundarias en unidades de 512 bytes.                                                                                              |
| MsiSelectionTreeSelectedPath            | Ruta de acceso en la que se va a instalar la característica seleccionada. Solo se define si la característica se instala como INSTALLSTATE \_ local.                                       |



 

> [!Note]
>
> El control SelectionTree nunca muestra el contenido del campo de texto de la [tabla de control](control-table.md) . En su lugar, este campo especifica el estilo de texto que va a mostrar el control y contiene una descripción del control utilizado por las utilidades de revisión de pantalla. Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&*Style*}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se utiliza esa fuente. La información que aparece a continuación se lee mediante las utilidades de revisión de pantalla como Descripción del control. Vea [accesibilidad](accessibility.md).

 

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nombre de una propiedad indirecta asociada al control. Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad que aparece en la columna de propiedades de la [tabla de control](control-table.md).                                    |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna de propiedades de la [tabla de control](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si cambia el atributo, el control refleja el nuevo valor.                                                                           |
| [Texto](text-control-attribute.md)                                 |                                  | Muestra texto en screenreaders según el texto escrito en la columna de texto de la [tabla de control](control-table.md). Vea [accesibilidad](accessibility.md).                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md) para que el control sea visible u oculto en el momento de su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bit de la columna Attributes del [control](control-table.md) para habilitar el control al crearlo.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                             |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna de propiedades de la [tabla de control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador que aparece en la columna de propiedades de la tabla de control.<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control está alineado a la derecha.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                         |
| [Lenguas](bidi-control-attribute.md)                                 | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase de TREEVIEW de WC mediante \_ la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos **WS \_ Border**, **televisores \_ HASLINES**, **televisores \_ HASBUTTONS**, **TV \_ LINESATROOT**, **televisores \_ DISABLEDRAGDROP**, **TV \_ SHOWSELALWAYS**, **WS \_ Child**, **WS \_ TABSTOP** y **WS \_ Group** .

El árbol de selección solo se rellena si se ha llamado a la acción [CostInitialize](costinitialize-action.md) y a la [acción CostFinalize](costfinalize-action.md) .

La siguiente cadena de la [tabla UIText](uitext-table.md) está relacionada con este control.



| Término                                                                                                         | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | La ruta de acceso que se muestra para un elemento en el estado ausente.<br/> |



 

Las seis cadenas siguientes se usan para mostrar el número de elementos secundarios seleccionados y el tamaño asociado al elemento resaltado:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

Las cadenas siguientes se usan para mostrar las opciones de selección disponibles para un elemento en un menú emergente:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

Las cadenas siguientes se usan para explicar la selección actual en [SelectionDescription](selectiondescription-controlevent.md) ControlEvent,.

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

Las cuatro cadenas traducidas siguientes se usan para dar formato al tamaño de un archivo:

-   Bytes
-   KB
-   MB
-   GB

 

 
