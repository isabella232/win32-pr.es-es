---
title: Sintaxis de consulta avanzada
description: La sintaxis de consulta avanzada (AQS) se usa en la búsqueda de escritorio de Microsoft Windows (WDS) para ayudar a los usuarios y a los programadores a definir y restringir mejor sus búsquedas.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "105695566"
---
# <a name="advanced-query-syntax"></a>Sintaxis de consulta avanzada

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

La sintaxis de consulta avanzada (AQS) se usa en la búsqueda de escritorio de Microsoft Windows (WDS) para ayudar a los usuarios y a los programadores a definir y restringir mejor sus búsquedas. El uso de AQS es una forma sencilla de limitar las búsquedas y ofrecer mejores conjuntos de resultados. Las búsquedas se pueden restringir mediante los siguientes parámetros:

-   Tipos de archivo: carpetas, documentos, presentaciones, imágenes, etc.
-   Almacenes de archivos: bases de datos y ubicaciones específicas.
-   Propiedades de archivo: tamaño, fecha, título, etc.
-   Contenido del archivo: Palabras clave como "entregas del proyecto", "AQS", "zapatos Blue Suede Shoes", etc.

Además, los parámetros de búsqueda se pueden combinar con los operadores de búsqueda. En el resto de esta sección se explica la sintaxis de la consulta, los parámetros y los operadores, y cómo se pueden combinar para ofrecer resultados de búsqueda de destino. En las tablas se describe la sintaxis que se usa con WDS, así como las propiedades que se pueden consultar para cada tipo de archivo que se muestra en la ventana Resultados de la **búsqueda de escritorio de Windows** .

## <a name="desktop-search-syntax"></a>Sintaxis de búsqueda de escritorio

Una consulta de búsqueda puede incluir una o más palabras clave, con operadores booleanos y criterios opcionales. Estos criterios opcionales pueden restringir una búsqueda basada en lo siguiente:

-   Ámbito o almacén de datos en el que residen los archivos
-   Tipos de archivos
-   Propiedades administradas de los archivos

Los criterios opcionales, que se describen con más detalle a continuación, usan la sintaxis siguiente:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Supongamos que un usuario desea buscar un documento que contenga la frase "Last Quarter", creada por John o Joanne, y que el usuario guardado en la carpeta Mis documentos. La consulta puede tener el siguiente aspecto:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Ámbito: ubicaciones y almacenes de datos

Los usuarios pueden limitar el ámbito de las búsquedas a ubicaciones de carpeta o almacenes de datos específicos. Por ejemplo, si utiliza varias cuentas de correo electrónico y desea limitar una consulta a Microsoft Outlook o Microsoft Outlook Express, puede utilizar `store:outlook` o `store:oe` respectivamente.



| Restricción de búsqueda por almacén de datos | Use              | Ejemplo                                  |
|-------------------------------|------------------|------------------------------------------|
| Escritorio                       | escritorio          | Tienda: escritorio                            |
| Archivos                         | files            | almacén: archivos                              |
| Outlook                       | Outlook          | Tienda: Outlook                            |
| Outlook Express               | oe               | almacén: OE                                 |
| Carpeta específica               | NombreCarpeta o in | NombreCarpeta: mis documentos o in: mis documentos |



 

Si tiene un controlador de protocolo en su lugar para rastrear almacenes personalizados, como Lotus Notes, puede usar el nombre del almacén o del controlador del protocolo para el almacén. Por ejemplo, si ha implementado un controlador de protocolo para incluir un almacén de datos de Lotus Notes como "Notas", la sintaxis de la consulta sería `store:notes` .

### <a name="common-file-kinds"></a>Tipos de archivo comunes

Los usuarios también pueden limitar sus búsquedas a tipos específicos de archivos, denominados tipos de archivo. En la tabla siguiente se enumeran los tipos de archivo y se ofrecen ejemplos de la sintaxis que se usa para buscar estos tipos de archivos.



