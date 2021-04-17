---
description: La tabla RegLocator contiene la información necesaria para buscar un archivo o un directorio mediante el registro, o para buscar una entrada concreta del registro. Esta tabla tiene las columnas siguientes.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabla RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667151"
---
# <a name="reglocator-table"></a>Tabla RegLocator

La tabla RegLocator contiene la información necesaria para buscar un archivo o un directorio mediante el registro, o para buscar una entrada concreta del registro. Esta tabla tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |
| Root        | [Entero](integer.md)       | N   | N        |
| Clave         | [RegPath](regpath.md)       | N   | N        |
| Nombre        | [Formatea](formatted.md)   | N   | Y        |
| Tipo        | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

El valor del campo Signature \_ representa una firma única que es una clave externa en la columna uno de la tabla [Signature](signature-table.md) . Si esta firma está presente en la tabla de firmas, la búsqueda es para un archivo. Si esta firma no está presente en la tabla de firmas y el valor de la columna Type es **msidbLocatorTypeRawValue**, la búsqueda es para el nombre de clave del registro al que apunta la tabla RegLocator. En caso contrario, la búsqueda es para un directorio al que apunta la tabla RegLocator.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces
</dt> <dd>

Clave raíz predefinida para el valor del registro.



| Constante                          | Hexadecimal | Decimal | Clave raíz             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | \_clase HKEY \_ raíz  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | HKEY \_ Current \_ User  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | HKEY \_ local \_ Machine |
| **msidbRegistryRootUsers**        | 0x003       | 3       | \_usuarios HKEY          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave para el valor del registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre del valor del Registro. Si este valor es null, se recupera el valor del valor sin nombre o predeterminado de la clave, si existe.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Un valor que determina si el valor del registro es un nombre de archivo, una ubicación de directorio o un valor de registro sin formato.

En la tabla siguiente se enumeran los valores válidos. Establezca uno de los tres primeros valores y **msidbLocatorType64bit** si es necesario. Si la entrada de este campo no está presente, el tipo se establece en 1.



| Constante                      | Hexadecimal | Decimal | Descripción                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | La ruta de acceso de la clave es un directorio.                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | La ruta de acceso de la clave es un nombre de archivo.                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | La ruta de acceso de la clave es un valor del registro.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Establezca este bit para que el instalador busque en la parte 64 de bits del registro. No establezca este bit para que el instalador busque en la parte 32 de bits del registro. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que si el valor del campo de tipo es **msidbLocatorTypeRawValue**, el instalador establece el valor de la propiedad especificada en el campo de propiedad de la tabla [AppSearch](appsearch-table.md) en el valor del registro. El instalador agrega un prefijo al valor del registro que identifica el tipo de valor del registro. Para obtener más información sobre los tipos de valores del registro, vea [tipos de valor del registro](../sysinfo/registry-value-types.md).



| Tipo de Registro   | Prefijo agregado por el instalador                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Registro \_ SZ         | Ninguno, pero si el primer carácter del valor del registro es \# , el instalador escapa el carácter prefijando otro \# .            |
| DWORD           | " \# " opcionalmente seguido de ' + ' o '-'                                                                                                  |
| REG \_ expandir \_ SZ | "\#%"                                                                                                                                   |
| REG \_ multi \_ SZ  | NULL. El instalador establece la propiedad en un valor que empieza con un valor NULL y termina con un valor null.                                          |
| \_binario de reg     | " \# x" en el caso de reg \_ Binary, el instalador convierte y guarda cada dígito hexadecimal (recorte) como un carácter ASCII precedido por " \# x". |



 

Normalmente, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.

Tenga en cuenta que no es posible usar la tabla RegLocator para comprobar solo la presencia de la clave. Sin embargo, puede buscar el valor predeterminado de una clave y recuperar su valor si no está vacío.

Para obtener más información, vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
