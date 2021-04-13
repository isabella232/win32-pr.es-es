---
description: La tabla CompLocator contiene la información necesaria para buscar un archivo o un directorio que use los datos de configuración del instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabla CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547011"
---
# <a name="complocator-table"></a>Tabla CompLocator

La tabla CompLocator contiene la información necesaria para buscar un archivo o un directorio que use los datos de configuración del instalador.

La tabla CompLocator contiene la siguiente información.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |
| ComponentId | [GUID](guid.md)             | N   | N        |
| Tipo        | [Entero](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Información de columna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

Esta columna representa una firma de archivo única y también es la clave externa en la [tabla de firmas](signature-table.md). Si la clave no está presente en la tabla de firmas, se supone que se trata de la presencia de un directorio señalado por la tabla CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

IDENTIFICADOR de componente del componente cuya ruta de acceso de clave se va a usar para la búsqueda. Debe ser el GUID de un componente que aparece en el campo ComponentId de la [tabla de componentes](component-table.md). Puede ser el identificador de componente de un componente que pertenece a otro producto instalado en el equipo. No debe ser el GUID de un componente publicado que aparece en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).

Para buscar el valor GUID del identificador de componente para un archivo instalado por otro producto, vaya al paquete de instalación del producto. Vaya a la [tabla de archivos](file-table.md) y busque la fila que contiene el identificador de archivo del archivo. La \_ columna componente de esta fila contiene el identificador de componente del componente que controla el archivo. Vaya a la [tabla de componentes](component-table.md) y busque la fila que contiene este identificador de componente en la columna componente. La columna ComponentId de esta fila contiene el GUID del identificador del componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Valor booleano que determina si la ruta de acceso de la clave del componente es un nombre de archivo o una ubicación de directorio.

En la tabla siguiente se enumeran los valores válidos. Si no está presente, el tipo se establece en 1 (uno).



| Constante                      | Hexadecimal | Decimal | Descripción              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | La ruta de acceso de la clave es un directorio. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | La ruta de acceso de la clave es un nombre de archivo. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

Normalmente, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.

Para obtener más información, vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



