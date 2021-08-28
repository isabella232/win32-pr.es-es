---
description: Las propiedades de resumen de paquetes de instalación, transformaciones y revisiones se describen en las tablas siguientes.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descripciones de propiedades de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb93e5881a25b6b79eef0fb0711acc1fec1b6666
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629548"
---
# <a name="summary-property-descriptions"></a>Descripciones de propiedades de resumen

Las propiedades de resumen de paquetes de instalación, transformaciones y revisiones se describen en las tablas siguientes. Tenga en cuenta que el significado de una propiedad de resumen determinada puede ser diferente en función de si la base de datos pertenece a un paquete de instalación, transformación o paquete de revisión. Para obtener más información sobre los IDs de propiedad, LOS PID y los tipos, vea Resumen del conjunto de propiedades de flujo [de información](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Paquetes de instalación



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad Resumen</th>
<th>Significado de esta propiedad en una base de datos de instalación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Título</strong></a></td>
<td>Descripción de este archivo como paquete de instalación. La descripción debe incluir la frase Base &quot; <a href="about-the-installer-database.md">de datos de instalación</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Subject</strong></a></td>
<td>Nombre del producto instalado por este paquete. Debe ser el mismo nombre que en la <a href="productname.md"><strong>propiedad ProductName.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Nombre del fabricante de este producto. Debe ser el mismo nombre que en la <a href="manufacturer.md"><strong>propiedad Fabricante.</strong></a></td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palabras clave</strong></a></td>
<td>Lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave en un archivo. Las palabras clave deben incluir &quot; &quot; installer, así como palabras clave específicas del producto.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentarios</strong></a></td>
<td>Contiene la frase: Esta base de datos del instalador contiene la lógica y los datos necesarios para &quot; instalar <nombre del <em>producto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Plantilla</strong></a> (OBLIGATORIO)</td>
<td>La plataforma y los idiomas compatibles con este paquete de instalación. Consulte <a href="template-summary.md"><strong>Plantilla para</strong></a> obtener sintaxis.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></td>
<td>Los desarrolladores de herramientas de edición de bases de datos pueden usar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modifique la base de datos de instalación. Esta propiedad debe establecerse en Null en una base de datos de envío final. El instalador establece esta propiedad en el valor de la propiedad <a href="logonuser.md"><strong>LogonUser</strong></a> durante una <a href="administrative-installation.md"><strong>instalación administrativa.</strong></a> El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (OBLIGATORIO)</td>
<td>Contiene el <a href="package-codes.md">código del paquete</a> del instalador.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última impresión</strong></a></td>
<td>Se puede establecer en la fecha y hora durante una <a href="administrative-installation.md">instalación administrativa</a> para registrar cuándo se creó la imagen administrativa.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Fecha y hora de creación</strong></a></td>
<td>Fecha y hora en que se creó esta base de datos del instalador.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Fecha y hora del último guardado</strong></a></td>
<td>Fecha y hora actuales del sistema en el momento en que se guardó por última vez la base de datos del instalador. Inicialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (OBLIGATORIO)</td>
<td>Contiene un valor que se usa para identificar la versión mínima del instalador requerida por este paquete de instalación. Por ejemplo, si el paquete requiere como mínimo la versión 2.0 del instalador, esta propiedad debe establecerse en un entero de 200.
<blockquote>
[!Note]<br />
El valor de esta propiedad debe ser 200 o superior con paquetes del instalador Windows de <a href="64-bit-windows-installer-packages.md">64 bits.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (OBLIGATORIO)</td>
<td>Tipo de la imagen de archivo de origen. Se almacena en lugar de la propiedad Count estándar. Esta propiedad es un campo de bits. Vea el <a href="word-count-summary.md"><strong>tema Recuento de</strong></a> palabras para los valores.<br/> A partir Windows Installer versión 4.0 en Windows Vista, esta propiedad incluye bits para especificar si se requieren privilegios elevados.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creación de una aplicación</strong></a></td>
<td>Contiene el nombre del software usado para crear esta base de datos de instalación.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Seguridad</strong></a></td>
<td>El valor de esta propiedad debe ser 2: solo lectura recomendado.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Valor numérico de la página de códigos ANSI utilizada para mostrar la información de resumen. Esta propiedad debe establecerse antes de que se establezcan las propiedades de cadena en la información de resumen.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformaciones



| Propiedad Resumen                                              | Significado de esta propiedad en una transformación                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Título**](title-summary.md)                                | Descripción de este archivo como una transformación. La descripción debe incluir la frase:["Transformar".](database-transforms.md)                                                                                                                                                                     |
| [**Subject**](subject-summary.md)                            | Nombre del producto instalado por el paquete de instalación original. Debe ser el mismo valor que la propiedad [**Resumen del asunto**](subject-summary.md) en el paquete de instalación original.                                                                                            |
| [**Autor**](author-summary.md)                              | Nombre del fabricante de esta transformación.                                                                                                                                                                                                                                                   |
| [**Palabras clave**](keywords-summary.md)                          | Lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave en un archivo. Las palabras clave deben incluir "Installer", así como palabras clave específicas del producto.                                                                                                                             |
| [**Comentarios**](comments-summary.md)                          | Contiene la frase: "Esta transformación contiene la lógica y los datos necesarios para instalar <*nombre de* producto>".                                                                                                                                                                                     |
| [**Plantilla**](template-summary.md) (OBLIGATORIO)               | Las versiones de plataforma y lenguaje compatibles con esta transformación. Este valor se puede dejar en blanco si no hay ninguna restricción. Solo se puede especificar un idioma para una transformación. Para obtener más información sobre la sintaxis, vea [**Template**](template-summary.md).                                |
| [**Guardado por última vez por**](last-saved-by-summary.md)                | La plataforma y los identificadores de lenguaje que tiene la base de datos después de que se haya transformado. La [**propiedad Resumen de plantilla**](template-summary.md) de la nueva base de datos debe establecerse en los mismos valores.                                                                                              |
| [**Número de revisión**](revision-number-summary.md) (OBLIGATORIO) | Una lista de los GUID del código de producto y la versión de los productos nuevos y originales, así como el GUID del código de actualización. La lista está separada por punto y coma como se muestra a continuación. *Original-Product-Code Original-Product-Version*; *New-Product Code New-Product-Version*; *Upgrade-Code*<br/>                       |
| [**Última impresión**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Fecha y hora de creación**](create-time-date-summary.md)          | Hora y fecha en que se creó la transformación.                                                                                                                                                                                                                                                 |
| [**Fecha y hora del último guardado**](last-saved-time-date-summary.md)  | La fecha y la hora actuales del sistema en el momento en que se guardó la transformación. Inicialmente null.                                                                                                                                                                                                             |
| [**Recuento de páginas**](page-count-summary.md) (OBLIGATORIO)           | Valor que se usa para indicar la versión mínima del instalador necesaria para procesar la transformación. El valor debe establecerse en el mayor de los dos valores de propiedad [**Recuento**](page-count-summary.md) de páginas que pertenecen a las bases de datos utilizadas para generar la transformación.                                 |
| [**Recuento de palabras**](word-count-summary.md) (OBLIGATORIO)           | Null                                                                                                                                                                                                                                                                                              |
| [**Recuento de caracteres**](character-count-summary.md)            | Esta parte del flujo de información de resumen se divide en dos palabras de 16 bits. La palabra superior contiene marcas [*de validación de transformación*](t-gly.md). La palabra inferior contiene [*marcas de condición de error de transformación*](t-gly.md). |
| [**Creación de una aplicación**](creating-application-summary.md)  | Contiene el nombre del software usado para crear esta transformación.                                                                                                                                                                                                                                  |
| [**Seguridad**](security-summary.md)                          | El valor de esta propiedad debe ser 4: solo lectura aplicada.                                                                                                                                                                                                                                      |
| [**Codepage**](codepage-summary.md)                          | Valor numérico de la página de códigos ANSI utilizada para mostrar la información de resumen. Esta propiedad debe establecerse antes de que se puedan establecer propiedades de cadena en la información de resumen.                                                                                                                    |



 

