---
description: La tabla de características define la estructura de árbol lógico de las características y contiene las columnas que se muestran en la tabla siguiente.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tabla de características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa91df750c4994a2d8a2308705213e48c864518
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158410"
---
# <a name="feature-table"></a>Tabla de características

La tabla de características define la estructura de árbol lógico de las características y contiene las columnas que se muestran en la tabla siguiente.



| Columna          | Tipo                         | Clave | Nullable |
|-----------------|------------------------------|-----|----------|
| Característica         | [Identificador](identifier.md) | Y   | N        |
| Elemento \_ primario de la característica | [Identificador](identifier.md) | N   | Y        |
| Título           | [Texto](text.md)             | N   | Y        |
| Descripción     | [Texto](text.md)             | N   | Y        |
| Mostrar         | [Entero](integer.md)       | N   | Y        |
| Nivel           | [Entero](integer.md)       | N   | N        |
| Directorio\_     | [Identificador](identifier.md) | N   | Y        |
| Atributos      | [Entero](integer.md)       | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Característica
</dt> <dd>

Clave principal que se usa para identificar un registro de características específico. El valor de este campo no debe superar una longitud máxima de 38 caracteres.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Elemento \_ primario de la característica
</dt> <dd>

Clave opcional de un registro primario en la misma tabla.

La clave apunta a la columna Característica. Si la característica primaria no está seleccionada, esta característica no está instalada. Un valor NULL en este campo indica que esta característica no tiene un elemento primario y es un elemento raíz. La columna \_ Elemento primario de la característica no debe ser igual a la columna Característica del mismo registro.

> [!Note]  
> La profundidad máxima de cualquier característica es 16. Se [produce un error 2701](windows-installer-error-messages.md) si existe una característica que supera esta profundidad máxima.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Cadena de texto corta que identifica una característica.

