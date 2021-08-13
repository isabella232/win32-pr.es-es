---
description: La tabla MsiAssembly especifica Windows configuración del instalador para los ensamblados .NET Framework Microsoft y los ensamblados Win32. Para obtener más información, vea Instalación de ensamblados en la caché global de ensamblados e Instalación de ensamblados Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabla MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda246bd6baba75d0f7e8d53f515a25abb0c163c2d3ef0b1b9705c123b8e69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381385"
---
# <a name="msiassembly-table"></a>Tabla MsiAssembly

La tabla MsiAssembly especifica Windows configuración del instalador para los ensamblados .NET Framework Microsoft y los ensamblados Win32. Para obtener más información, vea [Instalación de ensamblados en la caché global](installation-of-assemblies-to-the-global-assembly-cache.md) de ensamblados e Instalación de [ensamblados Win32.](installation-of-win32-assemblies.md)

En Windows XP, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo.](side-by-side-assemblies.md) Para obtener más información, consulte la API de [ensamblado en paralelo](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Esta característica no se admite.

La tabla MsiAssembly tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificador](identifier.md) | Y   | N        |
| Característica\_         | [Identificador](identifier.md) | N   | N        |
| Manifiesto de \_ archivo    | [Identificador](identifier.md) | N   | Y        |
| Aplicación de \_ archivo | [Identificador](identifier.md) | N   | Y        |
| Atributos        | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave de la [tabla de componentes](component-table.md) que especifica el Windows instalador que contiene este ensamblado.

El valor de este campo no debe establecerse en NULL. El campo KeyPath del componente de [la tabla de componentes](component-table.md) no debe ser NULL.

En el caso de los ensamblados Win32, el componente KeyPath no puede ser el archivo de manifiesto especificado en Manifiesto de \_ archivo. El manifiesto puede ser la ruta de acceso de clave para un .NET Framework o ensamblado de directiva.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave en la [tabla de características](feature-table.md).

Cuando el ensamblado debe instalarse mediante una instalación de características, Windows Installer instala la característica a la que apunta este campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifiesto de \_ archivo
</dt> <dd>

Clave externa en la [tabla de](file-table.md) archivos que especifica el archivo que contiene el manifiesto para un ensamblado .NET Framework o ensamblado Win32.

Para un ensamblado Win32, no especifique este archivo como archivo de ruta de acceso de clave de componente en el campo KeyPath de la [tabla de componentes](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicación de \_ archivo
</dt> <dd>

Para instalar el ensamblado en una ubicación privada, escriba el archivo de ruta de acceso de clave para el componente de ensamblado en este campo.

Este es el valor que aparece en el campo KeyPath de la [tabla de componentes](component-table.md). A continuación, el instalador puede instalar el ensamblado en la estructura de directorios del componente especificado en la tabla [de directorios](directory-table.md). Este campo debe ser NULL si el ensamblado se va a instalar en la caché global de ensamblados.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Escriba un valor de 1 (uno) para un ensamblado win32. Escriba un valor de 0 (cero) para un .NET Framework ensamblado.

Si la columna Atributos es NULL, el instalador trata el ensamblado como un .NET Framework ensamblado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si hay al menos una entrada en la tabla MsiAssembly, la tabla [InstallExecuteSequence](installexecutesequence-table.md) debe contener las acciones [MsiPublishAssemblies](msipublishassemblies-action.md)y [MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Dado que los ensamblados no se pueden revertir después de que se confirman, Windows Installer usa un proceso de instalación en dos pasos. Las interfaces para los ensamblados se crean durante las operaciones de instalación generadas por [la acción MsiPublishAssemblies](msipublishassemblies-action.md).

Los ensamblados no se confirman hasta la ejecución correcta de [la acción InstallFinalize](installfinalize-action.md). Esto significa que si se cree una acción personalizada o un recurso que se base en el ensamblado, se debe secuenciar después de [la acción InstallFinalize](installfinalize-action.md). Por ejemplo, si necesita iniciar un servicio que depende de un ensamblado en la caché global de ensamblados (GAC), debe programar el inicio de ese servicio después de la acción [InstallFinalize](installfinalize-action.md). Esto significa que no puede usar la [tabla ServiceControl](servicecontrol-table.md) para iniciar el servicio, sino que debe usar una acción personalizada que se secuencia después de InstallFinalize.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
