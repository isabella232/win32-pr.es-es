---
description: La tabla de características define la estructura de árbol lógico de las características de y contiene las columnas que se muestran en la tabla siguiente.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tabla de características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa91df750c4994a2d8a2308705213e48c864518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687188"
---
# <a name="feature-table"></a>Tabla de características

La tabla de características define la estructura de árbol lógico de las características de y contiene las columnas que se muestran en la tabla siguiente.



| Columna          | Tipo                         | Clave | Nullable |
|-----------------|------------------------------|-----|----------|
| Característica         | [Identificador](identifier.md) | Y   | N        |
| Característica \_ principal | [Identificador](identifier.md) | N   | Y        |
| Title           | [Texto](text.md)             | N   | Y        |
| Descripción     | [Texto](text.md)             | N   | Y        |
| Pantalla         | [Entero](integer.md)       | N   | Y        |
| Nivel           | [Entero](integer.md)       | N   | N        |
| Directorio\_     | [Identificador](identifier.md) | N   | Y        |
| Atributos      | [Entero](integer.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Ofrecen
</dt> <dd>

La clave principal que se usa para identificar un registro de características específico. El valor de este campo no debe superar una longitud máxima de 38 caracteres.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Característica \_ principal
</dt> <dd>

Una clave opcional de un registro primario de la misma tabla.

La clave apunta a la columna de la característica. Si la característica primaria no está seleccionada, esta característica no está instalada. Un valor null en este campo indica que esta característica no tiene un elemento primario y es un elemento raíz. La \_ columna principal de la característica no debe ser igual a la columna de característica del mismo registro.

> [!Note]  
> La profundidad máxima de cualquier característica es 16. Se produce un [error 2701](windows-installer-error-messages.md) si existe una característica que supera esta profundidad máxima.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titulo
</dt> <dd>

Cadena corta de texto que identifica una característica.

Esta cadena aparece como un elemento mediante el [control SelectionTree](selectiontree-control.md) del cuadro de [diálogo de selección](selection-dialog.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Cadena de texto más larga que describe una característica.

El [control de texto](text-control.md) del cuadro de [diálogo de selección](selection-dialog.md)muestra esta cadena traducible.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Muestra
</dt> <dd>

El número de este campo especifica el orden en el que se mostrará la característica en la interfaz de usuario.

El valor también determina si la característica se muestra o no de forma inicialmente expandida o contraída. Si el valor es null o 0 (cero), el registro no se muestra.

-   Si el valor es impar, el nodo de características se expande inicialmente.
-   Si el valor es par, el nodo de característica se contrae inicialmente.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Dosis
</dt> <dd>

El nivel de instalación inicial de esta característica. El procesamiento de la [tabla de condición](condition-table.md) puede modificar el valor de nivel.

Un nivel de instalación de 0 (cero) deshabilita el elemento y evita que se muestre. Una característica con un nivel de instalación de 0 (cero) no se instala durante la instalación, incluidas las instalaciones administrativas. Para obtener más información, consulte la información sobre el nivel de instalación en la sección Comentarios de este tema.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

La \_ columna directorio especifica el nombre de un directorio que se puede configurar mediante un [cuadro de diálogo de selección](selection-dialog.md).

Dado que este campo es una clave en la [tabla del directorio](directory-table.md), el directorio especificado debe aparecer en la primera columna de la tabla del directorio. Debe escribir una [propiedad pública](public-properties.md) en esta columna para que el directorio sea configurable y para mostrar un botón **examinar** en el [cuadro de diálogo de selección](selection-dialog.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

La opción de ejecución remota para las características que no están instaladas y para las que no se realiza ninguna solicitud de estado de característica mediante cualquiera de las siguientes propiedades.

-   [**ADDLOCAL (propiedad)**](addlocal.md)
-   [**Propiedad ADDSOURCE**](addsource.md)
-   [**Propiedad ADDDEFAULT**](adddefault.md)
-   [**Propiedad COMPADDLOCAL**](compaddlocal.md)
-   [**Propiedad COMPADDSOURCE**](compaddsource.md)
-   [**Propiedad FILEADDLOCAL**](fileaddlocal.md)
-   [**Propiedad FILEADDSOURCE**](fileaddsource.md)
-   [**QUITAR propiedad**](remove.md)
-   [**REINSTALL (propiedad)**](reinstall.md)
-   [**Propiedad de anuncio**](advertise.md)

Agregue los bits indicados al valor total de esta columna para incluir una opción de ejecución remota.

-   Si este campo está en blanco, el valor predeterminado es 0 (cero), msidbFeatureAttributesFavorLocal.
-   Si el nivel de instalación de características es 0 (cero), o mayor o igual que el nivel de instalación actual, no se realiza ningún cambio en el estado de la característica.



| Nombre                                         | Decimal | Hexadecimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | Los componentes de esta característica que no están marcados para la instalación desde el origen se instalan localmente. Un componente compartido por dos o más características, algunos de los cuales están establecidos en msidbFeatureAttributesFavorLocal y otros en msidbFeatureAttributesFavorSource, se instala localmente. Los componentes marcados como msidbComponentAttributesSourceOnly en la [tabla componente](component-table.md) siempre se ejecutan desde el CD o el servidor de origen. Los bits msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource funcionan con características no enumeradas por la [**propiedad de anuncio**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | Los componentes de esta característica no marcados para la instalación local se instalan para ejecutarse desde el CD-ROM o el servidor de origen. Un componente compartido por dos o más características, algunos de los cuales están establecidos en msidbFeatureAttributesFavorLocal y otros en msidbFeatureAttributesFavorSource, se instala para ejecutarse localmente. Los componentes marcados como msidbComponentAttributesLocalOnly en la [tabla componente](component-table.md) siempre se instalan de forma local. Los bits msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource funcionan con características no enumeradas por la [**propiedad de anuncio**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Establezca este atributo y el estado de la característica es el mismo que el estado del elemento primario de la característica. No puede usar esta opción si la característica se encuentra en la raíz de un árbol de características. Omita este atributo y el estado de la característica se determina según msidbFeatureAttributesDisallowAdvertise y msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/> Para garantizar que el estado de la característica secundaria siempre sigue el estado de su elemento primario, incluso si el elemento secundario y el elemento primario están establecidos inicialmente en ausente en el control SelectionTree, debe incluir msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent en los atributos de la característica secundaria.<br/> Tenga en cuenta que si establece msidbFeatureAttributesFollowParent sin establecer msidbFeatureAttributesUIDisallowAbsent, el instalador no puede forzar la característica secundaria fuera del estado ausente. En este caso, la característica secundaria coincide con el estado de instalación del elemento primario solo si el elemento secundario está establecido en un valor distinto de ausente.<br/> Establezca msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para asegurarse de que una característica secundaria sigue el estado de la característica primaria.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Establezca este atributo y el estado de la característica es anunciar. Si la característica aparece en la lista por la [**propiedad ADDDEFAULT**](adddefault.md) , este bit se omite y el estado de la característica se determina según MsidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource. Omita este atributo y el estado de la característica se determina según msidbFeatureAttributesDisallowAdvertise y msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Tenga en cuenta que este bit solo funciona con las características que se enumeran en la [**propiedad de anuncio**](advertise.md). Establezca este atributo para evitar que se anuncie la característica.<br/> Establezca este atributo y, si la característica enumerada no es un elemento primario o secundario, la característica se instala según msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/> Establezca este atributo para el elemento primario de una característica enumerada y el elemento primario está instalado.<br/> Establezca este atributo para el elemento secundario de una característica enumerada y el estado del elemento secundario no está presente.<br/> Omita este atributo y, si la característica enumerada no es un elemento primario o secundario, se anuncia el estado de la característica.<br/> Omita este atributo y, si la característica enumerada es un elemento primario o secundario, se anuncia el estado de ambas características.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Establezca este atributo y la interfaz de usuario no muestra una opción para cambiar el estado de la característica a ausente. Al establecer este atributo se fuerza la característica al estado de la instalación, independientemente de si la característica está visible en la interfaz de usuario. Omita este atributo y la interfaz de usuario muestra una opción para cambiar el estado de la característica a ausente.<br/> Establezca msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para asegurarse de que una característica secundaria sigue el estado de la característica primaria.<br/> Establecer este atributo no solo afecta a la interfaz de usuario, sino que también fuerza la característica al estado de instalación si la característica está visible en la interfaz de usuario o no.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | Establezca este atributo y el anuncio está deshabilitado para la característica si el Shell del sistema operativo no admite descriptores de Windows Installer. Omitir este atributo y no se deshabilita el anuncio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Algunos atributos son exclusivos entre sí. El intento de establecer estos atributos juntos en la misma característica hace que el paquete de instalación produzca un error en la [**validación del paquete**](package-validation.md).

-   No use msidbFeatureAttributesFavorAdvertise con msidbFeatureAttributesDisallowAdvertise.
-   No use msidbFeatureAttributesNoUnsupportedAdvertise con msidbFeatureAttributesDisallowAdvertise juntos.
-   No use msidbFeatureAttributesFollowParent con msidbFeatureAttributesFavorSource.
-   Tenga en cuenta que los valores msidbFeatureAttributesFollowParent y msidbFeatureAttributesFavorLocal son mutuamente excluyentes. Si se usa el valor msidbFeatureAttributesFollowParent, se supone que el valor msidbFeatureAttributesFavorLocal no existe.

</dd> </dl>

Tenga en cuenta que si se instala una característica secundaria, también se instalará su característica primaria. Si se instala una característica primaria, su característica secundaria no se instala necesariamente a menos que se establezcan los atributos msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent. Esta relación jerárquica de la instalación de las características de elementos primarios y secundarios también se usa para las instalaciones e instalaciones de GUI que usan propiedades de línea de comandos.

## <a name="remarks"></a>Observaciones

Se agregan varias columnas temporales adicionales a esta tabla cuando se carga en memoria para los cálculos utilizados por la selección de costos y la interfaz de usuario (UI).

Un componente puede compartirse entre dos o más características o aplicaciones. Si dos o más características hacen referencia al mismo componente, ese componente se selecciona para su instalación si se selecciona cualquiera de las características asociadas. Esto también puede ser el motivo por el que las características secundarias no se desinstalan cuando se quita una característica primaria. Si la característica secundaria consta de componentes que son necesarios para otras características o aplicaciones, el Windows Installer no quita la característica secundaria.

Para obtener más información, consulte [controlar los Estados de selección de características](controlling-feature-selection-states.md).

Nivel de instalación:

-   En cualquier instalación, hay un nivel de instalación definido, que es un valor entero comprendido entre 1 y 32.767. El valor inicial viene determinado por la [**propiedad INSTALLLEVEL**](installlevel.md), que se establece en la [tabla de propiedades](property-table.md).
-   Una característica se instala solo si el valor de nivel de característica es menor o igual que el nivel de instalación actual. La interfaz de usuario se puede crear de modo que, cuando se inicializa la instalación, el instalador permite al usuario modificar el nivel de instalación de cualquier característica en la tabla de características. Por ejemplo, un autor puede definir valores de nivel de instalación que representen opciones de instalación específicas, como **personalizado**, **típico** o **mínimo**, y, a continuación, crear un cuadro de diálogo que use [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) para permitir que el usuario seleccione uno de estos Estados.
-   En función del estado que seleccione el usuario, el cuadro de diálogo establece la propiedad nivel de instalación en el valor correspondiente. Si el autor asigna un nivel **típico** de 100 y el usuario selecciona **típico**, solo se instalan las características con un nivel de 100 o menos. Además, la opción **personalizada** puede conducir a otro cuadro de diálogo que contiene un [control SelectionTree](selectiontree-control.md). A continuación, el control SelectionTree permite al usuario cambiar individualmente si está instalada cada característica.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




