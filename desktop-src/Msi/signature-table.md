---
description: La tabla Signature contiene la información que identifica de forma única una firma de archivo. Para obtener más información acerca de las firmas, consulte firmas digitales y Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabla de firmas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678069"
---
# <a name="signature-table"></a>Tabla de firmas

La tabla Signature contiene la información que identifica de forma única una firma de archivo. Para obtener más información acerca de las firmas [, consulte firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).

La tabla de firmas tiene las columnas siguientes.



| Columna     | Tipo                               | Clave | Nullable |
|------------|------------------------------------|-----|----------|
| Firma  | [Identificador](identifier.md)       | Y   | N        |
| FileName   | [Texto](text.md)                   | N   | N        |
| MinVersion | [Texto](text.md)                   | N   | Y        |
| MaxVersion | [Texto](text.md)                   | N   | Y        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MinDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Idiomas  | [Texto](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatura
</dt> <dd>

La columna de firma es una firma de archivo única.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre del archivo.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

Versión mínima del archivo, con una comparación de idioma. Si se especifica este campo, el archivo debe tener una versión que sea al menos igual a MinVersion. Si el archivo tiene una versión igual al valor del campo MinVersion pero el idioma especificado en la columna idiomas es distinto, el archivo no cumple los criterios de filtro de firma.

> [!Note]  
> El idioma especificado en la columna idiomas se usa en la comparación y no hay ninguna manera de omitir el idioma. Si desea que un archivo cumpla los requisitos de campo de MinVersion independientemente del idioma, debe escribir un valor en el campo MinVersion que sea uno menos que el valor real. Por ejemplo, si la versión mínima del filtro es 2.0.2600.1183, use 2.0.2600.1182 para buscar el archivo sin que coincida con la información de idioma.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Versión máxima del archivo. Si se especifica este campo, el archivo debe tener una versión que sea como más similar a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Tamaño mínimo del archivo. Si se especifica este campo, el archivo en inspección debe tener un tamaño que sea al menos igual a MinSize. Debe ser un número no negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Tamañomáximo
</dt> <dd>

Tamaño máximo del archivo. Si se especifica este campo, el archivo que se está inspeccionando debe tener un tamaño que sea igual a MaxSize. Debe ser un número no negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

Fecha y hora de modificación mínima del archivo. Si se especifica este campo, el archivo en inspección debe tener una fecha y hora de modificación que sea al menos igual a MinDate. Debe ser un número no negativo. El formato de este campo es dos valores de 16 bits empaquetados de tipo **Word**. El valor de **palabra** de orden superior especifica la fecha en formato de fecha de ms-dos. El valor de **palabra** de orden inferior especifica la hora en formato de hora de ms-dos. Un valor de 0 para el valor de hora representa la medianoche. Consulte la sección Comentarios.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

La fecha de creación máxima del archivo. Si se especifica este campo, el archivo que se inspecciona debe tener una fecha de creación igual a MaxDate. Debe ser un número no negativo. El formato de este campo es dos valores de 16 bits empaquetados de tipo **Word**. El valor de **palabra** de orden superior especifica la fecha en formato de fecha de ms-dos. El valor de **palabra** de orden inferior especifica la hora en formato de hora de ms-dos. Un valor de 0 para el valor de hora representa la medianoche. Consulte la sección Comentarios.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas
</dt> <dd>

Idiomas admitidos por el archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

La firma se busca mediante la [tabla RegLocator](reglocator-table.md), la tabla [IniLocator](inilocator-table.md), la tabla [CompLocator](complocator-table.md)y la [tabla DrLocator](drlocator-table.md). Por lo general, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.

La tabla de firmas suele seguir las [reglas de control de versiones de archivos](file-versioning-rules.md)Windows Installer. Los idiomas especificados en la columna Languages de la tabla Signature no se evalúan a menos que las versiones del archivo sean equivalentes. La columna idiomas garantizará que un archivo sea de un idioma determinado si es de la versión solicitada. No hay ningún método disponible para omitir la columna de idiomas. Un valor NULL especificado en la columna Languages se trata como un archivo sin idioma y no coincide con la firma de archivo de un archivo con un idioma que aparece en la tabla Signature. En el siguiente ejemplo se busca una versión determinada de MSI.DLL.

[Tabla DrLocator](drlocator-table.md)

| Signatura\_ | Parent | Ruta                  | Profundidad |
|-------------|--------|-----------------------|-------|
| MsiDll      | acepta | c: \\ Windows \\ system32 | 0     |



 

[Tabla AppSearch](appsearch-table.md)



| Propiedad | Signatura\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabla de firmas



| Firma | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | MinDate | MaxDate | Idiomas |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | acepta     | acepta  | acepta  | acepta  | acepta  | 0         |



 

En este caso, y en Windows XP SP1, la [acción AppSearch](appsearch-action.md) establece MSIDLL en c: \\ Windows \\ system32 \\msi.dll porque MSI.DLL es un archivo independiente del idioma. Si el valor de la columna Languages se cambia de 0 a 1033, la acción AppSearch no puede encontrar el msi.dll coincidente y la propiedad MSIDLL no está definida.

No se puede usar la tabla de firmas para realizar consultas solo en lenguajes. Para buscar diferentes versiones de idioma de un archivo, debe tener una entrada independiente en la tabla de firmas para cada versión de idioma. Si se proporcionan varios idiomas en la columna idiomas, la búsqueda es para un archivo que admita todos esos idiomas.

El formato de las columnas MinDate y MaxDate son dos valores de 16 bits empaquetados de tipo **Word**.

**Palabra** de fecha



| Bits | Contenido                                             |
|------|-----------------------------------------------------|
| de 0 a 4  | Día del mes (1-31)                             |
| 5-8  | Mes (1 = enero, 2 = febrero, etc.)        |
| 9-15 | Desplazamiento de año desde 1980 (agregue 1980 para obtener el año real) |



 

Hora- **palabra**



| Bits  | Contenido                     |
|-------|-----------------------------|
| de 0 a 4   | Segundos divididos por 2        |
| 5-10  | Minutos (0-59)              |
| 11-15 | Hora (0-23 en el reloj de 24 horas) |



 

La fórmula para calcular los valores de los campos MinDate y MaxDate es la siguiente:

((Año-1980) \* 512 + mes \* 32 + día) \* 65536 + horas \* 2048 + minutos \* 32 + segundos/2

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



