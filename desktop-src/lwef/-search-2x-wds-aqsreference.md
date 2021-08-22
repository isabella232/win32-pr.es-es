---
title: Sintaxis de consulta avanzada
description: Microsoft Windows Desktop Search (WDS) usa la sintaxis de consulta avanzada (AQS) para ayudar a los usuarios y programadores a definir y restringir mejor sus búsquedas.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 2daf552f8f750335abacea4b550f92bd71c91c9b2b688a387b035a8180a8b3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601825"
---
# <a name="advanced-query-syntax"></a>Sintaxis de consulta avanzada

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Microsoft Windows Desktop Search (WDS) usa la sintaxis de consulta avanzada (AQS) para ayudar a los usuarios y programadores a definir y restringir mejor sus búsquedas. El uso de AQS es una manera sencilla de restringir las búsquedas y ofrecer mejores conjuntos de resultados. Las búsquedas se pueden restringir mediante los parámetros siguientes:

-   Tipos de archivo: carpetas, documentos, presentaciones, imágenes, entre otros.
-   Almacenes de archivos: bases de datos y ubicaciones específicas.
-   Propiedades del archivo: tamaño, fecha, título, entre otras.
-   Contenido del archivo: palabras clave como "project deliverables", "AQS", "blue suede shoes", y así sucesivamente.

Además, los parámetros de búsqueda se pueden combinar mediante operadores de búsqueda. En el resto de esta sección se explica la sintaxis de consulta, los parámetros y los operadores, y cómo se pueden combinar para ofrecer resultados de búsqueda de destino. Las tablas describen la sintaxis que se va a usar con WDS, así como las propiedades que se pueden consultar para cada tipo de archivo que se muestra en la ventana de resultados de Windows **Búsqueda** de escritorio.

## <a name="desktop-search-syntax"></a>Sintaxis de búsqueda de escritorio

Una consulta de búsqueda puede incluir una o varias palabras clave, con operadores booleanos y criterios opcionales. Estos criterios opcionales pueden restringir una búsqueda en función de lo siguiente:

-   Ámbito o almacén de datos en el que residen los archivos
-   Tipos de archivos
-   Propiedades administradas de archivos

Los criterios opcionales, que se describen con más detalle a continuación, usan la sintaxis siguiente:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Supongamos que un usuario quiere buscar un documento que contenga la frase "último trimestre", creada por John o John, y que el usuario guardó en la carpeta mydocuments. La consulta puede tener este aspecto:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Ámbito: ubicaciones y almacenes de datos

Los usuarios pueden limitar el ámbito de sus búsquedas a ubicaciones de carpetas o almacenes de datos específicos. Por ejemplo, si usa varias cuentas de correo electrónico y desea limitar una consulta a Microsoft Outlook o Microsoft Outlook Express, puede usar o `store:outlook` `store:oe` respectivamente.



| Restringir la búsqueda por almacén de datos | Use              | Ejemplo                                  |
|-------------------------------|------------------|------------------------------------------|
| Escritorio                       | escritorio          | store:desktop                            |
| Files                         | files            | store:files                              |
| Outlook                       | Outlook          | store:outlook                            |
| Outlook Express               | oe               | store:oe                                 |
| Carpeta específica               | foldername o in | foldername:MyDocuments o in:MyDocuments |



 

Si tiene un controlador de protocolo para rastrear almacenes personalizados, como Lotus Notes, puede usar el nombre del almacén o del controlador de protocolo para el almacén. Por ejemplo, si implementó un controlador de protocolo para incluir un almacén de datos de Lotus Notes como "notes", la sintaxis de consulta sería `store:notes` .

### <a name="common-file-kinds"></a>Tipos de archivo comunes

Los usuarios también pueden limitar sus búsquedas a tipos específicos de archivos, denominados tipos de archivo. En la tabla siguiente se enumeran los tipos de archivo y se ofrecen ejemplos de la sintaxis utilizada para buscar estos tipos de archivos.



| Para restringir por tipo de archivo:       | Use              | Ejemplo                        |
|---------------------------------|------------------|--------------------------------|
| Todos los tipos de archivo                  | Todo       | kind:everything                |
| Comunicaciones                  | comunicaciones   | kind:communications            |
| Contactos                        | contactos         | kind:contacts                  |
| Correo electrónico                          | email            | kind:email                     |
| Conversaciones de Instant Messenger | Im               | kind:im                        |
| Reuniones                        | Reuniones         | kind:meetings                  |
| Tareas                           | tareas            | kind:tasks                     |
| Notas                           | HDInsight            | kind:notes                     |
| Documentos                       | Documentación             | kind:docs                      |
| Documentos de texto                  | texto             | kind:text                      |
| Hojas de cálculo                    | Cálculo     | kind:spreadsheets              |
| Presentaciones                   | presentaciones    | kind:presentations             |
| Música                           | music            | kind:music                     |
| Imágenes                        | Fotos             | kind:pics                      |
| Vídeos                          | videos           | kind:videos                    |
| Carpetas                         | carpetas          | kind:folders                   |
| Nombre de la carpeta                     | foldername o in | foldername:mydocs o in:mydocs |
| Favoritos                       | favoritos        | kind:favorites                 |
| Programas                        | programas         | kind:programs                  |



 

