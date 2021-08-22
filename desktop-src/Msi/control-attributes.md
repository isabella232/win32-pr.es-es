---
description: Para obtener información sobre los atributos de control, vea el vínculo al control concreto que necesita crear en Controles, así como los vínculos a atributos de control concretos en las listas siguientes.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Atributos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9d7412ce3893b785dccf067287c191f033bdf5a100628577260ff10f74ce1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500725"
---
# <a name="control-attributes"></a>Atributos de control

Para obtener información sobre los atributos de control, vea el vínculo al control concreto que debe crear en [Controles,](controls.md) así como los vínculos a atributos de control concretos en las listas siguientes.

Los métodos siguientes se usan para especificar los atributos de un control :

-   Use la [tabla ControlCondition para](controlcondition-table.md) deshabilitar, habilitar, ocultar o mostrar un control según el valor de una propiedad o instrucción condicional. También puede usar esta tabla para invalidar el control predeterminado especificado en la tabla [Dialog](dialog-table.md).
-   Suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md). Escriba el identificador del atributo en la columna Atributo y el identificador de ControlEvent en la columna Evento de esta tabla.
-   Establezca las marcas de bits del atributo de control para el control en la columna Atributo de la [tabla Control](control-table.md). Esto establece los atributos tras la creación del control.

Algunos atributos no se pueden establecer para cada control ni especificarse mediante todos los métodos anteriores. Consulte los temas de control y atributo concretos para obtener más información.

Los valores iniciales de algunos atributos de control se pueden establecer con bits en la [tabla Control](control-table.md).



| Atributo                                          | Decimal | Hexadecimal | Constante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [Bidi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Habilitado](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indirecto](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Integer (Control)](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [Alineado a la derecha](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Estos atributos de los controles Text se establecen con bits.



| Atributo                                            | Decimal | Hexadecimal | Constante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [FormatSize](formatsize-control-attribute.md)       | 524 288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131 072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [NoWrap](nowrap-control-attribute.md)               | 262 144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Contraseña](password-control-attribute.md)           | 2 097 152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Transparente](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1 048 576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Este atributo del control ProgressBar se establece con un bit.



| Atributo                                      | Decimal | Hexadecimal | Constante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Estos atributos de los controles Volume y Directory SelectCombo se establecen con bits.



| Atributo                                                | Decimal | Hexadecimal | Constante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524 288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131 072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2 097 152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1 048 576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262 144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Estos atributos de los controles ListBox y ComboBox se establecen con bits.



| Atributo                                            | Decimal | Hexadecimal | Constante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [ComboList Control](combolist-control-attribute.md) | 131 072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Control ordenado](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Este atributo del control Edit se establece con un bit.



| Atributo                                    | Decimal | Hexadecimal | Constante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Multilínea](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Estos atributos de los controles PictureButton se establecen con bits.



| Atributo                                          | Decimal | Hexadecimal | Constante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262 144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Icono](icon-control-attribute.md)                 | 524 288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2 097 152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4 194 304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [PushLike Control](pushlike-control-attribute.md) | 131 072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Este atributo del control RadioButton se establece con un bit.



| Atributo                                    | Decimal  | Hexadecimal | Constante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Este atributo del control PushButton se establece con un bit.



| Atributo                                        | Decimal | Hexadecimal | Constante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesEentaciónShield** |



 

Este atributo del control VolumeCostList se establece con un bit.



| Atributo                                                                | Decimal | Hexadecimal | Constante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4 194 304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Los siguientes atributos de control no se establecen con bits. Estos atributos se crearon en las tablas de la interfaz de usuario o se establecen mediante [Eventos de control](control-events.md).

[NameName](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Control de progreso](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Vea [Agregar controles y texto.](adding-controls-and-text.md)

 

 



