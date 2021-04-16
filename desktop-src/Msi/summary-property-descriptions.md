---
description: En las tablas siguientes se describen las propiedades de Resumen de los paquetes de instalación, las transformaciones y las revisiones.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descripciones de propiedades de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678399"
---
# <a name="summary-property-descriptions"></a>Descripciones de propiedades de Resumen

En las tablas siguientes se describen las propiedades de Resumen de los paquetes de instalación, las transformaciones y las revisiones. Tenga en cuenta que el significado de una propiedad de Resumen determinada puede variar en función de si la base de datos pertenece a un paquete de instalación, transformación o paquete de revisión. Para obtener más información sobre los identificadores de propiedad, los PID y los tipos, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Paquetes de instalación



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Summary (propiedad)</th>
<th>Significado de esta propiedad en una base de datos de instalación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Title</strong></a></td>
<td>Descripción de este archivo como un paquete de instalación. La descripción debe incluir la frase &quot; <a href="about-the-installer-database.md">base de datos de instalación</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Asunto</strong></a></td>
<td>Nombre del producto instalado por este paquete. Debe ser el mismo nombre que en la propiedad <a href="productname.md"><strong>ProductName</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Nombre del fabricante de este producto. Debe ser el mismo nombre que en la propiedad <a href="manufacturer.md"><strong>manufacturer</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palabras clave</strong></a></td>
<td>Una lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave para un archivo. Las palabras clave deben incluir el &quot; instalador &quot; y las palabras clave específicas del producto.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentarios</strong></a></td>
<td>Contiene la frase: &quot; esta base de datos del instalador contiene la lógica y los datos necesarios para instalar <<em>nombre del producto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Plantilla</strong></a> (obligatorio)</td>
<td>La plataforma y los lenguajes compatibles con este paquete de instalación. Vea la <a href="template-summary.md"><strong>plantilla</strong></a> para ver la sintaxis.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></td>
<td>Los desarrolladores de herramientas de edición de bases de datos pueden utilizar esta propiedad durante el proceso de desarrollo para realizar un seguimiento de la última persona que modificó la base de datos de instalación. Esta propiedad debe establecerse en null en una base de datos de envío final. El instalador establece esta propiedad en el valor de la propiedad <a href="logonuser.md"><strong>LogonUser</strong></a> durante una <a href="administrative-installation.md"><strong>instalación administrativa</strong></a>. El instalador nunca usa esta propiedad y un usuario nunca necesita modificarla.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (obligatorio)</td>
<td>Contiene el <a href="package-codes.md">código de paquete</a> para el paquete del instalador.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última impresión</strong></a></td>
<td>Se puede establecer en la fecha y hora durante una <a href="administrative-installation.md">instalación administrativa</a> para registrar Cuándo se creó la imagen administrativa.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Crear hora/fecha</strong></a></td>
<td>Fecha y hora en que se creó la base de datos del instalador.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Fecha y hora de la última vez que se guardó</strong></a></td>
<td>Fecha y hora actuales del sistema en el momento en que se guardó por última vez la base de datos del instalador. Inicialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (obligatorio)</td>
<td>Contiene un valor que se usa para identificar la versión mínima del instalador requerida por este paquete de instalación. Por ejemplo, si el paquete requiere como mínimo la versión 2,0 del instalador, esta propiedad debe establecerse en un entero de 200.
<blockquote>
[!Note]<br />
El valor de esta propiedad debe ser 200 o superior con <a href="64-bit-windows-installer-packages.md">paquetes de Windows Installer de 64 bits</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (obligatorio)</td>
<td>Tipo de la imagen de archivo de origen. Almacenado en lugar de la propiedad de recuento estándar. Esta propiedad es un campo de bits. Vea el tema <a href="word-count-summary.md"><strong>recuento de palabras</strong></a> para los valores.<br/> A partir de Windows Installer versión 4,0 en Windows Vista, esta propiedad incluye bits para especificar si se requieren privilegios elevados.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creando aplicación</strong></a></td>
<td>Contiene el nombre del software utilizado para crear esta base de datos de instalación.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Seguridad</strong></a></td>
<td>El valor de esta propiedad debe ser 2 recomendado solo lectura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>737</strong></a></td>
<td>Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen. Esta propiedad debe establecerse antes de que se establezcan las propiedades de cadena en la información de resumen.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformaciones



