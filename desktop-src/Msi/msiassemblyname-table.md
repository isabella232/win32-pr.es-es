---
description: La tabla MsiAssembly y la tabla MsiAssemblyName especifican Windows del instalador para ensamblados de Common Language Runtime y ensamblados Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabla MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071884"
---
# <a name="msiassemblyname-table"></a>Tabla MsiAssemblyName

La [tabla MsiAssembly y](msiassembly-table.md) la tabla MsiAssemblyName especifican Windows del instalador para ensamblados de Common Language Runtime y ensamblados Win32. Para obtener información, [vea Instalación de ensamblados en la caché global](installation-of-assemblies-to-the-global-assembly-cache.md) de ensamblados e Instalación de [ensamblados Win32.](installation-of-win32-assemblies.md)

La tabla MsiAssemblyName especifica el esquema para los elementos de un nombre de caché de ensamblados segura para un ensamblado .NET Framework o Win32. El nombre se construye anexando todos los elementos con la misma clave de \_ componente. Consulte el ejemplo siguiente.

Windows El instalador puede instalar ensamblados win32 como [ensamblados en paralelo.](side-by-side-assemblies.md) Para obtener más información, consulte la API de [ensamblado en paralelo](../sbscs/side-by-side-assembly-api.md).

La tabla MsiAssemblyName tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| Nombre        | [Texto](text.md)             | Y   | N        |
| Value       | [Texto](text.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave en la [tabla de componentes](component-table.md) que especifica el Windows installer que contiene este ensamblado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del atributo asociado al valor especificado en la columna Valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor asociado al nombre especificado en la columna Nombre.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información que se ha escrito en la tabla MsiAssemblyName debe coincidir con la información del archivo de manifiesto del ensamblado. Si la información del manifiesto y la tabla MsiAssemblyName no coinciden, la eliminación de la aplicación puede dejar el ensamblado en el equipo.

Para los ensamblados Win32, debe haber una fila en la tabla MsiAssemblyName para cada una de las siguientes entradas en el campo Nombre: type, name, version, language, publicKeyToken y processorArchitecture. El valor correspondiente para cada nombre se puede especificar en el campo Valor. Los pares nombre-valor de msiAssemblyName Table deben coincidir con los atributos type, name, version, language, publicKeyToken y processorArchitecture en el manifiesto del ensamblado.

Para los ensamblados privados de Common Language Runtime (.NET Frameworkversions 1.0 y 1.1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: Nombre, Versión y Referencia cultural. El valor correspondiente para cada nombre se puede especificar en el campo Valor.

Para los ensamblados globales de Common Language Runtime (.NET Framework versiones 1.0 y 1.1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: Nombre, Versión, Referencia cultural y PublicKeyToken. El valor correspondiente para cada nombre se puede especificar en el campo Valor.

La .NET Framework versión 1.1 es la versión mínima que se puede usar para realizar una actualización local de un ensamblado global de Common Language Runtime. Puede comprobar la [**propiedad MsiNetAssemblySupport**](msinetassemblysupport.md) para la versión. La tabla MsiAssemblyName también debe tener un campo FileVersion porque este tipo de actualización de ensamblado solo cambia FileVersion. Para obtener más información, vea [Actualizar ensamblados](updating-assemblies.md).

Por ejemplo, el manifiesto de ensamblado para ComponentA podría tener una sección assemblyIdentity como se muestra a continuación para un ensamblado win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

En este caso, rellene la tabla MsiAssemblyName como se muestra a continuación.



| Componente  | Nombre                  | Value             |
|------------|-----------------------|-------------------|
| ComponenteA | type                  | win32             |
| ComponenteA | name                  | ms-sxstest-simple |
| ComponenteA | version               | 1.0.0.0           |
| ComponenteA | language              | en                |
| ComponenteA | Publickeytoken        | 1111111111222222  |
| ComponenteA | processorArchitecture | x86               |



 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