### <a name="boolean-operators"></a>Operadores booleanos

Las palabras clave de búsqueda y las propiedades de archivo se pueden combinar para ampliar o restringir una búsqueda con operadores. En la tabla siguiente se explican los operadores comunes que se usan en una consulta de búsqueda.



| Palabra clave/símbolo  | Ejemplos                                              | Función                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | seguridad social NO<br/>                        | Busca elementos que contienen elementos *sociales,* pero no *de seguridad.*<br/>                                              |
|                 | seguridad social<br/>                           | Busca elementos que contienen elementos *sociales* *y de seguridad.*<br/>                                              |
| O BIEN              | seguridad social o<br/>                         | Busca elementos que contienen elementos *sociales* o *de seguridad.*<br/>                                                    |
| Comillas | "seguridad social"<br/>                          | Busca elementos que contienen la frase exacta de la *seguridad social.*<br/>                                        |
| Paréntesis     | (seguridad social)<br/>                          | Busca elementos que contienen *seguridad y sociales* en cualquier orden. <br/>                                      |
| >            | date:>11/05/04<br/> size:>500<br/>  | Busca elementos con una fecha posterior al 05/11/04. <br/> Busca elementos con un tamaño superior a 500 bytes.<br/> |
| <            | date:<11/05/04 <br/> size:<500<br/> | Busca elementos con una fecha anterior al 05/11/04. <br/> Busca elementos con un tamaño inferior a 500 bytes.<br/>   |
| ..              | date:11/05/04..11/10/04<br/>                    | Busca elementos con una fecha que comienza el 05/11/04 y termina el 10/11/04.<br/>                               |



 

