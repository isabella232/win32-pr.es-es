---
description: La tabla MsiAssembly y la tabla MsiAssemblyName especifican Windows Installer valores para los ensamblados de Common Language Runtime y los ensamblados Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabla MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669846"
---
# <a name="msiassemblyname-table"></a>Tabla MsiAssemblyName

La tabla [MsiAssembly](msiassembly-table.md) y la tabla MsiAssemblyName especifican Windows Installer valores para los ensamblados de Common Language Runtime y los ensamblados Win32. Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).

La tabla MsiAssemblyName especifica el esquema de los elementos de un nombre de caché de ensamblados seguro para un ensamblado de .NET Framework o Win32. El nombre se construye anexando todos los elementos con la misma clave de componente \_ . Consulte el ejemplo siguiente.

Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md). Para obtener más información, consulte la [API de ensamblados en paralelo](../sbscs/side-by-side-assembly-api.md).

La tabla MsiAssemblyName tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| Nombre        | [Texto](text.md)             | Y   | N        |
| Value       | [Texto](text.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave en la [tabla de componentes](component-table.md) que especifica el componente de Windows Installer que contiene este ensamblado.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre del atributo asociado con el valor especificado en la columna valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor asociado al nombre especificado en la columna nombre.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información que se crea en la tabla MsiAssemblyName debe coincidir con la información del archivo de manifiesto del ensamblado. Si la información de la tabla manifest y MsiAssemblyName no coinciden, la eliminación de la aplicación puede dejar el ensamblado en el equipo.

En el caso de los ensamblados Win32, debe haber una fila en la tabla MsiAssemblyName para cada una de las siguientes entradas en el campo Nombre: tipo, nombre, versión, idioma, publicKeyToken y processorArchitecture. El valor correspondiente para cada nombre se puede especificar en el campo de valor. Los pares nombre-valor de la tabla MsiAssemblyName deben coincidir con los atributos Type, Name, version, Language, publicKeyToken y processorArchitecture en el manifiesto del ensamblado.

En el caso de los ensamblados de Common Language Runtime privados (.NET Frameworkversions 1,0 y 1,1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: nombre, versión y referencia cultural. El valor correspondiente para cada nombre se puede especificar en el campo de valor.

En el caso de los ensamblados de Common Language Runtime globales (.NET Framework las versiones 1,0 y 1,1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: nombre, versión, referencia cultural y PublicKeyToken. El valor correspondiente para cada nombre se puede especificar en el campo de valor.

La versión .NET Framework 1,1 es la versión mínima que se puede usar para realizar una actualización en contexto de un ensamblado de Common Language Runtime global. Puede comprobar la versión de la propiedad [**MsiNetAssemblySupport**](msinetassemblysupport.md) . La tabla MsiAssemblyName también debe tener un campo FileVersion porque este tipo de actualización de ensamblado solo cambia la FileVersion. Para obtener más información, vea [Actualizar ensamblados](updating-assemblies.md).

Por ejemplo, el manifiesto del ensamblado del componente a puede tener una sección assemblyIdentity como se indica a continuación para un ensamblado Win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

En este caso, rellene la tabla MsiAssemblyName como se indica a continuación.



| Componente  | Nombre                  | Value             |
|------------|-----------------------|-------------------|
| Componentea | type                  | 32             |
| Componentea | name                  | MS-sxstest: simple |
| Componentea | version               | 1.0.0.0           |
| Componentea | language              | en                |
| Componentea | publicKeyToken        | 1111111111222222  |
| Componentea | processorArchitecture | x86               |



 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
