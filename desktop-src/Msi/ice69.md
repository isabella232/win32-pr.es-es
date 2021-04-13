---
description: ICE69 comprueba que todas las subcadenas del formulario \[ $componentkey \] dentro de una cadena con formato no son componentes de referencias cruzadas.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278460"
---
# <a name="ice69"></a>ICE69

ICE69 comprueba que todas las subcadenas del formulario \[ $componentkey \] dentro de una cadena [con formato](formatted.md) no son componentes de referencias cruzadas. Una referencia entre componentes se produce cuando la \[ \] propiedad $componentkey de una cadena con formato hace referencia a un componente distinto del componente almacenado en la \_ columna componente de las tablas.

Los problemas con la referencia entre componentes surgen de la manera en que se evalúan las cadenas [con formato](formatted.md) . Si el componente al que se hace referencia con la \[ \] propiedad $componentkey ya está instalado y no se cambia durante la instalación actual (por ejemplo, se vuelve a instalar, se mueve al origen, etc.), la expresión \[ $componentkey se \] evalúa como null, porque el estado de la acción del componente en \[ $componentkey \] es NULL. Pueden producirse problemas similares durante las operaciones de actualización y reparación.

## <a name="result"></a>Resultado

ICE69 devuelve un error si una \[ \] subcadena de $componentkey dentro de una cadena [con formato](formatted.md) hace referencia cruzada a un componente de otra característica. ICE69 devuelve una advertencia si una \[ \] subcadena de $componentkey dentro de una cadena con formato hace referencia cruzada a un componente de la misma característica. (La tabla [FeatureComponents](featurecomponents-table.md) se usa para determinar esta asignación. Se debe asignar a la misma característica para la advertencia. La referencia a los componentes de las características primarias o a los componentes que hacen referencia a las características secundarias se considera un error).

ICE69 notifica un error si la \[ \# \] subcadena FileKey de una cadena [con formato](formatted.md) hace referencia a un archivo que no se especifica en la tabla de [archivos](file-table.md) como perteneciente al mismo componente.

## <a name="example"></a>Ejemplo

ICE69 notifica lo siguiente para los ejemplos mostrados.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Para corregir este error, no haga referencia cruzada a los componentes. Cambie el \[ $componentkey \] para que coincida con el componente del acceso directo.

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Argumento     |
|-----------|-------------|--------------|
| Prueba      | QuickTest   | -v \[ $Test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

Las tablas de [extensión](extension-table.md) y de [verbo](verb-table.md) son casos especiales en los que la tabla de verbos hace referencia a una extensión que pertenece a un componente. Sin embargo, una extensión puede pertenecer a varios componentes porque la clave principal de la tabla de extensión se compone de las columnas de extensión y componente \_ . Lógicamente, puede tener la siguiente situación.

[Tabla de verbos](verb-table.md) (parcial)



| Extensión | Verbo\_ | Argumento                |
|-----------|--------|-------------------------|
| TST       | abrir   | -v \[ $COMP 1 \] \[ $COMP 2\] |



 

[Tabla de extensión](extension-table.md) (parcial)



| Extensión | Componente\_ |
|-----------|-------------|
| TST       | COMP1       |
| TST       | COMP2       |



 

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Prueba        |
| Característica2  | Test2       |



 

En este caso, debe asegurarse de que al menos una de las \[ propiedades de $componentkey se \] evalúe como un valor distinto de NULL. Sin embargo, \[ cada \] propiedad $componentkey de la columna argument de la tabla Verb ( \[ $comp 1 \] y \[ $COMP 2 \] en el ejemplo anterior) debe hacer referencia a un componente posible incluido en la extensión asociada al verbo. Una referencia como \[ $COMP 3 \] produciría una advertencia de ICE69.

La [tabla AppID](appid-table.md) tiene una situación similar a la de la tabla Verb. Usa la [tabla de clases](class-table.md) para su referencia de componente. En este caso, la tabla AppId se valida de la misma manera que la validación Verb-Extension (ahora AppId-Class).

La columna de argumento de la tabla de clase se valida como el [acceso directo](shortcut-table.md), el [registro](registry-table.md)y las tablas similares.

## <a name="table-used-during-execution-only-if-found"></a>Tabla utilizada durante la ejecución (solo si se encuentra)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registro](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Acceso directo](shortcut-table.md)

[Verbo](verb-table.md)

[Extensión](extension-table.md)

[Clase](class-table.md)

[AppId](appid-table.md)

[Entorno](environment-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