## <a name="patch-packages"></a>Paquetes de revisión



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad Summary</th>
<th>Significado de esta propiedad en un paquete de revisión</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Título</strong></a></td>
<td>Descripción de este archivo como un paquete de revisión. La descripción debe incluir la frase: &quot; <a href="patch-packages.md">Patch</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Subject</strong></a></td>
<td>Descripción de la revisión que incluye el nombre del producto.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Nombre del fabricante del paquete de revisión.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palabras clave</strong></a></td>
<td>Lista delimitada por punto y coma de orígenes de la revisión.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentarios</strong></a></td>
<td>Contiene la frase: Esta revisión contiene la lógica y los datos necesarios para instalar &quot; <nombre de <em>producto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Plantilla</strong></a> (OBLIGATORIO)</td>
<td>Lista delimitada por punto y coma de los códigos de producto que pueden aceptar esta revisión.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></td>
<td>Lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican mediante esta revisión.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (OBLIGATORIO)</td>
<td>Contiene el código de revisión guid de la revisión. Esto puede estar seguido de una lista de GUID de código de revisión para las revisiones que se quitan cuando se aplica esta revisión. Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.
<blockquote>
[!Note]<br />
Si el paquete de revisión contiene una tabla <a href="msipatchsequence-table.md"><strong>MsiPatchSequence,</strong></a> la revisión no quita las revisiones enumeradas después del GUID de la revisión actual.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última impresión</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Fecha y hora de creación</strong></a></td>
<td>Fecha y hora en que se creó el archivo de revisión.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Hora y fecha del último guardado</strong></a></td>
<td>La fecha y hora actuales del sistema en el momento en que se guardó el paquete de revisión. Este valor es inicialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (OBLIGATORIO)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (OBLIGATORIO)</td>
<td>Contiene un valor que indica la versión Windows del instalador necesaria para instalar la revisión. Una revisión con un valor de recuento de palabras de 4 requiere Windows installer versión 3.0 o posterior para que se aplique la revisión. Un valor de 3 indica que se requiere Windows installer versión 2.0 o posterior. Un valor de 2 indica que Windows installer versión 1.2 o posterior. El valor predeterminado es 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creación de una aplicación</strong></a></td>
<td>Nombre del software usado para crear la revisión.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Seguridad</strong></a></td>
<td>El valor de esta propiedad debe ser 4: solo lectura aplicada.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Codepage</strong></a></td>
<td>Valor numérico de la página de códigos ANSI utilizada para mostrar la información de resumen. Esta propiedad debe establecerse antes de que las propiedades de cadena se establezcan en la información de resumen.</td>
</tr>
</tbody>
</table>



 

 

 




