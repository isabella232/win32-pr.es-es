---
description: La tabla MsiShortcutProperty permite al Instalador de ventana establecer propiedades para los accesos directos que también Windows shell.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabla MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074361"
---
# <a name="msishortcutproperty-table"></a>Tabla MsiShortcutProperty

La tabla MsiShortcutProperty permite al Instalador de ventana establecer propiedades para los accesos directos que también [Windows shell.](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) A partir de Windows Vista y Windows Server 2008, Windows Shell proporciona una interfaz IPropertyStore para objetos de shell como accesos directos. Un Windows Installer 5.0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede establecer estas propiedades cuando se instala el acceso directo.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 5.0.

La tabla MsiShortcutProperty tiene las siguientes columnas.



| Columna              | Tipo                         | Clave | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificador](identifier.md) | Y   | N        |
| Acceso directo\_          | [Identificador](identifier.md) | N   | N        |
| PropertyKey         | [Formato](formatted.md)   | N   | N        |
| PropVariantValue    | [Formato](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Identificador único de esta fila de la tabla MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Acceso directo\_
</dt> <dd>

Tecla de la tabla [Acceso](shortcut-table.md) directo que identifica el acceso directo que tiene un conjunto de propiedades.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Valor de cadena que proporciona información para la [**estructura PROPERTYKEY.**](/windows/win32/api/wtypes/ns-wtypes-propertykey) La información de este campo debe hacer referencia al nombre canónico de una propiedad registrada con el Windows de propiedades. Para obtener más información sobre el Windows de propiedades, vea Información general [del sistema de propiedades](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valor de cadena que proporciona información para la [**estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

</dd> </dl>

Se pueden establecer varias propiedades en un acceso directo. Si la misma propiedad se establece varias veces en el mismo acceso directo, el valor se establece en un orden no especificado.

Windows El instalador solo puede establecer propiedades de acceso directo cuando el acceso directo está instalado o reinstalado. Una revisión que no reinstala un acceso directo que ya se ha instalado no actualiza las propiedades del acceso directo. Una revisión puede actualizar las propiedades incluyendo una tabla [de métodos abreviados](shortcut-table.md) en el paquete de revisión y reinstalando el acceso directo.

## <a name="remarks"></a>Observaciones

[Windows mensaje](windows-installer-error-messages.md) de error 1946 del instalador se devuelve como una advertencia y la instalación continúa si Windows Installer no puede establecer una propiedad de acceso directo especificada en la tabla MsiShortcutProperty.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
</dl>

 

 
