---
description: La tabla CompLocator contiene la información necesaria para buscar un archivo o directorio que use los datos de configuración del instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: CompLocator (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6a51ad618521ff49b2a5b13f76fcfbae4207b5cdf4d77e76d3e128816bbb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145084"
---
# <a name="complocator-table"></a>CompLocator (tabla)

La tabla CompLocator contiene la información necesaria para buscar un archivo o directorio que use los datos de configuración del instalador.

La tabla CompLocator contiene la siguiente información.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificador](identifier.md) | Y   | N        |
| Componentid | [GUID](guid.md)             | N   | N        |
| Tipo        | [Entero](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Información de columna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

Esta columna representa una firma de archivo única y también es la clave externa en la tabla [de firma](signature-table.md). Si la clave no está presente en la tabla de firma, se supone que la búsqueda es para la presencia de un directorio al que apunta la tabla CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

Identificador de componente del componente cuya ruta de acceso de clave se va a usar para la búsqueda. Debe ser el GUID de un componente que aparece en el campo ComponentId de la [tabla de componentes](component-table.md). Puede ser el identificador de componente de un componente que pertenece a otro producto instalado en el equipo. No debe ser el GUID de un componente publicado que aparezca en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).

Para buscar el valor guid del identificador de componente para un archivo instalado por otro producto, vaya al paquete de instalación del producto. Vaya a la [tabla de archivos](file-table.md) y busque la fila que contiene el identificador de archivo del archivo. La columna \_ Componente de esta fila contiene el identificador de componente para el componente que controla el archivo. Vaya a la [tabla Componente y](component-table.md) busque la fila que contiene este identificador de componente en la columna Componente . La columna ComponentId de esta fila contiene el GUID del identificador de componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Valor booleano que determina si la ruta de acceso de clave del componente es un nombre de archivo o una ubicación de directorio.

En la tabla siguiente se enumeran los valores válidos. Si no está presente, Type se establece en 1 (uno).



| Constante                      | Hexadecimal | Decimal | Descripción              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | La ruta de acceso de la clave es un directorio. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | La ruta de acceso de la clave es un nombre de archivo. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta tabla se usa con la [tabla de AppSearch](appsearch-table.md).

Normalmente, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.

Para obtener más información, vea Buscar aplicaciones, archivos, entradas del Registro o [.ini de archivos existentes.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



