---
description: ICE69 comprueba que todas las subcadenas del formulario $componentkey dentro de una cadena con formato no hacen referencia \[ \] cruzada a los componentes.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074554"
---
# <a name="ice69"></a>ICE69

ICE69 comprueba que todas las subcadenas del formulario $componentkey dentro de una cadena con formato no hacen referencia \[ \] cruzada a los componentes. [](formatted.md) Se produce una referencia entre componentes cuando la propiedad $componentkey de una cadena con formato hace referencia a un componente distinto del componente almacenado en la columna Componente de \[ \] las \_ tablas.

Los problemas con la referencia entre componentes surgen de la forma en que se [evalúan](formatted.md) las cadenas con formato. Si el componente al que se hace referencia con la propiedad $componentkey ya está instalado y no se cambia durante la instalación actual (por ejemplo, se vuelve a instalar, se mueve \[ al origen, etc.), la expresión $componentkey se evalúa como null, porque el estado de acción del componente en \] $componentkey es \[ \] \[ \] null. Pueden producirse problemas similares durante las operaciones de actualización y reparación.

## <a name="result"></a>Resultado

ICE69 devuelve un error si un $componentkey una subcadena dentro de una cadena con formato hace referencia \[ cruzada a un componente de otra \] característica. [](formatted.md) ICE69 devuelve una advertencia si una subcadena $componentkey dentro de una cadena con formato hace referencia cruzada a un \[ componente de la misma \] característica. (La [tabla FeatureComponents](featurecomponents-table.md) se usa para determinar esta asignación. Debe asignarse a la misma característica para la advertencia. La referencia a componentes en características primarias o a componentes de referencia en características secundarias se considera un error).

ICE69 notifica un error si la subcadena FileKey dentro de una cadena con formato hace referencia a un archivo que no se especifica en la tabla File como perteneciente \[ \# al mismo \] componente. [](formatted.md) [](file-table.md)

## <a name="example"></a>Ejemplo

ICE69 informa de lo siguiente para los ejemplos mostrados.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Para corregir este error, no haga referencia cruzada a los componentes. Cambie el \[ $componentkey \] para que coincida con el componente del acceso directo.

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Argumento     |
|-----------|-------------|--------------|
| Prueba      | Quicktest   | -v \[ $Test\] |
| Acceso directo2 | Quicktest   | \[$Test 2\]   |



 

Las [tablas Verbo](verb-table.md) y [Extensión](extension-table.md) son casos especiales en los que la tabla Verbo hace referencia a una extensión que pertenece a un componente. Sin embargo, una extensión puede pertenecer a varios componentes, ya que la clave principal de la tabla de extensiones se forma de las columnas Extension y \_ Component. Lógicamente, puede tener la siguiente situación.

[Tabla de verbos](verb-table.md) (parcial)



| Extensión | Verbo\_ | Argumento                |
|-----------|--------|-------------------------|
| Tst       | abierto   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Tabla de extensiones](extension-table.md) (parcial)



| Extensión | Componente\_ |
|-----------|-------------|
| Tst       | comp1       |
| Tst       | comp2       |



 

[Tabla FeatureComponents](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Característica 1  | Quicktest   |
| Característica 1  | Prueba        |
| Característica 2  | Test2       |



 

En este caso, debe asegurarse de que al menos una de las propiedades $componentkey se evalúa \[ como un valor distinto de \] NULL. Sin embargo, cada propiedad $componentkey de la columna Argument de la tabla \[ \] Verb \[ ($comp 1 y \] \[ $comp 2 en el \] ejemplo anterior) debe hacer referencia a un posible componente incluido con la extensión asociada al verbo. Una referencia como \[ $comp 3 \] produciría una advertencia de ICE69.

La [tabla AppId](appid-table.md) tiene una situación similar a la tabla Verb. Usa la tabla [Class para su](class-table.md) referencia de componente. En este caso, la tabla AppId se valida de la misma manera que la Verb-Extension validación (ahora AppId-Class).

La columna Argument de la tabla Class se valida como [el método abreviado](shortcut-table.md), el [Registro](registry-table.md)y tablas similares.

## <a name="table-used-during-execution-only-if-found"></a>Tabla usada durante la ejecución (solo si se encuentra)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registro](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Acceso directo](shortcut-table.md)

[Verb](verb-table.md)

[Extensión](extension-table.md)

[Clase](class-table.md)

[Appid](appid-table.md)

[Entorno](environment-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



