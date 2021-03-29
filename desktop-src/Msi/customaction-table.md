---
description: La tabla CustomAction proporciona los medios para integrar el código personalizado y los datos en la instalación de. El origen del código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabla CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810393"
---
# <a name="customaction-table"></a>Tabla CustomAction

La tabla CustomAction proporciona los medios para integrar el código personalizado y los datos en la instalación de. El origen del código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.

La tabla CustomAction tiene las columnas siguientes.



| Columna       | Tipo                               | Clave | Nullable |
|--------------|------------------------------------|-----|----------|
| Acción       | [Identificador](identifier.md)       | Y   | N        |
| Tipo         | [Entero](integer.md)             | N   | N        |
| Source       | [CustomSource](customsource.md)   | N   | Y        |
| Destino       | [Formatea](formatted.md)         | N   | Y        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Nombre de la acción. La acción normalmente aparece en una tabla de secuencia a menos que otra acción personalizada la llame. Si el nombre coincide con cualquier acción integrada, nunca se llama a la acción personalizada.

Clave de la tabla principal.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Campo de bits de marca que especifica el tipo básico de acción y opciones personalizadas. Vea [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md) para obtener una lista de los tipos básicos. Vea [Opciones de procesamiento de devolución](custom-action-return-processing-options.md)de acción personalizada, [Opciones de programación](custom-action-execution-scheduling-options.md)de la ejecución de acciones personalizadas, [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md)y opciones de ejecución de la [acción personalizada In-Script](custom-action-in-script-execution-options.md).

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes
</dt> <dd>

Un nombre de propiedad o una clave externa en otra tabla. Para obtener una explicación de los posibles orígenes de acciones personalizadas, vea [Custom Action sources](custom-action-sources.md) y la [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md). Por ejemplo, la columna de origen puede contener una clave externa en la primera columna de una de las tablas siguientes que contengan el origen del código de acción personalizada.

[Tabla del directorio](directory-table.md) para llamar a ejecutables existentes.

[Tabla de archivos](file-table.md) para llamar a archivos ejecutables y dll que se acaban de instalar.

[Tabla binaria](binary-table.md) para llamar a ejecutables, archivos dll y datos almacenados en la base de datos.

[Tabla de propiedades](property-table.md) para llamar a ejecutables cuyas rutas de acceso están retenidas por una propiedad.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir
</dt> <dd>

Parámetro de ejecución que depende del tipo básico de acción personalizada. Consulte la [lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md) para obtener una descripción de lo que se debe escribir en este campo para cada tipo de acción personalizada. Por ejemplo, este campo puede contener lo siguiente en función de la acción personalizada.



| Destino                                    | Acción personalizada                         |
|-------------------------------------------|---------------------------------------|
| Punto de entrada (obligatorio)                    | Llamar a un archivo DLL.                        |
| Nombre del archivo ejecutable con argumentos (obligatorio) | Llamar a un ejecutable existente.       |
| Argumentos de la línea de comandos (opcional)         | Llamar a un archivo ejecutable recién instalado. |
| Nombre de archivo de destino (obligatorio)               | Crear un archivo a partir de datos personalizados.     |
| Null                                      | Ejecutar código de script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Escriba el valor de **msidbCustomActionTypePatchUninstall** en este campo para especificar una acción personalizada con la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md).

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible. Esta opción está disponible a partir de Windows Installer 4,5.

</dd> </dl>

Para obtener más información, vea todos los temas de [acciones personalizadas](custom-actions.md).

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

 

 



