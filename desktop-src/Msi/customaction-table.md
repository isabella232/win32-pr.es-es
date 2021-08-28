---
description: La tabla CustomAction proporciona el medio de integrar el código y los datos personalizados en la instalación. El origen del código que se ejecuta puede ser una secuencia incluida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: CustomAction (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725ac6ad72b1f84da2c43c94a91cd4a466bd02a5af19261b4b07dfd1c496ae76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947869"
---
# <a name="customaction-table"></a>CustomAction (tabla)

La tabla CustomAction proporciona el medio de integrar el código y los datos personalizados en la instalación. El origen del código que se ejecuta puede ser una secuencia incluida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.

La tabla CustomAction tiene las columnas siguientes.



| Columna       | Tipo                               | Clave | Nullable |
|--------------|------------------------------------|-----|----------|
| Acción       | [Identificador](identifier.md)       | Y   | N        |
| Tipo         | [Entero](integer.md)             | N   | N        |
| Source       | [CustomSource](customsource.md)   | N   | Y        |
| Destino       | [Formato](formatted.md)         | N   | Y        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de la acción. Normalmente, la acción aparece en una tabla de secuencia a menos que la llame otra acción personalizada. Si el nombre coincide con cualquier acción integrada, nunca se llama a la acción personalizada.

Clave de tabla principal.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Campo de bits de marca que especifica el tipo básico de acción personalizada y opciones. Vea [Lista de resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md) para obtener una lista de los tipos básicos. Vea [Custom Action Return Processing Options](custom-action-return-processing-options.md)( Opciones de procesamiento de devolución de acciones personalizadas), Custom Action Execution [Scheduling Options](custom-action-execution-scheduling-options.md)(Opciones de programación de ejecución de acciones personalizadas), Custom Action Hidden Target [Option](custom-action-hidden-target-option.md)(Opción de destino oculto de acción personalizada) y Custom Action In-Script Execution Options (Opciones de ejecución de [acciones personalizadas).](custom-action-in-script-execution-options.md)

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuente
</dt> <dd>

Un nombre de propiedad o una clave externa en otra tabla. Para obtener una explicación de los posibles orígenes de acciones personalizadas, vea Orígenes de [acciones personalizadas](custom-action-sources.md) y [La lista de resumen de todos los tipos de acción personalizados.](summary-list-of-all-custom-action-types.md) Por ejemplo, la columna Origen puede contener una clave externa en la primera columna de una de las tablas siguientes que contiene el origen del código de acción personalizado.

[Tabla de directorios](directory-table.md) para llamar a archivos ejecutables existentes.

[Tabla de archivos](file-table.md) para llamar a archivos ejecutables y archivos DLL que se acaba de instalar.

[Tabla binaria para](binary-table.md) llamar a archivos ejecutables, archivos DLL y datos almacenados en la base de datos.

[Tabla de propiedades](property-table.md) para llamar a ejecutables cuyas rutas de acceso están retenidos por una propiedad.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Objetivo
</dt> <dd>

Parámetro de ejecución que depende del tipo básico de acción personalizada. Consulte la [Lista de resumen de todos los](summary-list-of-all-custom-action-types.md) tipos de acción personalizados para obtener una descripción de lo que debe especificarse en este campo para cada tipo de acción personalizada. Por ejemplo, este campo puede contener lo siguiente en función de la acción personalizada.



| Destino                                    | Acción personalizada                         |
|-------------------------------------------|---------------------------------------|
| Punto de entrada (obligatorio)                    | Llamar a un archivo DLL.                        |
| Nombre ejecutable con argumentos (obligatorio) | Llamar a un ejecutable existente.       |
| Argumentos de la línea de comandos (opcional)         | Llamar a un ejecutable que acaba de instalarse. |
| Nombre de archivo de destino (obligatorio)               | Crear un archivo a partir de datos personalizados.     |
| Null                                      | Ejecutar código de script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Escriba el **valor msidbCustomActionTypePatchUninstall** en este campo para especificar una acción personalizada con la opción de desinstalación de [revisión de acción personalizada](custom-action-patch-uninstall-option.md).

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta opción está disponible a partir de Windows Installer 4.5.

</dd> </dl>

Para obtener más información, vea todos los temas de [Acciones personalizadas.](custom-actions.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



