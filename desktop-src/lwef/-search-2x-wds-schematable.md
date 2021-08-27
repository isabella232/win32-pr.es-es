---
title: Esquema (características heredadas Windows entorno)
description: El esquema documenta los valores y las propiedades que usa el índice para almacenar datos para indexación u ordenación.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d5c80690914073af1c67e2bd00376974547d30c4dc487c0656d4452d3fe828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753154"
---
# <a name="schema"></a>Schema

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

El esquema documenta los valores y las propiedades que usa el índice para almacenar datos para indexación u ordenación. En la tabla Esquema se enumeran las columnas y sus propiedades (tipo y propid) incluidas en el esquema de Microsoft Windows Desktop Search (WDS) 2.6.5.

## <a name="schema"></a>Schema



| Nombre de columna                  | Descripción                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Comentarios                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Crear                       | Fecha y hora en que se creó el archivo                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Carpeta fácil de usar para el elemento                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autor del documento                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Palabras clave                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Prefijo del asunto (Re:, Fw:, etc.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Título                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Descripción fácil de usar del tipo de archivo del Registro (por ejemplo: .psq --> archivo de consulta de Product Studio)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nombre de la carpeta primaria                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| IsAttachment                 | Indica que el elemento es un archivo adjunto.                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | Indica que el elemento está marcado para su eliminación (papelera de reciclaje, elementos eliminados, etc.).                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | Fecha en que el usuario ha visto por última vez el elemento                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Personas                       | Personas implicadas en este elemento                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/People                       |
| PerceivedType                | PerceivedType del objeto NOTE: esto es solo para la recuperación.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nombre para mostrar de PerceivedType.  Nunca se muestra ni se consulta                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Fecha más interesante (hora de última escritura para archivos, fecha recibida por correo electrónico)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Size                         | Tamaño de un archivo.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Asunto del archivo. NOTA: Actualmente, los asuntos de correo electrónico se asignan a PrimaryTitle hoy y no se duplican debido a su longitud. | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | Dirección URL basada en consultas                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Escritura                        | Fecha y hora de la última escritura en el archivo                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Fecha de vencimiento de un elemento                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Indica que el elemento no está totalmente disponible                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Indica que el elemento está marcado como completado                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Indica que el elemento está marcado                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Texto que se muestra para la marca, por ejemplo, Revisión, Seguimiento, etc.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identidad                     | Identidad de los usuarios del sistema operativo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Identity                     |
| IsRead                       | Indica que se ha leído el elemento                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| Importancia                   | Importancia o prioridad de MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Importance                   |
| ContainerHash                | Código hash que identifica los datos adjuntos que se eliminarán en función de una dirección URL de contenedor común                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Formato de documento o MIMETYPE (por ejemplo, "message/rfc822" para un archivo EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Hora en que el indexador rastreó por última vez el documento para la actualización del catálogo.                                                           | 0b63e350-9ccc-11d0-bcdb-00805fccce04/4                            |
| Tienda                        | El controlador de almacén o protocolo (FILE, MAIL, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| FileExt                      | Extensión de archivo                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nombre del archivo.                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| nombreCorto                    | Nombre de archivo corto (8.3) para el archivo                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Nombres de datos adjuntos en un mensaje                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Direcciones en el campo Bcc:                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Nombres de persona en el campo Bcc:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Direcciones en el campo Cc:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Nombres de persona en el campo Cc:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | Identificador único de una conversación en subprocesos de correo electrónico                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | Direcciones en el campo Desde:                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nombre de persona en el campo From:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indica que el correo se reenvía a o se reenvía (cdoPR \_ ACTION=261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indica que el correo tiene datos adjuntos (T o F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Tiempo de entrega                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ReceivedDate                 |
| ToAddress                    | Direcciones en el campo Para:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | Nombres de persona en el campo Para:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | Estado de una tarea                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Hora de finalización (normalmente para reuniones o eventos)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indica que el elemento es periódico (por ejemplo, reuniones)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Hora de inicio (normalmente para reuniones o eventos)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Duración de la reunión en minutos                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Duration                     |
| Location                     | Ubicación donde se produce el elemento (como una reunión)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Location                     |
| Aniversario                  | Fecha de aniversario                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Anniversary                  |
| AssistantName                | Nombre del asistente                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Teléfono del asistente                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | Fecha de nacimiento del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Birthday                     |
| BusinessAddressCity          | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressAddressAddress        | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressAddressAddress        |
| BusinessAddressCountry       | Información de dirección de negocio                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Llamada a la información de teléfono                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Nombres de los hijos para el contacto                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Children                     |
| CompanyMainTelephone         | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nombre del correo electrónico de contacto                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nombre para mostrar de la dirección de correo electrónico                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| Nombre                    | Nombre del contacto                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nombre completo del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sexo                       | Varón/mujer/otro                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Gender                       |
| Hobby                        | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Qt                        |
| HomeAddressCity              | Información de la dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Información de la dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Información de la dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Información de la dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressAddressAddress            | Información de la dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressAddressAddress            |
| HomeFaxNumber                | Información de facsímil                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Información de facsímil                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| IMAddress                    | Información de mensaje instantáneo                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | Puesto del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AliasName                     |
| Office                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| Apellidos                     | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Título de la carrera (Dr., Mr., Mrs., Ms.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Información de teléfono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Secuescencia                   |
| Cónyuge                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Secuescencia                       |
| Sufijo                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Suffix                       |
| TelexNumber                  | Información de Telex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Información de TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Página web de contacto                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/WebPage                      |
| DocCompany                   | Compañía                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | User the doc wa last saved by                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Última impresión                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Diapositivas                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Velocidad media de datos en Kbps para el archivo de audio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Longitud en milisegundos del archivo de audio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nombre del álbum                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nombre del intérprete                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Género del álbum                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Número de pistas del álbum                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Año en el que se registró el álbum                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Fabricante de la cámara                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modelo de cámara                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME de los datos tomados                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientación                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensiones de la imagen                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Resolución X para la imagen                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Resolución Y para la imagen                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Alto del fotograma para la secuencia de vídeo                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Velocidad de fotogramas en fotogramas por milisegundo para la secuencia de vídeo                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Ancho del fotograma para la secuencia de vídeo                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Clase                        | Nombre de la clase                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/class                        |
| Función                     | Nombre de función                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/func                         |
| Estructura                       | Nombre de la estructura                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/struct                       |
| Interfaz                    | Nombre de interfaz                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/interface                    |
| Delegado                     | Nombre del delegado                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/delegate                     |
| Propiedad                     | Nombre de propiedad                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/property                     |
| Enumeración                         | Nombre de enumeración                                                                                                               | 8dee0300-16c2-101b-b121-08002b2ecda9/enum                         |
| Const                        | Nombre de const                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/const                        |
| Evento                        | Nombre del evento                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/event                        |
| Campo                        | Nombre del campo                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/field                        |
| Definir                       | Definición del nombre                                                                                                             | 8dee0300-16c2-101b-b121-08002b2ecda9/def                          |
| Componente                    | Nombre de componente                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/component                    |
| Proyecto                      | Nombre de proyecto                                                                                                            | 8dee0300-16c2-101b-b121-08002b2ecda9/project                      |
| Solución                     | Nombre de la solución                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/solution                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