| Summary (propiedad)                                              | Significado de esta propiedad en una transformación                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Title**](title-summary.md)                                | Descripción de este archivo como una transformación. La descripción debe incluir la frase: "[Transform](database-transforms.md)".                                                                                                                                                                     |
| [**Asunto**](subject-summary.md)                            | Nombre del producto instalado por el paquete de instalación original. Debe ser el mismo valor que la propiedad de [**Resumen del asunto**](subject-summary.md) en el paquete de instalación original.                                                                                            |
| [**Autor**](author-summary.md)                              | Nombre del fabricante de esta transformación.                                                                                                                                                                                                                                                   |
| [**Palabras clave**](keywords-summary.md)                          | Una lista de palabras clave que pueden usar los exploradores de archivos para realizar búsquedas de palabras clave para un archivo. Las palabras clave deben incluir "Installer", así como palabras clave específicas del producto.                                                                                                                             |
| [**Comentarios**](comments-summary.md)                          | Contiene la frase: "esta transformación contiene la lógica y los datos necesarios para instalar <*nombre de producto*>".                                                                                                                                                                                     |
| [**Plantilla**](template-summary.md) (obligatorio)               | Versiones de plataforma e idioma compatibles con esta transformación. Este valor puede dejarse en blanco si no hay ninguna restricción. Solo se puede especificar un idioma para una transformación. Para obtener más información sobre la sintaxis, consulte [**Template**](template-summary.md).                                |
| [**Guardado por última vez por**](last-saved-by-summary.md)                | Los IDENTIFICADOres de plataforma e idioma que tiene la base de datos una vez transformada. La propiedad de [**Resumen de plantilla**](template-summary.md) de la nueva base de datos debe establecerse en los mismos valores.                                                                                              |
| [**Número de revisión**](revision-number-summary.md) (obligatorio) | Una lista de los GUID de código de producto y la versión de los productos nuevos y originales y el GUID del código de actualización. La lista está separada por punto y coma como se indica a continuación. *Original-Product-Code original-Product-version*; *New-Product Code New-Product-version*; *Actualización: código*<br/>                       |
| [**Última impresión**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**Crear hora/fecha**](create-time-date-summary.md)          | Fecha y hora en que se creó la transformación.                                                                                                                                                                                                                                                 |
| [**Fecha y hora de la última vez que se guardó**](last-saved-time-date-summary.md)  | Fecha y hora actuales del sistema en el momento en que se guardó la transformación. Inicialmente null.                                                                                                                                                                                                             |
| [**Recuento de páginas**](page-count-summary.md) (obligatorio)           | Valor que se usa para indicar la versión mínima del instalador necesaria para procesar la transformación. El valor se debe establecer en el mayor de los dos valores de propiedad de [**recuento de páginas**](page-count-summary.md) que pertenecen a las bases de datos utilizadas para generar la transformación.                                 |
| [**Recuento de palabras**](word-count-summary.md) (obligatorio)           | Null                                                                                                                                                                                                                                                                                              |
| [**Recuento de caracteres**](character-count-summary.md)            | Esta parte de la secuencia de información de resumen se divide en palabras de 2 16 bits. La palabra superior contiene [*marcas de validación de transformación*](t-gly.md). La palabra inferior contiene [*marcas de condición de error de transformación*](t-gly.md). |
| [**Creando aplicación**](creating-application-summary.md)  | Contiene el nombre del software utilizado para crear esta transformación.                                                                                                                                                                                                                                  |
| [**Seguridad**](security-summary.md)                          | El valor de esta propiedad debe ser de solo lectura.                                                                                                                                                                                                                                      |
| [**737**](codepage-summary.md)                          | Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen. Esta propiedad debe establecerse antes de que se puedan establecer las propiedades de cadena en la información de resumen.                                                                                                                    |



 

## <a name="patch-packages"></a>Paquetes de revisión



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Summary (propiedad)</th>
<th>Significado de esta propiedad en un paquete de revisión</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Title</strong></a></td>
<td>Una descripción de este archivo como un paquete de revisión. La descripción debe incluir la frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Asunto</strong></a></td>
<td>Una descripción de la revisión que incluye el nombre del producto.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>Nombre del fabricante del paquete de revisión.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palabras clave</strong></a></td>
<td>Una lista delimitada por punto y coma de orígenes de la revisión.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentarios</strong></a></td>
<td>Contiene la frase: &quot; esta revisión contiene la lógica y los datos necesarios para instalar <<em>nombre del producto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Plantilla</strong></a> (obligatorio)</td>
<td>Una lista delimitada por punto y coma de los códigos de producto que pueden aceptar esta revisión.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Guardado por última vez por</strong></a></td>
<td>Una lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se aplican en esta revisión.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisión</strong></a> (obligatorio)</td>
<td>Contiene el código de revisión del GUID de la revisión. Esto puede ir seguido de una lista de GUID de código de revisión para las revisiones que se quitan cuando se aplica esta revisión. Los códigos de revisión se concatenan sin delimitadores que separan los GUID de la lista.
<blockquote>
[!Note]<br />
Si el paquete de revisión contiene una tabla <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , la revisión no quita las revisiones enumeradas después del GUID de la revisión actual.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última impresión</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Crear hora/fecha</strong></a></td>
<td>Fecha y hora en que se creó el archivo de revisión.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Fecha y hora de la última vez que se guardó</strong></a></td>
<td>Fecha y hora actuales del sistema en el momento en que se guardó el paquete de revisión. Este valor es inicialmente null.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Recuento de páginas</strong></a> (obligatorio)</td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Recuento de palabras</strong></a> (obligatorio)</td>
<td>Contiene un valor que indica la versión mínima Windows Installer necesaria para instalar la revisión. Una revisión con un valor de recuento de palabras de 4 requiere Windows Installer versión 3,0 o posterior para que se aplique la revisión. Un valor de 3 indica que se requiere Windows Installer versión 2,0 o posterior. Un valor de 2 indica que se requiere Windows Installer versión 1,2 o posterior. El valor predeterminado es 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Recuento de caracteres</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Creando aplicación</strong></a></td>
<td>Nombre del software que se usa para crear la revisión.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Seguridad</strong></a></td>
<td>El valor de esta propiedad debe ser de solo lectura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>737</strong></a></td>
<td>Valor numérico de la página de códigos ANSI que se usa para mostrar la información de resumen. Esta propiedad debe establecerse antes de que se establezcan las propiedades de cadena en la información de resumen.</td>
</tr>
</tbody>
</table>



 

 

 