El control [SelectionTree](selectiontree-control.md) del cuadro de diálogo de selección muestra esta [cadena como un elemento](selection-dialog.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Cadena de texto más larga que describe una característica.

El control Texto del cuadro de diálogo de selección muestra esta [cadena localizable.](selection-dialog.md) [](text-control.md)

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Monitor
</dt> <dd>

El número de este campo especifica el orden en el que se mostrará la característica en la interfaz de usuario.

El valor también determina si la característica se muestra o no expandida o contraida inicialmente. Si el valor es NULL o 0 (cero), no se muestra el registro.

-   Si el valor es impar, el nodo de característica se expande inicialmente.
-   Si el valor es par, el nodo de característica se contrae inicialmente.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Nivel
</dt> <dd>

Nivel de instalación inicial de esta característica. El procesamiento [de la tabla de](condition-table.md) condiciones puede modificar el valor de nivel.

Un nivel de instalación de 0 (cero) deshabilita el elemento e impide que se muestre. Una característica con un nivel de instalación de 0 (cero) no se instala durante ninguna instalación, incluidas las instalaciones administrativas. Para obtener más información, vea la información "Nivel de instalación" en la sección Comentarios de este tema.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directorio\_
</dt> <dd>

La columna \_ Directorio especifica el nombre de un directorio que se puede configurar mediante un cuadro de diálogo de [selección](selection-dialog.md).

Dado que este campo es una clave en la tabla [de](directory-table.md)directorios , el directorio especificado debe aparecer en la primera columna de la tabla de directorios. Debe escribir una propiedad [pública en](public-properties.md) esta columna para que el directorio sea configurable y para mostrar un **botón** Examinar en el cuadro de [diálogo Selección](selection-dialog.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Opción de ejecución remota para las características que no están instaladas y para las que no se realiza ninguna solicitud de estado de característica mediante cualquiera de las propiedades siguientes.

-   [**Propiedad ADDLOCAL**](addlocal.md)
-   [**Propiedad ADDSOURCE**](addsource.md)
-   [**Propiedad ADDDEFAULT**](adddefault.md)
-   [**ComPADDLOCAL, propiedad**](compaddlocal.md)
-   [**ComPADDSOURCE, propiedad**](compaddsource.md)
-   [**Propiedad FILEADDLOCAL**](fileaddlocal.md)
-   [**Propiedad FILEADDSOURCE**](fileaddsource.md)
-   [**Remove (propiedad)**](remove.md)
-   [**REINSTALL( Propiedad)**](reinstall.md)
-   [**PROPIEDAD ADVERTISE**](advertise.md)

Agregue los bits indicados al valor total de esta columna para incluir una opción de ejecución remota.

-   Si este campo está en blanco, el valor predeterminado es 0 (cero), msidbFeatureAttributesFavorLocal.
-   Si el nivel de instalación de la característica es 0 (cero), o mayor o igual que el nivel de instalación actual, no se realiza ningún cambio en el estado de la característica.



| Nombre                                         | Decimal | Hexadecimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | Los componentes de esta característica que no están marcados para la instalación desde el origen se instalan localmente. Un componente compartido por dos o más características, algunas de las cuales se establecen en msidbFeatureAttributesFavorLocal y otras en msidbFeatureAttributesFavorSource, se instala localmente. Los componentes marcados como msidbComponentAttributesSourceOnly en la [tabla de](component-table.md) componentes siempre se ejecutan desde el CD o servidor de origen. Los bits msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource funcionan con características no enumeradas por la [**propiedad ADVERTISE**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | Los componentes de esta característica no marcados para la instalación local se instalan para ejecutarse desde el CD-ROM o el servidor de origen. Un componente compartido por dos o más características, algunas de las cuales se establecen en msidbFeatureAttributesFavorLocal y otras en msidbFeatureAttributesFavorSource, se instala para ejecutarse localmente. Los componentes marcados como msidbComponentAttributesLocalOnly en la [tabla de](component-table.md) componentes siempre se instalan localmente. Los bits msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource funcionan con características no enumeradas por la [**propiedad ADVERTISE**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Establezca este atributo y el estado de la característica sea el mismo que el estado del elemento primario de la característica. No puede usar esta opción si la característica se encuentra en la raíz de un árbol de características. Omita este atributo y el estado de la característica se determina según msidbFeatureAttributesDisallowAdvertise y msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/> Para garantizar que el estado de la característica secundaria siempre sigue el estado de su elemento primario, incluso cuando el elemento secundario y el elemento primario se establecen inicialmente en absent en el control SelectionTree, debe incluir msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent en los atributos de la característica secundaria.<br/> Tenga en cuenta que si establece msidbFeatureAttributesFollowParent sin establecer msidbFeatureAttributesUIDisallowAbsent, el instalador no puede forzar que la característica secundaria salga del estado ausente. En este caso, la característica secundaria coincide con el estado de instalación del elemento primario solo si el elemento secundario está establecido en un valor distinto de absent.<br/> Establezca msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para asegurarse de que una característica secundaria sigue el estado de la característica primaria.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Establezca este atributo y el estado de la característica es Anunciar. Si la propiedad [**ADDDEFAULT**](adddefault.md) enumera la característica, este bit se omite y el estado de la característica se determina según msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource. Omita este atributo y el estado de la característica se determina según msidbFeatureAttributesDisallowAdvertise y msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Tenga en cuenta que este bit solo funciona con características enumeradas por la [**propiedad ADVERTISE**](advertise.md). Establezca este atributo para evitar que se anuncie la característica.<br/> Establezca este atributo y, si la característica enumerada no es un elemento primario o secundario, la característica se instala según msidbFeatureAttributesFavorLocal y msidbFeatureAttributesFavorSource.<br/> Establezca este atributo para el elemento primario de una característica enumerada y el elemento primario está instalado.<br/> Establezca este atributo para el elemento secundario de una característica enumerada y el estado del elemento secundario sea Absent.<br/> Omita este atributo y, si la característica enumerada no es un elemento primario o secundario, el estado de la característica es Anunciar.<br/> Omita este atributo y, si la característica enumerada es primaria o secundaria, el estado de ambas características es Anunciar.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Establezca este atributo y la interfaz de usuario no muestra una opción para cambiar el estado de la característica a Absent. Al establecer este atributo se fuerza la característica al estado de instalación, independientemente de si la característica está visible o no en la interfaz de usuario. Omita este atributo y la interfaz de usuario mostrará una opción para cambiar el estado de la característica a Absent.<br/> Establezca msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para asegurarse de que una característica secundaria sigue el estado de la característica primaria.<br/> Establecer este atributo no solo afecta a la interfaz de usuario, sino que también obliga a la característica al estado de instalación tanto si la característica está visible en la interfaz de usuario como si no.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | Establezca este atributo y la publicidad está deshabilitada para la característica si el shell del sistema operativo no admite Windows descriptores del instalador. Omita este atributo y la publicidad no está deshabilitada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Algunos atributos son exclusivos entre sí. Al intentar establecer estos atributos juntos en la misma característica, el paquete de instalación produce un error [**en la validación del paquete.**](package-validation.md)

-   No use msidbFeatureAttributesFavorAdvertise con msidbFeatureAttributesDisallowAdvertise.
-   No use msidbFeatureAttributesNoUnsupportedAdvertise con msidbFeatureAttributesDisallowAdvertise juntos.
-   No use msidbFeatureAttributesFollowParent con msidbFeatureAttributesFavorSource.
-   Tenga en cuenta que los valores msidbFeatureAttributesFollowParent y msidbFeatureAttributesFavorLocal son mutuamente excluyentes. Si se usa el valor msidbFeatureAttributesFollowParent, se supone que el valor msidbFeatureAttributesFavorLocal no existe.

</dd> </dl>

Tenga en cuenta que si se instala una característica secundaria, también se instala su característica primaria. Si se instala una característica primaria, su característica secundaria no se instala necesariamente a menos que se establezcan sus atributos msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent. Esta relación jerárquica de la instalación de características primarias y secundarias también se usa para las instalaciones e instalaciones de GUI que usan propiedades de línea de comandos.

## <a name="remarks"></a>Observaciones

Se agregan varias columnas temporales adicionales a esta tabla cuando se carga en memoria para los cálculos utilizados por la selección de costos e interfaz de usuario (UI).

Un componente se puede compartir entre dos o más características o aplicaciones. Si dos o más características hacen referencia al mismo componente, ese componente se selecciona para la instalación si se selecciona cualquiera de las características asociadas. Este también puede ser el motivo por el que las características secundarias no se desinstalan cuando se quita una característica primaria. Si la característica secundaria consta de componentes necesarios para otras características o aplicaciones, el instalador de Windows no quita la característica secundaria.

Para obtener más información, vea [Controlar los estados de selección de características](controlling-feature-selection-states.md).

Nivel de instalación:

-   Para cualquier instalación, hay un nivel de instalación definido, que es un valor entero de 1 a 32 767. El valor inicial viene determinado por la [**propiedad INSTALLLEVEL**](installlevel.md), que se establece en la [tabla de propiedades](property-table.md).
-   Una característica solo se instala si el valor de nivel de característica es menor o igual que el nivel de instalación actual. La interfaz de usuario se puede crear para que, cuando se inicialice la instalación, el instalador permita al usuario modificar el nivel de instalación de cualquier característica de la tabla de características. Por ejemplo, un autor puede definir valores de nivel de instalación que representan opciones de instalación específicas, como **Custom**, **Typical** o **Minimum** y, a continuación, crear un cuadro de diálogo que use [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) para permitir al usuario seleccionar uno de estos estados.
-   Según el estado que seleccione el usuario, el cuadro de diálogo establece la propiedad de nivel de instalación en el valor correspondiente. Si el autor asigna **típico** un nivel de 100 y el usuario selecciona Típico **,** solo se instalan aquellas características con un nivel de 100 o menos. Además, la **opción Personalizado** podría dar lugar a otro cuadro de diálogo que contiene un control [SelectionTree](selectiontree-control.md). A continuación, el control SelectionTree permite al usuario cambiar individualmente si cada característica está instalada o no.

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

 

 




