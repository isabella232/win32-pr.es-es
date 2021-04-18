---
description: ': Valida la tabla de actualización de una base de datos Windows Installer.'
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ':'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652862"
---
# <a name="ice61"></a>:

: Comprueba la tabla de actualización para asegurarse de que se cumplen las condiciones siguientes:

-   Todas las propiedades ActionProperty no se han creado previamente en la tabla de propiedades.
-   Todas las propiedades de ActionProperty son propiedades públicas.
-   Todas las propiedades de ActionProperty se incluyen en la propiedad [**SecureCustomProperties**](securecustomproperties.md) .
-   Todas las propiedades de ActionProperty son únicas para cada registro de la tabla de actualización.
-   Todos los valores de VersionMax no son menores que los valores de VersionMin correspondientes.
-   Los valores VersionMin y VersionMax son versiones de producto válidas. Vea la propiedad [**ProductVersion**](productversion.md) para el formato de versión de producto válido.
-   No se realiza ningún intento de quitar una versión más reciente o igual del producto actual.

Si no se corrige una advertencia o un error informados por:, generalmente se producen problemas en la actualización de la aplicación. En función del error exacto, podría ser cualquier cosa, desde la salida de los archivos de la versión anterior, la eliminación de los archivos de la versión anterior aunque sean necesarios para la nueva aplicación o un error completo de la actualización.

## <a name="result"></a>Resultado

: Expone una advertencia o un error si no se cumple alguna de las condiciones anteriores.

## <a name="example"></a>Ejemplo

: Notifica los siguientes errores y advertencias para los ejemplos que se muestran.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

En este caso, la primera fila intentaría quitar un producto de la misma versión. (VersionMax columna es igual a la versión del producto en la tabla de propiedades).

Para corregir este error, use una versión de la columna VersionMax anterior a la versión actual especificada en la tabla de propiedades. Quite el bit **msidbUpgradeAttributesVersionMaxInclusive** de la columna Attributes si el valor de VersionMax es igual a la versión actual. Si la intención es solo detectar el producto y no quitarlo, al agregar el bit **msidbUpgradeAttributesOnlyDetect** a la columna atributos también se corregirá este error.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A menos que la propiedad se muestre en la propiedad [**SecureCustomProperties**](securecustomproperties.md) , la propiedad no se pasa al lado del servidor de la instalación cuando se encuentra la propiedad.

Para corregir este error, agregue la propiedad a [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Las propiedades de actualización deben ser propiedades públicas del resultado que se va a pasar al lado del servidor de la instalación.

Para corregir este error, utilice todas las letras mayúsculas en el nombre de la propiedad.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Una propiedad solo se puede usar en una fila de la tabla de actualización.

Para corregir este error, use una propiedad diferente para la segunda fila.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

La versión mínima debe ser inferior a la versión máxima.

Para corregir este error, compruebe los números de versión en busca de errores tipográficos. Si son correctos y desea utilizar el intervalo entre las dos versiones, alterne para que VersionMin sea menor que VersionMax.

[Tabla de propiedades](property-table.md)



| Propiedad                                                 | Value                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Actualizar tabla](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos | Remove                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 3082     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



