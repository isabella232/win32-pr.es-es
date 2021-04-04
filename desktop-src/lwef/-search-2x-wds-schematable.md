---
title: Esquema (características heredadas del entorno de Windows)
description: El esquema documenta los valores y las propiedades que utiliza el índice para almacenar los datos para la indización o la ordenación.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a122959b007ba4d4434e65b53fc2e330857cafe
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "104077423"
---
# <a name="schema"></a>Schema

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

El esquema documenta los valores y las propiedades que utiliza el índice para almacenar los datos para la indización o la ordenación. En la tabla de esquema se enumeran las columnas y sus propiedades (Type y PROPID) incluidas en el esquema para Microsoft Windows Desktop Search (WDS) 2.6.5.

## <a name="schema"></a>Schema



| Nombre de columna                  | Descripción                                                                                                             | PROPID                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Comentarios                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Crear                       | Fecha y hora en que se creó el archivo                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Carpeta descriptiva para el elemento                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autor del documento                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Palabras clave                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Prefijo del asunto (re:, FW:, etc.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Title                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Descripción descriptiva del tipo de archivo del registro (por ejemplo:. PSQ--> archivo de consulta de Product Studio)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nombre de la carpeta principal                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/NombreCarpeta                   |
| IsAttachment                 | Indica que el elemento es un dato adjunto                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | Indica que el elemento está marcado para su eliminación (papelera de reciclaje, elementos eliminados, etc.)                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | Fecha en que el usuario vio por última vez el elemento                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Personas                       | Personas implicadas en este elemento                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/People                       |
| PerceivedType                | PerceivedType del objeto Nota: solo para la recuperación.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nombre para mostrar de PerceivedType.Nunca se muestra o se consulta                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Fecha más interesante (hora de última escritura de los archivos, fecha de recepción del correo electrónico)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Tamaño                         | Tamaño de un archivo.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Asunto del archivo. Nota: Actualmente, los asuntos de correo electrónico se asignan a PrimaryTitle hoy y no se duplican debido a su longitud | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | URL basada en consultas                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Escritura                        | Fecha y hora de la última escritura en el archivo                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Fecha de vencimiento de un elemento                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Indica que el elemento no está totalmente disponible                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Indica que el elemento está marcado como completado                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Indica que el elemento está marcado                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Texto que se muestra para la marca; por ejemplo, revisar, seguimiento, etc.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identidad                     | Identidad para los usuarios de OE                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/identidad                     |
| IsRead                       | Indica que se ha leído el elemento                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| Importancia                   | Importancia o prioridad de MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/importancia                   |
| ContainerHash                | Código hash que identifica los datos adjuntos que se van a eliminar en función de una dirección URL de contenedor común.                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Formato de documento o MIMETYPE (por ejemplo ' Message/rfc822 ' para un archivo EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Hora en que el indexador rastreó por última vez el documento para actualizar el catálogo                                                           | 0b63e350-9ccc-11d0-bcdb-00805fccce04/4                            |
| Tienda                        | El controlador de almacenamiento o de protocolo (archivo, correo, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/almacén                        |
| FileExt                      | Extensión de archivo                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nombre del archivo.                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| nombreCorto                    | Nombre de archivo corto (8,3) para el archivo                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Nombres de los datos adjuntos de un mensaje                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Direcciones en el campo Cco:                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Nombres de persona en el campo Cco:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Direcciones en el campo CC:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Nombres de persona en el campo CC:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | IDENTIFICADOR único de una conversación en los subprocesos de correo electrónico                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | Direcciones en desde: campo                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nombre de la persona en el campo de:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indica que se ha respondido o reenviado el correo ( \_ acción cdoPR = 261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indica que mail tiene datos adjuntos (T o F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Hora de entrega                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/recepción                 |
| ToAddress                    | Direcciones en el campo para:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | Nombres de persona en el campo para:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | Estado de una tarea                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Hora de finalización (normalmente para reuniones y eventos)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indica que el elemento es periódico (por ejemplo, reuniones)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Hora de inicio (normalmente para reuniones y eventos)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Duración de la reunión en minutos                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/duración                     |
| Location                     | Ubicación donde se produce el elemento (como una reunión)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ubicación                     |
| Aniversario                  | Fecha de aniversario                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/aniversario                  |
| AssistantName                | Nombre del asistente                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Teléfono del ayudante                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | Cumpleaños del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/cumpleaños                     |
| BusinessAddressCity          | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressStreet        | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressStreet        |
| BusinessAddressCountry       | Información de dirección del trabajo                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Llamar a la información telefónica                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Nombres de los hijos para contactos                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Children                     |
| CompanyMainTelephone         | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nombre de correo electrónico de contacto                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nombre para mostrar de la dirección de correo electrónico                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| FirstName                    | Nombre del contacto                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nombre completo del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sexo                       | Hombre/hembra/otros                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/sexo                       |
| Afición                        | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/pasatiempo                        |
| HomeAddressCity              | Información de dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Información de dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Información de dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Información de dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Información de dirección principal                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressStreet            |
| HomeFaxNumber                | Información de facsímil                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Información de facsímil                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| Imdirección                    | Información de mensajes instantáneos                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/inaddress                    |
| JobTitle                     | Puesto del contacto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/alias                     |
| Office                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Profesión title (Dr., Mr, Mrs., Sra.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Información telefónica                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/profesión                   |
| Pareja                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/cónyuge                       |
| Sufijo                       | Información de contacto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/sufijo                       |
| TelexNumber                  | Información de télex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Información TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Página Web de contacto                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Página Web                      |
| DocCompany                   | Compañía                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Usuario en el que se guardó por última vez el documento wa                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Última impresión                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Diapositivas                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Velocidad media de datos en kbps para el archivo de audio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Longitud en milisegundos del archivo de audio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nombre del álbum                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nombre del artista                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Género del álbum                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Número de pistas en el álbum                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Año en el que se grabó el álbum                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Fabricante de la cámara                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modelo de cámara                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME de datos tomados                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientación                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensiones de la imagen                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Resolución X de la imagen                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Resolución Y para la imagen                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Alto de marco para el flujo de vídeo                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Velocidad de fotogramas en fotogramas por milisegundo para el flujo de vídeo                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Ancho de marco del flujo de vídeo                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Clase                        | Nombre de la clase                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/clase                        |
| Función                     | Nombre de función                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/FUNC                         |
| Estructura                       | Nombre de la estructura                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/struct                       |
| Interfaz                    | Nombre de interfaz                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/interfaz                    |
| Delegado                     | Nombre de delegado                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/delegado                     |
| Propiedad                     | Nombre de propiedad                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/propiedad                     |
| Enumeración                         | Nombre de enumeración                                                                                                               | 8dee0300-16c2-101B-B121-08002b2ecda9/enumeración                         |
| Const                        | Nombre const                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/const                        |
| Evento                        | Nombre del evento                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/evento                        |
| Campo                        | Nombre del campo                                                                                                              | 8dee0300-16c2-101B-B121-08002b2ecda9/campo                        |
| Definir                       | Definir nombre                                                                                                             | 8dee0300-16c2-101B-B121-08002b2ecda9/Def                          |
| Componente                    | Nombre de componente                                                                                                          | 8dee0300-16c2-101B-B121-08002b2ecda9/componente                    |
| proyecto                      | Nombre de proyecto                                                                                                            | 8dee0300-16c2-101B-B121-08002b2ecda9/proyecto                      |
| Solución                     | Nombre de la solución                                                                                                           | 8dee0300-16c2-101B-B121-08002b2ecda9/solución                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




