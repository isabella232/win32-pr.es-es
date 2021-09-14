---
description: La tabla Firma contiene la información que identifica de forma única una firma de archivo. Para obtener más información sobre las firmas, vea Firmas digitales y Windows instalador.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabla de firmas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074289"
---
# <a name="signature-table"></a>Tabla de firmas

La tabla Firma contiene la información que identifica de forma única una firma de archivo. Para obtener más información sobre las firmas, vea Firmas digitales [y Windows Installer](digital-signatures-and-windows-installer.md).

La tabla Signature tiene las siguientes columnas.



| Columna     | Tipo                               | Clave | Nullable |
|------------|------------------------------------|-----|----------|
| Firma  | [Identificador](identifier.md)       | Y   | N        |
| FileName   | [Texto](text.md)                   | N   | N        |
| MinVersion | [Texto](text.md)                   | N   | Y        |
| Maxversion | [Texto](text.md)                   | N   | Y        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MinDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Lenguajes  | [Texto](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma
</dt> <dd>

La columna Firma es una firma de archivo única.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Nombre del archivo.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

La versión mínima del archivo, con una comparación de idioma. Si se especifica este campo, el archivo debe tener una versión que sea al menos igual a MinVersion. Si el archivo tiene una versión igual al valor del campo MinVersion, pero el idioma especificado en la columna Idiomas difiere, el archivo no cumple los criterios de filtro de firma.

> [!Note]  
> El idioma especificado en la columna Idiomas se usa en la comparación y no hay ninguna manera de omitir el idioma. Si desea que un archivo cumpla el requisito de campo MinVersion independientemente del lenguaje, debe escribir un valor en el campo MinVersion que sea uno menor que el valor real. Por ejemplo, si la versión mínima del filtro es 2.0.2600.1183, use 2.0.2600.1182 para buscar el archivo sin coincidir con la información de idioma.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>Maxversion
</dt> <dd>

Versión máxima del archivo. Si se especifica este campo, el archivo debe tener una versión que sea como máximo igual a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Tamaño mínimo del archivo. Si se especifica este campo, el archivo que se está inspeccionando debe tener un tamaño igual al menos a MinSize. Debe ser un número no negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Maxsize
</dt> <dd>

Tamaño máximo del archivo. Si se especifica este campo, el archivo que se está inspeccionando debe tener un tamaño igual como máximo a MaxSize. Debe ser un número no negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

Fecha y hora de modificación mínimas del archivo. Si se especifica este campo, el archivo que se está inspeccionando debe tener una fecha y hora de modificación que sea al menos igual a MinDate. Debe ser un número no negativo. El formato de este campo es de dos valores empaquetados de 16 bits de tipo **WORD.** El valor word **de orden** superior especifica la fecha en formato de fecha MS-DOS. El valor **word de orden** bajo especifica la hora en formato de hora MS-DOS. Un valor de 0 para el valor de hora representa la medianoche. Consulte la sección Comentarios.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

Fecha de creación máxima del archivo. Si se especifica este campo, el archivo que se está inspeccionando debe tener una fecha de creación que sea como máximo igual a MaxDate. Debe ser un número no negativo. El formato de este campo es de dos valores empaquetados de 16 bits de tipo **WORD.** El valor word **de orden** superior especifica la fecha en formato de fecha MS-DOS. El valor **word de orden** bajo especifica la hora en formato de hora MS-DOS. Un valor de 0 para el valor de hora representa la medianoche. Consulte la sección Comentarios.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas
</dt> <dd>

Idiomas admitidos por el archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

La firma se busca mediante la [tabla RegLocator](reglocator-table.md), la [tabla IniLocator](inilocator-table.md), la [tabla CompLocator](complocator-table.md)y la [tabla DrLocator](drlocator-table.md). Por lo general, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.

La tabla Firma suele seguir las reglas de control de versiones Windows [archivo del instalador.](file-versioning-rules.md) Los idiomas especificados en la columna Idiomas de la tabla Firma no se evalúan a menos que las versiones de archivo sean equivalentes. La columna Idiomas garantizará que un archivo sea de un idioma determinado si es de la versión solicitada. No hay ningún método disponible para omitir la columna Idiomas. Un valor NULL especificado en la columna Idiomas se trata como un archivo sin un idioma y no coincide con la firma de archivo de un archivo con un idioma que aparece en la tabla Firma. En el ejemplo siguiente se busca una versión determinada de MSI.DLL.

[Tabla DrLocator](drlocator-table.md)

| Firma\_ | Parent | Path                  | Profundidad |
|-------------|--------|-----------------------|-------|
| MsiDll      | {null} | c: \\ windows \\ system32 | 0     |



 

[Tabla de AppSearch](appsearch-table.md)



| Propiedad. | Firma\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabla de firmas



| Firma | FileName | MinVersion    | Maxversion | MinSize | MaxSize | MinDate | MaxDate | Lenguajes |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | {null}     | {null}  | {null}  | {null}  | {null}  | 0         |



 

En este caso, y en Windows XP SP1, la acción [AppSearch](appsearch-action.md) establece MSIDLL en c: windows system32msi.dll porque MSI.DLL es un archivo neutro del \\ \\ \\ lenguaje. Si el valor de la columna Languages se cambia de 0 a 1033, la acción AppSearch no encuentra el valor de msi.dll y la propiedad MSIDLL no está definida.

No se puede usar la tabla Signature para consultar solo los idiomas. Para buscar versiones de idioma diferentes de un archivo, debe tener una entrada independiente en la tabla Firma para cada versión de idioma. Si se proporcionan varios idiomas en la columna Idiomas, la búsqueda es para un archivo que admita todos esos idiomas.

El formato de las columnas MinDate y MaxDate son dos valores empaquetados de 16 bits de tipo **WORD.**

Fecha **WORD**



| Bits | Contenido                                             |
|------|-----------------------------------------------------|
| 0–4  | Día del mes (1-31)                             |
| 5-8  | Mes (1 = enero, 2 = febrero, y así sucesivamente)        |
| 9-15 | Ajuste de año de 1980 (agregue 1980 para obtener el año real) |



 

Palabra **de tiempo**



| Bits  | Contenido                     |
|-------|-----------------------------|
| 0–4   | Segundos divididos por 2        |
| 5-10  | Minutos (0-59)              |
| 11-15 | Hora (de 0 a 23 en el reloj de 24 horas) |



 

La fórmula para calcular los valores de campo MinDate y MaxDate es:

( (Año - 1980) \* 512 + Mes \* 32 + Día ) \* 65536 + Horas \* 2048 + Minutos \* 32 + Segundos/2

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