> [!Note]
>
> Los operadores **NOT** y **OR** deben estar en mayúsculas y no se pueden combinar en una consulta (por ejemplo, `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Propiedades booleanas

Algunos tipos de archivo permiten a los usuarios buscar archivos mediante propiedades booleanas, como se describe en la tabla siguiente.



| Propiedad       | Ejemplo                   | Función                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| is:attachment  | report is:attachment      | Busca elementos que tienen datos adjuntos que contienen *el informe*. Igual a `isattachment:true`.                           |
| isonline:      | report isonline:true      | Busca elementos que están en línea y que contienen *el informe*.                                                         |
| es recurrente:   | report isrecurring:true   | Busca elementos que son periódicos y que contienen el *informe*.                                                       |
| isflagged:     | report isflagged:true     | Busca los elementos marcados (revisión, seguimiento, por ejemplo) y que contienen *el informe*.                       |
| isdeleted:     | report isdeleted:true     | Busca los elementos marcados como eliminados (papelera de reciclaje o Elementos eliminados, por ejemplo) y que contienen *el informe*. |
| iscompleted:   | report iscompleted:false  | Busca elementos que no están marcados como completos y que contienen *el informe*.                                        |
| hasattachment: | report hasattachment:true | Busca los elementos que contienen el *informe y* que tienen datos adjuntos.                                                          |
| hasflag:       | report hasflag:true       | Busca los elementos que contienen *el informe* y que tienen marcas.                                                                |



 

### <a name="dates"></a>Fechas

Además de buscar fechas e intervalos de fechas específicos mediante los operadores descritos anteriormente, AQS permite valores de fecha relativos (como , o ) y valores de día (como o ) y `today` `tomorrow` `next week` `Tuesday` `Monday..Wednesday` mes ( `February` ).



| En relación con:    | Ejemplo de sintaxis                                                                                                                         | Resultado                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Día             | date:today<br/> date:tomorrow<br/> date:yesterday<br/>                                                               | Busca elementos con la fecha de hoy.<br/> Busca elementos con la fecha de mañana.<br/> Busca elementos con la fecha de ayer. <br/>                                                                                                                                                                                                                     |
| Semana/mes/año | date:this week<br/> date:last week<br/> date:next month<br/> date:past month<br/> date:coming year <br/> | Busca elementos con una fecha que se encuentra dentro de la semana actual.<br/> Busca elementos con una fecha que se encuentra dentro de la semana anterior.<br/> Busca elementos con una fecha que se encuentra dentro de la próxima semana.<br/> Busca elementos con una fecha que se encuentra dentro del mes anterior.<br/> Busca elementos con una fecha que se encuentra dentro del próximo año. <br/> |



 

## <a name="properties-by-file-kind"></a>Propiedades por tipo de archivo

Los usuarios pueden buscar propiedades específicas de diferentes tipos de archivo. Algunas propiedades (como el tamaño del archivo) son comunes a todos los archivos, mientras que otras se limitan a un tipo específico. El recuento de diapositivas, por ejemplo, es específico de las presentaciones. En las tablas siguientes se muestran estas propiedades por tipo de archivo.

### <a name="file-kind-everything"></a>Tipo de archivo: Todo

Estas son propiedades comunes a todos los tipos de archivo. Para incluir todos los tipos de archivos en una consulta, la sintaxis es:

`kind:everything <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad       | Use                      | Ejemplo                        |
|----------------|--------------------------|--------------------------------|
| Título          | title, subject o about  | title:"Quarterly Financial"    |
| Status         | status                   | status:complete                |
| Fecha           | fecha                     | date:last week                 |
| Fecha de modificación  | datemodified o modified | modified:last week             |
| Importancia     | importancia o prioridad   | importance:high                |
| Size           | tamaño                     | size:> 50                   |
| Deleted        | deleted o isdeleted     | isdeleted:true                 |
| ¿Son datos adjuntos?  | isattachment             | isattachment:true              |
| En             | to o toname             | to:bob                         |
| CC             | cc o ccname             | cc:john                        |
| Compañía        | company                  | company:Microsoft              |
| Ubicación       | ubicación                 | location:"Conference Room 102" |
| Category       | category                 | category:Business              |
| Palabras clave       | keywords                 | keywords:"sales projections"   |
| Álbum          | Álbum                    | album:"Fly by Night"           |
| Nombre de archivo      | nombre de archivo o archivo         | filename:MyResume              |
| Género          | genre                    | genre:rock                     |
| Autor         | author o by             | author:"Stephen King"          |
| Personas         | personas o con           | with:(sonja o david)          |
| Carpeta         | carpeta, en o ruta de acceso    | folder:downloads               |
| Extensión de archivo | ext o fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Datos adjuntos

Estas son propiedades comunes a los datos adjuntos. Para limitar la búsqueda solo a datos adjuntos, la sintaxis es:

`kind:attachment <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad | Use            | Ejemplo                  |
|----------|----------------|--------------------------|
| Personas   | personas o con | people:john o with:john |



 

### <a name="contacts"></a>Contactos

Estas son propiedades comunes a los contactos. Para limitar la búsqueda solo a contactos, la sintaxis es:

`kind:contacts <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad              | Use                 | Ejemplo                            |
|-----------------------|---------------------|------------------------------------|
| Puesto             | jobtitle            | jobtitle:CFO                       |
| Dirección de mensajería instantánea            | imaddress           | imaddress:john\_doe@msn.com        |
| Teléfono del asistente     | assistantsphone     | assistantsphone:555-3323           |
| Nombre del asistente        | assistantname       | assistantname:Paul                 |
| Profession            | Profesión          | y, por tanto,                 |
| Alias              | nickname            | alias:Texas                       |
| Cónyuge                | Cónyuge              | lugar de la vida:                      |
| Ciudad empresarial         | businesscity        | businesscity:Seattle               |
| Código postal del negocio  | businesspostalcode  | businesspostalcode:98006           |
| Página principal de la empresa    | businesshomepage    | businesshomepage:www.microsoft.com |
| Número de teléfono de devolución de llamada | callbackphonenumber | callbackphonenumber:555-555-2121   |
| Teléfono del automóvil             | Carphone            | carphone:555-555-2121              |
| Children              | secundarios            | children:Timmy                     |
| Nombre            | firstname           | firstname:John                     |
| Apellido             | lastname            | lastname:Doe                       |
| Fax principal              | homefax             | homefax:555-555-2121               |
| Nombre del administrador        | managersname        | managersname:John                  |
| Buscapersonas                 | pager               | pager:555-555-2121                 |
| Teléfono del trabajo        | businessphone       | businessphone:555-555-2121         |
| Teléfono particular            | homePhone           | homephone:555-555-2121             |
| Teléfono móvil          | Móvil         | mobilephone:555-555-2121           |
| Office                | Office              | office:sample                      |
| Aniversario           | Aniversario         | anniversary:1/1/06                 |
| Birthday              | Cumpleaños            | lugar:1/1/06                    |
| Página web              | Página web             | webpage:www.microsoft.com          |



 

> [!Note]
>
> Teléfono los números se indexa según lo especificado. Por ejemplo, si un usuario no in include a country or area code when entering the phone number, users will not be able to locate a contact if searching with country or area code in the phone number.

 

### <a name="communications"></a>Comunicaciones

Estas son propiedades comunes a las comunicaciones. Para limitar la búsqueda solo a las comunicaciones, la sintaxis es:

`kind:communications <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad       | Use                           | Ejemplo                         |
|----------------|-------------------------------|---------------------------------|
| From           | desde o organizador             | from:john                       |
| Received       | recibido o enviado              | sent:yesterday                  |
| Asunto        | asunto o título              | subject:"Quarterly Financial"   |
| Tiene datos adjuntos | hasattachments, hasattachment | hasattachment:true              |
| Datos adjuntos    | datos adjuntos o datos adjuntos     | attachment:presentation.ppt     |
| CCO            | bcc, bccname o bccaddress    | bcc:dave                        |
| Dirección CC     | ccaddress o cc               | ccaddress:john\_doe@outlook.com |
| Marca de seguimiento | followupflag                  | followupflag:2                  |
| Fecha de vencimiento       | duedate o due                | due:last week                   |
| Lectura           | read o isread                | is:read                         |
| Se ha completado   | iscompleted                   | is:completed                    |
| Incompleto     | incomplete o isincomplete    | is:incomplete                   |
| Tiene marca       | hasflag o isflagged          | has:flag                        |
| Duration       | duration                      | duration:> 50                |



 

### <a name="calendar"></a>Calendario

Estas son propiedades comunes a los calendarios. Para limitar la búsqueda solo a calendarios, la sintaxis es:

`kind:calendar <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad  | Use                      | Ejemplo          |
|-----------|--------------------------|------------------|
| Periódica | recurrentes o recurrentes | is:recurring     |
| Organizer | organizador, por o desde    | organizer:dc |



 

### <a name="documents"></a>Documentos

Estas son propiedades comunes a los documentos. Para limitar la búsqueda solo a documentos, la sintaxis es:

`kind:documents <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad          | Use             | Ejemplo                       |
|-------------------|-----------------|-------------------------------|
| Comentarios          | comments        | comments:"needs final review" |
| Último guardado por     | lastsavedby     | lastsavedby:john              |
| Administrador de documentos  | documentmanager | documentmanager:john          |
| Número de revisión   | revisionnumber  | revisionnumber:1.0.3          |
| Formato de documento   | documentformat  | documentformat:MIMETYPE       |
| Fecha de la última impresión | datelastprinted | datelastprinted:last week     |



 

### <a name="presentation"></a>Presentación

Estas son propiedades comunes a las presentaciones. Para limitar la búsqueda solo a presentaciones, la sintaxis es:

`kind:presentation <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad    | Use        | Ejemplo           |
|-------------|------------|-------------------|
| Recuento de diapositivas | recuento de diapositivas | slidecount:>20 |



 

### <a name="music"></a>Música

Estas son propiedades comunes a los archivos de música. Para limitar la búsqueda solo a música, la sintaxis es:

`kind:music <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad | Use                | Ejemplo                  |
|----------|--------------------|--------------------------|
| Velocidad de bits | velocidad de bits, velocidad      | velocidad de bits:192              |
| Artista   | artist, by o from | artist:John Artist       |
| Duration | duration           | duration:3               |
| Álbum    | Álbum              | album:"greatest hits"    |
| Género    | genre              | genre:rock               |
| Track    | track              | track:12                 |
| Year     | year               | year:> 1980 < 1990 |



 

### <a name="picture"></a>Imagen

Estas son propiedades comunes a las imágenes. Para limitar la búsqueda solo a imágenes, la sintaxis es:

`kind:picture <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad     | Use         | Ejemplo               |
|--------------|-------------|-----------------------|
| Make de la cámara  | cameramake  | cameramake:sample     |
| Modelo de cámara | cameramodel | cameramodel:sample    |
| Dimensions   | dimensions  | dimensions:8X10       |
| Orientación  | orientation | orientation:landscape |
| Fecha de toma   | datetaken   | datetaken:yesterday   |
| Ancho        | width       | width:1600            |
| Alto       | height      | height:1200           |



 

### <a name="video"></a>Vídeo

Estas son propiedades comunes a los vídeos. Para limitar la búsqueda solo a vídeos, la sintaxis es:

`kind:video <property>:<value>`

donde `<property>` es una propiedad que se muestra a continuación y es el término de búsqueda especificado por el `<value>` usuario.



| Propiedad | Use           | Ejemplo                                |
|----------|---------------|----------------------------------------|
| Nombre     | name, subject | name:"Family Vacation to the Beach 05" |
| Ext      | ext, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Llamada a WDS desde la línea de comandos](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Llamada a WDS desde Páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





