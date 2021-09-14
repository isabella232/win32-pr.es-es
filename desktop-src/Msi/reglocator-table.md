---
description: La tabla RegLocator contiene la información necesaria para buscar un archivo o directorio mediante el Registro o para buscar una entrada del Registro determinada. Esta tabla tiene las columnas siguientes.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: RegLocator Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069678"
---
# <a name="reglocator-table"></a>RegLocator Table

La tabla RegLocator contiene la información necesaria para buscar un archivo o directorio mediante el Registro o para buscar una entrada del Registro determinada. Esta tabla tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificador](identifier.md) | Y   | N        |
| Root        | [Entero](integer.md)       | N   | N        |
| Clave         | [RegPath](regpath.md)       | N   | N        |
| Nombre        | [Formato](formatted.md)   | N   | Y        |
| Tipo        | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

El valor del campo Firma representa una firma única que es una clave \_ externa en la columna uno de la tabla [Firma.](signature-table.md) Si esta firma está presente en la tabla Firma, la búsqueda es para un archivo. Si esta firma no está presente en la tabla Signature y el valor de la columna Type es **msidbLocatorTypeRawValue,** la búsqueda es para el nombre de clave del Registro al que apunta la tabla RegLocator. De lo contrario, la búsqueda es para un directorio al que apunta la tabla RegLocator.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíz
</dt> <dd>

Clave raíz predefinida para el valor del Registro.



| Constante                          | Hexadecimal | Decimal | Clave raíz             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | RAÍZ DE CLASES HKEY \_ \_  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | USUARIO ACTUAL DE HKEY \_ \_  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | HKEY \_ LOCAL \_ MACHINE |
| **msidbRegistryRootUsers**        | 0x003       | 3       | USUARIOS DE \_ HKEY          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave para el valor del Registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del valor del Registro. Si este valor es NULL, se recupera el valor del valor sin nombre o predeterminado de la clave, si existe.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Valor que determina si el valor del Registro es un nombre de archivo, una ubicación de directorio o un valor del Registro sin formato.

En la tabla siguiente se enumeran los valores válidos. Establezca uno de los tres primeros valores y **msidbLocatorType64bit** si es necesario. Si la entrada de este campo no está presente, Type se establece en 1.



| Constante                      | Hexadecimal | Decimal | Descripción                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | La ruta de acceso de la clave es un directorio.                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | La ruta de acceso de la clave es un nombre de archivo.                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | La ruta de acceso de clave es un valor del Registro.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Establezca este bit para que el instalador busque la parte de 64 bits del registro. No establezca este bit para que el instalador busque la parte de 32 bits del registro. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que si el valor del campo Tipo es **msidbLocatorTypeRawValue,** el instalador establece el valor de la propiedad especificada en el campo Propiedad de la tabla [AppSearch](appsearch-table.md) en el valor del Registro. El instalador agrega un prefijo al valor del Registro que identifica el tipo de valor del Registro. Para obtener más información sobre los tipos de valores del Registro, vea [Tipos de valor del Registro](../sysinfo/registry-value-types.md).



| Tipo de Registro   | Prefijo agregado por el instalador                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ SZ         | Ninguno, pero si el primer carácter del valor del Registro es , el instalador se escapará del \# carácter anteciendo a otro \# .            |
| DWORD           | " \# " opcionalmente seguido de '+' o '-'                                                                                                  |
| REG \_ EXPAND \_ SZ | "\#%"                                                                                                                                   |
| REG \_ MULTI \_ SZ  | NULL. El instalador establece la propiedad en un valor que comienza con un valor NULL y termina con un valor NULL.                                          |
| REG \_ BINARY     | "x" En el caso de REG BINARY, el instalador convierte y guarda cada dígito \# hexadecimal (nibble) como un carácter ASCII precedido \_ por \# "x". |



 

Normalmente, las columnas de esta tabla no se localizan. Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.

Tenga en cuenta que no es posible usar la tabla RegLocator para comprobar solo la presencia de la clave. Sin embargo, puede buscar el valor predeterminado de una clave y recuperar su valor si no está vacía.

Para obtener más información, vea Buscar aplicaciones, archivos, entradas del Registro o [.ini de archivos existentes.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
