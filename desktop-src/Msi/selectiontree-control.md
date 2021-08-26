---
description: Este control permite a un usuario cambiar el estado de selección de las características enumeradas en la tabla Características.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: SelectionTree (Control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894a7d90829172c29a6f1df1ffc4139cc0bf6c540bd49193c3cc2f3a396891ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040355"
---
# <a name="selectiontree-control"></a>SelectionTree (Control)

Este control permite a un usuario cambiar el estado de selección de las características enumeradas en la [tabla Característica](feature-table.md). El control está asociado a una propiedad con valores de cadena que el usuario puede establecer mediante un [cuadro de diálogo Examinar](browse-dialog.md). Para asociar el control a una propiedad, escriba el nombre de la propiedad en la columna Propiedad de la [tabla Control](control-table.md).

El control SelectionTree publica automáticamente los siguientes eventos [de control](control-events.md) en Windows XP o sistemas operativos anteriores. El control SelectionTree publica estos eventos cuando se cambia el elemento seleccionado de un nodo a otro. Si el árbol de selección no tiene nodos, el control publica estos eventos y borra el contenido de los controles que se suscriben al evento. No es necesario que estos ControlEvents aparezcan en la [tabla ControlEvent](controlevent-table.md).



| Evento de control                                                 | Descripción                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Publica una cadena de la tabla [UIText](uitext-table.md) que describe el elemento resaltado.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Genera un cuadro de diálogo Examinar que se usa para modificar la ruta de acceso del elemento resaltado.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Publica una cadena de la [tabla Característica](feature-table.md) que describe el elemento resaltado.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Elimina el texto descriptivo o deshabilita los botones de un elemento obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Publica la ruta de acceso del elemento resaltado.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Publica si hay o no una ruta de acceso de selección asociada a la característica seleccionada actualmente. |
| [SelectionSize](selectionsize-controlevent.md)               | Publica el tamaño del elemento resaltado.                                                        |



 

A partir de los sistemas Windows Server 2003, los controles SelectionTree publican todos los eventos de la tabla anterior y, además, publican un [control ControlEvent](doaction-controlevent.md) o [SetProperty ControlEvent.](setproperty-controlevent.md) Los registros se deben agregar a la [tabla ControlEvent para](controlevent-table.md) publicar DoAction o SetProperty ControlEvents.



| Evento de control                               | Descripción                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Notifica al instalador que ejecute una acción personalizada. |
| [SetProperty](setproperty-controlevent.md) | Establece una propiedad en un nuevo valor.                    |



 

A partir Windows installer versión 3.0, los controles [](custom-actions.md) SelectionTree publican un evento que ejecuta acciones personalizadas enumeradas en la [tabla ControlEvent](controlevent-table.md). El control SelectionTree publica este evento cada vez que cambia la selección de características en el control o cada vez que se elige un estado de selección diferente para la característica actual. Las acciones personalizadas se ejecutan cada vez que se publica el evento. El control SelectionTree envía información a la acción personalizada estableciendo los valores de las siguientes propiedades. Todas estas propiedades se borran cuando se cierra el control SelectionTree.

**Windows Installer 2.0:** No se admite. El control SelectionTree no publica el evento y no establece las siguientes propiedades.



| Propiedad                                | Descripción                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | Nombre de la característica seleccionada en el campo Característica de la [tabla Característica](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | Estado de la acción de instalación de la característica seleccionada. El valor puede ser INSTALLSTATE \_ ABSENT, INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE o INSTALLSTATE \_ ADVERTISED. |
| MsiSelectonTreeChildrenCount            | Número de nodos secundarios directos.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Número de nodos secundarios directos que son INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE o INSTALLSTATE \_ ADVERTISED.                                                    |
| MsiSelectionTreeSelectedCost            | Costo de la instalación de la característica seleccionada en unidades de 512 bytes.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Costo de instalar todas las características de elementos secundarios en unidades de 512 bytes.                                                                                              |
| MsiSelectionTreeSelectedPath            | Ruta de acceso donde se instala la característica seleccionada. Solo se define si la característica se instala como INSTALLSTATE \_ LOCAL.                                       |



 

> [!Note]
>
> El control SelectionTree nunca muestra el contenido del campo Texto de la [tabla](control-table.md) Control. En su lugar, este campo especifica el estilo de texto que va a mostrar el control y contiene una descripción del control utilizado por las utilidades de revisión de pantalla. Para establecer la fuente y el estilo de fuente de una cadena de texto, antefirima la cadena de caracteres mostrados con { style} o \\ {&*style*}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usa esa fuente. Las utilidades de revisión de pantalla leen la información siguiente como la descripción del control. Consulte [Accesibilidad.](accessibility.md)

 

## <a name="control-attributes"></a>Atributos de control

Puede usar los atributos siguientes con este control. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nombre de una propiedad indirecta asociada al control . Si se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Si se establece el bit de atributo indirecto, este nombre también es el valor de la propiedad enumerada en la columna Propiedad de la [tabla Control](control-table.md).                                    |
| [Position](position-control-attribute.md)                         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la [tabla Control](control-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nombre de la propiedad asociada a este control. Si no se establece el bit de atributo indirecto, el control muestra o cambia el valor de la propiedad que tiene este nombre. Este atributo se especifica en la columna Property de la [tabla Control](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor actual de la propiedad mostrada o modificada por este control. Si no se establece el bit de atributo indirecto, este es el valor de PropertyName. Si se establece el bit de atributo indirecto, este es el valor de IndirectPropertyName. Si el atributo cambia, el control refleja el nuevo valor.                                                                           |
| [Texto](text-control-attribute.md)                                 |                                  | Muestra texto en lectores de pantalla según el texto especificado en la columna Texto de la [tabla Control](control-table.md). Consulte [Accesibilidad.](accessibility.md)                                                                                                                                                                                                          |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md) para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                     |
| [Habilitado](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control en estado deshabilitado. Control en un estado habilitado.<br/> Incluya este bit en la palabra de bits en la columna Atributos del [control para](control-table.md) habilitar el control en la creación.<br/> También puede habilitar o deshabilitar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                   |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D y bloqueado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                             |
| [Indirecto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | El control muestra o cambia el valor de la propiedad en la columna Propiedad de la [tabla Control](control-table.md). El control muestra o cambia el valor de la propiedad que tiene el identificador enumerado en la columna Propiedad de la tabla Control.<br/> Determina si se hace referencia indirectamente a la propiedad asociada a este control.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                              |
| [Alineado a la derecha](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control se alinea a la derecha.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | La barra de desplazamiento se encuentra en el lado derecho del control. La barra de desplazamiento se encuentra en el lado izquierdo del control.<br/>                                                                                                                                                                                                                                         |
| [Bidi](bidi-control-attribute.md)                                 | 0x000000E0                       | Establezca este valor para una combinación de los atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)y [LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

Este control se puede crear desde la clase WC \_ TREEVIEW mediante la [**función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos **WS \_ BORDER**, **TVS \_ HASLINES,** **TVS \_ HASBUTTONS,** **TVS \_ LINESATROOT,** **TVS \_ DISABLEDRAGDROP,** **TVS \_ SHOWSELALWAYS,** **WS \_ CHILD,** **WS \_ TABSTOP** y **WS \_ GROUP.**

El árbol de selección solo se rellena si se ha llamado a la acción [CostInitialize](costinitialize-action.md) y a la acción [CostFinalize.](costfinalize-action.md)

La siguiente cadena de la [tabla UIText](uitext-table.md) está relacionada con este control.



| Término                                                                                                         | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | Ruta de acceso mostrada para un elemento en estado ausente.<br/> |



 

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

Las cadenas siguientes se usan para explicar la selección actual en [selectionDescription](selectiondescription-controlevent.md) ControlEvent.

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

Las cuatro cadenas localizadas siguientes se usan para dar formato al tamaño de un archivo:

-   Bytes
-   KB
-   MB
-   GB

 

 