| Para restringir por tipo de archivo:       | Use              | Ejemplo                        |
|---------------------------------|------------------|--------------------------------|
| Todos los tipos de archivo                  | hay       | Kind: todo                |
| Comunicaciones                  | comunicaciones   | tipo: comunicaciones            |
| Contactos                        | contactos         | Kind: contactos                  |
| Correo electrónico                          | email            | tipo: correo electrónico                     |
| Conversaciones de Messenger instantáneo | instantáne               | Kind: IM                        |
| Reuniones                        | mantener         | tipo: reuniones                  |
| Tareas                           | tareas            | tipo: tareas                     |
| Notas                           | HDInsight            | tipo: notas                     |
| Documentos                       | Documentación             | tipo: docs                      |
| Documentos de texto                  | text             | Kind: texto                      |
| Hojas de cálculo                    | hojas     | Kind: hojas de cálculo              |
| Presentaciones                   | presentaciones    | tipo: presentaciones             |
| Música                           | music            | tipo: música                     |
| Imágenes                        | selecciones             | Kind: pics                      |
| Vídeos                          | videos           | tipo: vídeos                    |
| Carpetas                         | carpetas          | Kind: carpetas                   |
| Nombre de carpeta                     | NombreCarpeta o in | NombreCarpeta: mis documentos o in: mis documentos |
| Favoritos                       | favoritos        | Kind: Favoritos                 |
| Programas                        | programas         | tipo: programas                  |



 

### <a name="boolean-operators"></a>Operadores booleanos

Las palabras clave de búsqueda y las propiedades de archivo se pueden combinar para ampliar o reducir una búsqueda con operadores. En la tabla siguiente se explican los operadores comunes que se usan en una consulta de búsqueda.



| Palabra clave/símbolo  | Ejemplos                                              | Función                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | social no seguridad<br/>                        | Busca elementos que contengan *redes sociales*, pero no *seguridad*.<br/>                                              |
|                 | seguridad social<br/>                           | Busca elementos que contengan la seguridad *social* y la *seguridad*.<br/>                                              |
| O BIEN              | social o de seguridad<br/>                         | Busca elementos que contengan el *social* o la *seguridad*.<br/>                                                    |
| Comillas | "seguridad social"<br/>                          | Busca elementos que contengan la frase exacta *seguridad social*.<br/>                                        |
| Paréntesis     | (seguridad social)<br/>                          | Busca elementos que contengan la *seguridad* *social* y en cualquier orden.<br/>                                      |
| >            | Fecha: >11/05/04<br/> tamaño: >500<br/>  | Busca elementos con una fecha posterior a 11/05/04. <br/> Busca elementos con un tamaño superior a 500 bytes.<br/> |
| <            | Fecha: <11/05/04 <br/> tamaño: <500<br/> | Busca elementos con una fecha anterior a 11/05/04. <br/> Busca elementos con un tamaño inferior a 500 bytes.<br/>   |
| ..              | Fecha: 11/05/04.. 11/10/04<br/>                    | Busca elementos con una fecha que empiece en 11/05/04 y termina en 11/10/04.<br/>                               |



 

