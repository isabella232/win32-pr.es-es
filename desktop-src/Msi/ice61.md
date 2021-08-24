---
description: ICE61 valida la tabla Upgrade de una base de Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c772a076decaa385d01047daa45871aeeaf7898d4cf3347606c4066d1f7f2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580985"
---
# <a name="ice61"></a>ICE61

ICE61 comprueba la tabla de actualización para asegurarse de que se cumplen las condiciones siguientes:

-   Todas las propiedades ActionProperty no están preautoradas en la tabla Property.
-   Todas las propiedades ActionProperty son Propiedades públicas.
-   Todas las propiedades ActionProperty se incluyen en [**la propiedad SecureCustomProperties.**](securecustomproperties.md)
-   Todas las propiedades ActionProperty son únicas para cada registro de la tabla Upgrade.
-   Todos los valores de VersionMax no son menores que los valores versionMin correspondientes.
-   Los valores VersionMin y VersionMax son versiones de producto válidas. Consulte la [**propiedad ProductVersion**](productversion.md) para obtener el formato de versión de producto válido.
-   No se intenta quitar una versión más reciente o igual del producto actual.

Por lo general, si no se corrige una advertencia o un error notificado por ICE61, se producirán problemas en la actualización de la aplicación. Dependiendo del error exacto, podría ser cualquier cosa: dejar los archivos de la versión anterior, eliminar los archivos de la versión anterior aunque la nueva aplicación los necesite o completar un error en la actualización.

## <a name="result"></a>Resultado

ICE61 envía una advertencia o un error si alguna de las condiciones anteriores no es verdadera.

## <a name="example"></a>Ejemplo

ICE61 notifica los siguientes errores y advertencias para los ejemplos mostrados.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

En este caso, la primera fila intentaría quitar un producto de la misma versión. (La columna VersionMax es igual a la versión del producto en la tabla Property).

Para corregir este error, use una versión de la columna VersionMax inferior a la versión actual especificada en la tabla Property. Quite el **bit msidbUpgradeAttributesVersionMaxInclusive** de la columna Attributes si VersionMax es igual a la versión actual. Si la intención es solo detectar el producto y no quitarlo, agregar el bit **msidbUpgradeAttributesOnlyDetect** a la columna Atributos también corregirá este error.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

A menos que la propiedad aparezca en [**la propiedad SecureCustomProperties,**](securecustomproperties.md) la propiedad no se pasa al lado servidor de la instalación cuando se encuentra la propiedad.

Para corregir este error, agregue la propiedad a [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Las propiedades de actualización deben ser propiedades públicas para que el resultado se pase al lado servidor de la instalación.

Para corregir este error, use todas las letras mayúsculas en el nombre de propiedad.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Una propiedad solo se puede usar en una fila de la tabla Upgrade.

Para corregir este error, use una propiedad diferente para la segunda fila.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

La versión mínima debe ser menor que la versión máxima.

Para corregir este error, compruebe los números de versión en busca de errores tipográficos. Si son correctos y desea usar el intervalo entre las dos versiones, cambie para que VersionMin sea menor que VersionMax.

[Tabla de propiedades](property-table.md)



| Propiedad                                                 | Value                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Actualizar tabla](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Lenguaje | Atributos | Quitar                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 3082     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



