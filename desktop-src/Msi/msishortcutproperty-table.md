---
description: La tabla MsiShortcutProperty habilita el instalador de Windows para establecer las propiedades de los accesos directos que también son objetos de Shell de Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabla MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546422"
---
# <a name="msishortcutproperty-table"></a>Tabla MsiShortcutProperty

La tabla MsiShortcutProperty habilita el instalador de Windows para establecer las propiedades de los accesos directos que también son objetos de [Shell de Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . A partir de Windows Vista y Windows Server 2008, el shell de Windows proporciona una interfaz IPropertyStore para objetos de shell como métodos abreviados. Un paquete Windows Installer 5,0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede establecer estas propiedades cuando se instala el acceso directo.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 5,0.

La tabla MsiShortcutProperty tiene las columnas siguientes.



| Columna              | Tipo                         | Clave | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificador](identifier.md) | Y   | N        |
| Acceso directo\_          | [Identificador](identifier.md) | N   | N        |
| PropertyKey         | [Formatea](formatted.md)   | N   | N        |
| PropVariantValue    | [Formatea](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Identificador único para esta fila de la tabla MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Contextual\_
</dt> <dd>

Clave en la tabla de [accesos directos](shortcut-table.md) que identifica el acceso directo que tiene establecida una propiedad.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Valor de cadena que proporciona información para la estructura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . La información de este campo debe hacer referencia al nombre canónico de una propiedad registrada con el sistema de propiedades de Windows. Para obtener más información sobre el sistema de propiedades de Windows, vea la [información general](/previous-versions//bb776909(v=vs.85))sobre el sistema de propiedades.

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valor de cadena que proporciona información para la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Se pueden establecer varias propiedades en un acceso directo. Si se establece la misma propiedad varias veces en el mismo método abreviado, el valor se establece en un orden no especificado.

Windows Installer puede establecer las propiedades de acceso directo solo cuando se instala o se vuelve a instalar el acceso directo. Una revisión que no Reinstala un acceso directo que ya se ha instalado no actualiza las propiedades del acceso directo. Una revisión puede actualizar las propiedades incluyendo una tabla de [acceso directo](shortcut-table.md) en el paquete de revisión y reinstalando el acceso directo.

## <a name="remarks"></a>Observaciones

[Windows Installer mensaje de Error](windows-installer-error-messages.md) 1946 se devuelve como una advertencia y la instalación continúa, si Windows Installer no puede establecer una propiedad de acceso directo especificada en la tabla MsiShortcutProperty.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
</dl>

 

 