> [!Note]
>
> Los operadores **Not** y **or** deben estar en mayúsculas y no se pueden combinar en una consulta (por ejemplo, `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Propiedades booleanas

Algunos tipos de archivo permiten a los usuarios buscar archivos mediante propiedades booleanas, como se describe en la tabla siguiente.



| Propiedad       | Ejemplo                   | Función                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| is: Attachment  | el informe es: datos adjuntos      | Busca elementos que tengan datos adjuntos que contengan el *Informe*. Igual a `isattachment:true`.                           |
| isonline:      | IsOnline de informe: true      | Busca elementos que están en línea y que contienen *informes*.                                                         |
| isrecurring:   | IsRecurring de informe: true   | Busca elementos que son recurrentes y que contienen *informes*.                                                       |
| isflagged:     | isflagged de informe: true     | Busca elementos marcados (revisar, seguimiento, por ejemplo) y que contienen *Informe*.                       |
| IsDeleted     | Informe IsDeleted: true     | Busca elementos marcados como eliminados (papelera de reciclaje o elementos eliminados, por ejemplo) y que contienen *informes*. |
| IsCompleted   | Informe IsCompleted: false  | Busca elementos que no estén marcados como completos y que contengan el *Informe*.                                        |
| hasattachment | hasattachment de informe: true | Busca elementos que contienen *informes* y tienen datos adjuntos                                                          |
| hasflag:       | hasflag de informe: true       | Busca elementos que contengan el *Informe* y que tengan marcas.                                                                |



 

### <a name="dates"></a>Fechas

Además de buscar fechas y intervalos de fechas específicos mediante los operadores descritos anteriormente, AQS permite valores de fecha relativos (como `today` , `tomorrow` o `next week` ) y valores de día (como `Tuesday` o `Monday..Wednesday` ) y de mes ( `February` ).



| Con respecto a:    | Ejemplo de sintaxis                                                                                                                         | Resultado                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Día             | Fecha: hoy<br/> Fecha: mañana<br/> Fecha: ayer<br/>                                                               | Busca elementos con la fecha de hoy.<br/> Busca elementos con la fecha de mañana.<br/> Busca elementos con la fecha de ayer. <br/>                                                                                                                                                                                                                     |
| Semana/mes/año | Fecha: esta semana<br/> Fecha: última semana<br/> Fecha: mes siguiente<br/> Fecha: mes pasado<br/> Fecha: próximo año <br/> | Busca elementos con una fecha comprendida en la semana actual.<br/> Busca elementos con una fecha comprendida en la semana anterior.<br/> Busca elementos con una fecha comprendida en la semana próxima.<br/> Busca elementos con una fecha incluida en el mes anterior.<br/> Busca elementos con una fecha comprendida en el próximo año. <br/> |



 

## <a name="properties-by-file-kind"></a>Propiedades por tipo de archivo

Los usuarios pueden buscar propiedades específicas de diferentes tipos de archivos. Algunas propiedades (como el tamaño de archivo) son comunes a todos los archivos, mientras que otras están limitadas a un tipo específico. El número de diapositivas, por ejemplo, es específico de las presentaciones. En las tablas siguientes se enumeran estas propiedades por tipo de archivo.

### <a name="file-kind-everything"></a>Tipo de archivo: todo

Se trata de propiedades comunes a todos los tipos de archivo. Para incluir todos los tipos de archivos en una consulta, la sintaxis es:

`kind:everything <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad       | Use                      | Ejemplo                        |
|----------------|--------------------------|--------------------------------|
| Título          | título, asunto o acerca de  | Título: "trimestral financiera"    |
| Status         | status                   | Estado: completado                |
| Fecha           | fecha                     | Fecha: última semana                 |
| Fecha de modificación  | DateModified o modificado | modificado: última semana             |
| Importancia     | importancia o prioridad   | importancia: alta                |
| Tamaño           | tamaño                     | tamaño: > 50                   |
| Deleted        | eliminado o IsDeleted     | IsDeleted: true                 |
| Datos adjuntos  | isattachment             | isattachment: true              |
| En             | a o toname             | a: Bob                         |
| CC             | CC o ccname             | CC: Juan                        |
| Compañía        | company                  | empresa: Microsoft              |
| Location       | ubicación                 | Ubicación: "sala de conferencias 102" |
| Category       | category                 | Categoría: empresa              |
| Palabras clave       | keywords                 | Palabras clave: "proyecciones de ventas"   |
| Álbum          | álbum                    | álbum: "volar por la noche"           |
| Nombre de archivo      | nombre de archivo o archivo         | nombre de archivo: alnude              |
| Género          | genre                    | genre:rock                     |
| Autor         | autor o por             | Autor: "Stephen King"          |
| Personas         | personas o con           | con: (Sonja o David)          |
| Carpeta         | carpeta, en o ruta de acceso    | carpeta: descargas               |
| Extensión de archivo | EXT o fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Datos adjuntos

Se trata de propiedades comunes a los datos adjuntos. Para limitar la búsqueda solo a los datos adjuntos, la sintaxis es:

`kind:attachment <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad | Use            | Ejemplo                  |
|----------|----------------|--------------------------|
| Personas   | personas o con | personas: Juan o con: Juan |



 

### <a name="contacts"></a>Contactos

Se trata de propiedades comunes a los contactos. Para limitar la búsqueda solo a los contactos, la sintaxis es:

`kind:contacts <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad              | Use                 | Ejemplo                            |
|-----------------------|---------------------|------------------------------------|
| Puesto             | jobtitle            | jobtitle: CFO                       |
| Dirección de IM            | imdirección           | imdirección: John\_doe@msn.com        |
| Teléfono del ayudante     | assistantsphone     | assistantsphone: 555-3323           |
| Nombre del asistente        | assistantname       | assistantname: Paul                 |
| Profession            | Professional          | profesión: fontanero                 |
| Alias              | nickname            | alias: Tex                       |
| Pareja                | pareja              | cónyuge: Debbie                      |
| Ciudad de negocio         | businesscity        | businesscity: Seattle               |
| Código postal del trabajo  | businesspostalcode  | businesspostalcode: 98006           |
| Página principal de la empresa    | businesshomepage    | businesshomepage: www. Microsoft. com |
| Número de teléfono de devolución de llamada | callbackphonenumber | callbackphonenumber: 555-555-2121   |
| Teléfono del automóvil             | Carphone            | Carphone: 555-555-2121              |
| Children              | secundarios            | elementos secundarios: Timmy                     |
| Nombre            | firstname           | Nombre: Juan                     |
| Apellido             | lastname            | LastName: DOE                       |
| Fax particular              | homefax             | homefax: 555-555-2121               |
| Nombre del administrador        | managersname        | managersname: Juan                  |
| Buscapersonas                 | pager               | buscapersonas: 555-555-2121                 |
| Teléfono del trabajo        | businessphone       | businessphone: 555-555-2121         |
| Teléfono particular            | homePhone           | HomePhone: 555-555-2121             |
| Teléfono móvil          | mobilephone         | mobilephone: 555-555-2121           |
| Office                | Office              | Office: ejemplo                      |
| Aniversario           | aniversario         | aniversario: 1/1/06                 |
| Birthday              | nació            | cumpleaños: 1/1/06                    |
| Página web              | Web             | Página Web: www. Microsoft. com          |



 

> [!Note]
>
> Los números de teléfono se indexan según lo especificado. Por ejemplo, si un usuario no incluyó un código de país o área al escribir el número de teléfono, los usuarios no podrán encontrar un contacto si buscan el código de país o área en el número de teléfono.

 

### <a name="communications"></a>Comunicaciones

Se trata de propiedades comunes a las comunicaciones. Para limitar la búsqueda solo a las comunicaciones, la sintaxis es:

`kind:communications <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad       | Use                           | Ejemplo                         |
|----------------|-------------------------------|---------------------------------|
| From           | desde o organizador             | de: Juan                       |
| Received       | recibido o enviado              | Enviado: ayer                  |
| Asunto        | asunto o título              | asunto: "trimestral financiera"   |
| Tiene datos adjuntos | hasattachments, hasattachment | hasattachment: true              |
| Datos adjuntos    | datos adjuntos o datos adjuntos     | attachment:presentation.ppt     |
| CCO            | BCC, bccname o bccaddress    | CCO: Dave                        |
| Dirección de CC     | ccaddress o CC               | ccaddress: Juan\_doe@outlook.com |
| Marca de seguimiento | followupflag                  | followupflag: 2                  |
| Fecha de vencimiento       | DueDate o vencimiento                | vencimiento: última semana                   |
| Lectura           | lectura o isread                | es: lectura                         |
| Se completó   | IsCompleted                   | es: completado                    |
| Incompleto     | incompleto o isincomplete    | is: incompleto                   |
| Tiene marca       | hasflag o isflagged          | tiene: marca                        |
| Duration       | duration                      | duración: > 50                |



 

### <a name="calendar"></a>Calendario

Se trata de propiedades comunes a los calendarios. Para limitar la búsqueda solo a los calendarios, la sintaxis es:

`kind:calendar <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad  | Use                      | Ejemplo          |
|-----------|--------------------------|------------------|
| Periódica | periódico o IsRecurring | es: periódico     |
| Organizer | Organizador, por o desde    | Organizador: Debbie |



 

### <a name="documents"></a>Documentos

Se trata de propiedades comunes a los documentos. Para limitar la búsqueda solo a los documentos, la sintaxis es:

`kind:documents <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad          | Use             | Ejemplo                       |
|-------------------|-----------------|-------------------------------|
| Comentarios          | comments        | Comentarios: "necesita revisión final" |
| Guardado por última vez por     | lastsavedby     | lastsavedby: Juan              |
| Administrador de documentos  | documentmanager | DocumentManager: Juan          |
| Número de revisión   | RevisionNumber  | RevisionNumber: 1.0.3          |
| Formato de documento   | documentformat  | documentformat: MIMETYPE       |
| Fecha de la última impresión | datelastprinted | datelastprinted: última semana     |



 

### <a name="presentation"></a>Presentación

Se trata de propiedades comunes a las presentaciones. Para limitar la búsqueda solo a las presentaciones, la sintaxis es:

`kind:presentation <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad    | Use        | Ejemplo           |
|-------------|------------|-------------------|
| Recuento de diapositivas | slidecount | slidecount: >20 |



 

### <a name="music"></a>Música

Se trata de propiedades comunes a los archivos de música. Para limitar la búsqueda solo a la música, la sintaxis es:

`kind:music <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad | Use                | Ejemplo                  |
|----------|--------------------|--------------------------|
| Velocidad de bits | velocidad de bits, velocidad      | velocidad de bits: 192              |
| Artistas   | intérprete, por o desde | Intérprete: John cantante       |
| Duration | duration           | duración: 3               |
| Álbum    | álbum              | álbum: "mayores éxitos"    |
| Género    | genre              | genre:rock               |
| Track    | track              | pista: 12                 |
| Year     | year               | año: > 1980 < 1990 |



 

### <a name="picture"></a>Imagen

Se trata de propiedades comunes a las imágenes. Para limitar la búsqueda solo a las imágenes, la sintaxis es:

`kind:picture <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad     | Use         | Ejemplo               |
|--------------|-------------|-----------------------|
| Marca de cámara  | cameramake  | cameramake: ejemplo     |
| Modelo de cámara | cameramodel | cameramodel: ejemplo    |
| Dimensions   | dimensions  | Dimensiones: 8X10       |
| Orientación  | orientation | orientación: horizontal |
| Fecha de creación   | datetaken   | datetaken: ayer   |
| Ancho        | width       | ancho: 1600            |
| Alto       | height      | alto: 1200           |



 

### <a name="video"></a>Vídeo

Se trata de propiedades comunes a los vídeos. Para limitar la búsqueda solo a los vídeos, la sintaxis es:

`kind:video <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y `<value>` es el término de búsqueda especificado por el usuario.



| Propiedad | Use           | Ejemplo                                |
|----------|---------------|----------------------------------------|
| Nombre     | nombre, asunto | Nombre: "vacaciones de la familia para la playa 05" |
| Ext      | EXT, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Llamar a WDS desde la línea de comandos](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Llamar a WDS desde páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





