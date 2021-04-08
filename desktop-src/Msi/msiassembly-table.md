---
description: La tabla MsiAssembly especifica la configuración de Windows Installer para los ensamblados de Microsoft .NET Framework y los ensamblados Win32. Para obtener más información, vea Instalar ensamblados en la caché global de ensamblados e instalar ensamblados Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabla MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003049"
---
# <a name="msiassembly-table"></a>Tabla MsiAssembly

La tabla MsiAssembly especifica la configuración de Windows Installer para los ensamblados de Microsoft .NET Framework y los ensamblados Win32. Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).

En Windows XP, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md). Para obtener más información, consulte la [API de ensamblados en paralelo](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Esta característica no se admite.

La tabla MsiAssembly tiene las columnas siguientes.



| Columna            | Tipo                         | Clave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificador](identifier.md) | Y   | N        |
| Característica\_         | [Identificador](identifier.md) | N   | N        |
| Manifiesto de archivo \_    | [Identificador](identifier.md) | N   | Y        |
| Aplicación de archivo \_ | [Identificador](identifier.md) | N   | Y        |
| Atributos        | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave en la [tabla de componentes](component-table.md) que especifica el Windows Installer componente que contiene este ensamblado.

El valor de este campo no debe establecerse en NULL. El campo de ruta de la [tabla de componentes](component-table.md) no debe ser null.

En el caso de los ensamblados de Win32, la ruta de acceso de componente no puede ser el archivo de manifiesto especificado en el manifiesto de archivo \_ . El manifiesto puede ser la ruta de la ruta de una .NET Framework o un ensamblado de directiva.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Clave en la [tabla de características](feature-table.md).

Cuando la instalación de una característica debe instalar el ensamblado, Windows Installer instala la característica señalada por este campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifiesto de archivo \_
</dt> <dd>

Una clave externa en la [tabla de archivos](file-table.md) que especifica el archivo que contiene el manifiesto de un ensamblado de .NET Framework o de Win32.

En el caso de un ensamblado Win32, no especifique este archivo como el archivo de ruta de acceso de la clave de componente en el campo de ruta de clave de la [tabla de componentes](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicación de archivo \_
</dt> <dd>

Para instalar el ensamblado en una ubicación privada, escriba el archivo de ruta de acceso de la clave para el componente de ensamblado en este campo.

Este es el valor que aparece en el campo de ruta de la ruta de la [tabla de componentes](component-table.md). Después, el instalador puede instalar el ensamblado en la estructura de directorios del componente que se especifica en la [tabla del directorio](directory-table.md). Este campo debe ser null si el ensamblado se va a instalar en la caché global de ensamblados.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Escriba un valor de 1 (uno) para un ensamblado Win32. Escriba un valor de 0 (cero) para un ensamblado de .NET Framework.

Si la columna Attributes es NULL, el instalador trata el ensamblado como un ensamblado de .NET Framework.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si hay al menos una entrada en la tabla MsiAssembly, la [tabla InstallExecuteSequence](installexecutesequence-table.md) debe contener la [acción MsiPublishAssemblies](msipublishassemblies-action.md)y la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Dado que los ensamblados no se pueden revertir una vez confirmados, Windows Installer usa un proceso de instalación de dos pasos. Las interfaces a los ensamblados se crean durante las operaciones de instalación generadas por la [acción MsiPublishAssemblies](msipublishassemblies-action.md).

Los ensamblados no se confirman hasta que la ejecución de la [acción InstallFinalize](installfinalize-action.md)es correcta. Esto significa que si crea una acción personalizada o un recurso que se basa en el ensamblado, se debe secuenciar después de la [acción InstallFinalize](installfinalize-action.md). Por ejemplo, si necesita iniciar un servicio que depende de un ensamblado en la caché de ensamblados global (GAC), debe programar el inicio de ese servicio después de la [acción InstallFinalize](installfinalize-action.md). Esto significa que no puede usar la [tabla ServiceControl](servicecontrol-table.md) para iniciar el servicio, sino que debe usar una acción personalizada que se secuenciará después de InstallFinalize.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
