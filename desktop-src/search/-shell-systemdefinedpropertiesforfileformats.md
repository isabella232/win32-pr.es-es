---
description: Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined propiedades de los formatos de archivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153946"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>System-Defined propiedades de los formatos de archivo personalizados

Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo. Si va a crear un formato de archivo personalizado, debe admitir tantas propiedades definidas por el sistema como pueda. Antes de crear un controlador de propiedades personalizado, debe revisar los controladores proporcionados por el sistema para ver si puede usar uno en lugar de escribir el suyo propio.

En la tabla siguiente se clasifican los formatos de archivo y, a continuación, se enumeran las propiedades del sistema más importantes que debe admitir el formato de archivo. Para proporcionar una experiencia de usuario adecuada, debe admitir todas las propiedades de prioridad 1 y 2 para su categoría de formato de archivo.

-   [Comunicaciones](#communications)
-   [Contactos](#contacts)
-   [Documentos](#documents)
-   [Genérico](#generic)
-   [Canción](#music)
-   [Imágenes](#pictures)
-   [Vídeos](#videos)
-   [Temas relacionados](#related-topics)

## <a name="communications"></a>Comunicaciones



| Nombre            | Propiedad                               | Prioridad |
|-----------------|----------------------------------------|----------|
| Fecha de recepción   | System. Message. DateReceived            | 1        |
| Desde nombres      | System. Message. FromName                | 1        |
| Tiene datos adjuntos | System. Message. HasAttachments          | 1        |
| Mailbox         | System. Communication. storeddisplayname | 1        |
| NOMBRE            | System. FileName                        | 1        |
| Asunto         | System. Subject                         | 1        |
| A nombres        | System. Message. ToName                  | 1        |
| Category        | System. Category                        | 2        |
| Tipo            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contactos



| Nombre             | Propiedad                           | Prioridad |
|------------------|------------------------------------|----------|
| Nombre de cuenta     | System. Communication. AccountName   | 1        |
| Teléfono del trabajo   | System. contact. BusinessTelephone   | 1        |
| Compañía          | System. Company                     | 1        |
| Dirección de correo electrónico    | System. contact. PrimaryEmailAddress | 1        |
| Importancia       | System. ImportanceText              | 1        |
| Teléfono móvil     | System. contact. MobileTelephone     | 1        |
| Dirección de la empresa | System. contact. BusinessAddress     | 2        |
| Fax del trabajo     | System. contact. BusinessFaxNumber   | 2        |
| Category         | System. Category                    | 2        |
| Dirección particular     | System. contact. HomeAddress         | 2        |
| Teléfono particular       | System. contact. HomeTelephone       | 2        |
| Título            | System.Title                       | 2        |



 

## <a name="documents"></a>Documentos



| Nombre      | Propiedad             | Prioridad |
|-----------|----------------------|----------|
| Authors   | System.Author        | 1        |
| Texto completo | System. FullText      | 1        |
| Etiquetas      | System.Keywords      | 1        |
| Tipo      | System.PerceivedType | 1        |
| Category  | System. Category      | 2        |
| Título     | System.Title         | 2        |



 

## <a name="generic"></a>Genérico



| Nombre     | Propiedad             | Prioridad |
|----------|----------------------|----------|
| Authors  | System.Author        | 1        |
| Title    | System.Title         | 1        |
| Tipo     | System.PerceivedType | 1        |
| Category | System. Category      | 2        |
| Etiquetas     | System.Keywords      | 2        |



 

## <a name="music"></a>Música



| Nombre         | Propiedad                     | Prioridad |
|--------------|------------------------------|----------|
| \#           | System. Music. TrackNumber     | 1        |
| Álbum        | System. Music. álbum      | 1        |
| Intérprete      | System. Music. artista          | 1        |
| Género        | System. Music. Genre           | 1        |
| Rating       | System. Rating                | 1        |
| Title        | System.Title                 | 1        |
| Intérprete del álbum | System. Music. AlbumArtist     | 2        |
| Velocidad de bits     | System. audio. EncodingBitrate | 2        |
| Conductores   | System. Music. conductores       | 2        |
| Length       | System. Media. Duration        | 2        |
| Protegido    | System. DRM. IsProtected       | 2        |
| Year         | System. Media. Year            | 2        |



 

## <a name="pictures"></a>Imágenes



| Nombre          | Propiedad                        | Prioridad |
|---------------|---------------------------------|----------|
| Fecha de importación | System. DateImported             | 1        |
| Fecha de creación    | System. Photo. DateTaken          | 1        |
| Rating        | System. Rating                   | 1        |
| Etiquetas          | System.Keywords                 | 1        |
| Tipo          | System.PerceivedType            | 1        |
| Authors       | System.Author                   | 2        |
| Creador de cámara  | System. Photo. CameraManufacturer | 2        |
| Modelo de cámara  | System. Photo. CameraModel        | 2        |
| Comentarios      | System. Comment                  | 2        |
| Dimensions    | System. Image. Dimensions         | 2        |



 

## <a name="videos"></a>Vídeos



| Nombre         | Propiedad                 | Prioridad |
|--------------|--------------------------|----------|
| Length       | System. Media. Duration    | 1        |
| Rating       | System. Rating            | 1        |
| Etiquetas         | System.Keywords          | 1        |
| Tipo         | System.PerceivedType     | 1        |
| Alto de marco | System. video. FrameHeight | 2        |
| Ancho de marco  | System. video. FrameWidth  | 2        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Sistema de propiedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
