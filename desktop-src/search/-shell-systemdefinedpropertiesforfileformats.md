---
description: Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined propiedades para formatos de archivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28dcf137d10fffb3cc192acf66b1279b83fd079b6b81cf963dfed8a78408388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944505"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>System-Defined propiedades para formatos de archivo personalizados

Microsoft Windows proporciona varias propiedades del sistema que puede usar para los formatos de archivo. Si va a crear un formato de archivo personalizado, debe admitir tantas propiedades definidas por el sistema como sea posible. Antes de crear un controlador de propiedades personalizado, debe revisar los controladores proporcionados por el sistema para ver si puede usar uno en lugar de escribir el suyo propio.

En la tabla siguiente se clasifican los formatos de archivo y, a continuación, se enumeran las propiedades del sistema más importantes que debe admitir el formato de archivo. Para proporcionar una buena experiencia de usuario, debe admitir todas las propiedades de prioridad 1 y 2 para su categoría de formato de archivo.

-   [Comunicaciones](#communications)
-   [Contactos](#contacts)
-   [Documentos](#documents)
-   [Genérico](#generic)
-   [Música](#music)
-   [Imágenes](#pictures)
-   [Vídeos](#videos)
-   [Temas relacionados](#related-topics)

## <a name="communications"></a>Comunicaciones



| Nombre            | Propiedad                               | Prioridad |
|-----------------|----------------------------------------|----------|
| Fecha de recibido   | System.Message.DateReceived            | 1        |
| Desde nombres      | System.Message.FromName                | 1        |
| Tiene datos adjuntos | System.Message.HasAttachments          | 1        |
| Mailbox         | System.Communication.storeddisplayname | 1        |
| NOMBRE            | System.FileName                        | 1        |
| Asunto         | System.Subject                         | 1        |
| Para nombres        | System.Message.ToName                  | 1        |
| Category        | System.Category                        | 2        |
| Tipo            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contactos



| Nombre             | Propiedad                           | Prioridad |
|------------------|------------------------------------|----------|
| Nombre de cuenta     | System.Communication.AccountName   | 1        |
| Teléfono del trabajo   | System.Contact.BusinessTelephone   | 1        |
| Compañía          | System.Company                     | 1        |
| Dirección de correo electrónico    | System.Contact.PrimaryEmailAddress | 1        |
| Importancia       | System.ImportanceText              | 1        |
| Teléfono móvil     | System.Contact.MobileTelephone     | 1        |
| Dirección de negocio | System.Contact.BusinessAddress     | 2        |
| Fax empresarial     | System.Contact.BusinessFaxNumber   | 2        |
| Category         | System.Category                    | 2        |
| Dirección principal     | System.Contact.HomeAddress         | 2        |
| Teléfono particular       | System.Contact.HomeTelephone       | 2        |
| Título            | System.Title                       | 2        |



 

## <a name="documents"></a>Documentos



| Nombre      | Propiedad             | Prioridad |
|-----------|----------------------|----------|
| Authors   | System.Author        | 1        |
| Texto completo | System.FullText      | 1        |
| Etiquetas      | System.Keywords      | 1        |
| Tipo      | System.PerceivedType | 1        |
| Category  | System.Category      | 2        |
| Título     | System.Title         | 2        |



 

## <a name="generic"></a>Genérico



| Nombre     | Propiedad             | Prioridad |
|----------|----------------------|----------|
| Authors  | System.Author        | 1        |
| Título    | System.Title         | 1        |
| Tipo     | System.PerceivedType | 1        |
| Category | System.Category      | 2        |
| Etiquetas     | System.Keywords      | 2        |



 

## <a name="music"></a>Música



| Nombre         | Propiedad                     | Prioridad |
|--------------|------------------------------|----------|
| \#           | Sistema. Música. TrackNumber     | 1        |
| Álbum        | Sistema. Música. AlbumTitle      | 1        |
| Artistas      | Sistema. Música. Artista          | 1        |
| Género        | Sistema. Música. Género           | 1        |
| Rating       | System.Rating                | 1        |
| Título        | System.Title                 | 1        |
| Album Artist | Sistema. Música. AlbumArtist     | 2        |
| Velocidad de bits     | System.Audio.EncodingBitrate | 2        |
| Conductores   | Sistema. Música. Director       | 2        |
| Length       | System.Media.Duration        | 2        |
| Protegido    | System.DRM.IsProtected       | 2        |
| Year         | System.Media.Year            | 2        |



 

## <a name="pictures"></a>Imágenes



| Nombre          | Propiedad                        | Prioridad |
|---------------|---------------------------------|----------|
| Fecha de importación | System.DateImported             | 1        |
| Fecha de toma    | System.Photo.DateTaken          | 1        |
| Rating        | System.Rating                   | 1        |
| Etiquetas          | System.Keywords                 | 1        |
| Tipo          | System.PerceivedType            | 1        |
| Authors       | System.Author                   | 2        |
| Creador de cámaras  | System.Photo.CameraManufacturer | 2        |
| Modelo de cámara  | System.Photo.CameraModel        | 2        |
| Comentarios      | System.Comment                  | 2        |
| Dimensions    | System.Image.Dimensions         | 2        |



 

## <a name="videos"></a>Vídeos



| Nombre         | Propiedad                 | Prioridad |
|--------------|--------------------------|----------|
| Length       | System.Media.Duration    | 1        |
| Rating       | System.Rating            | 1        |
| Etiquetas         | System.Keywords          | 1        |
| Tipo         | System.PerceivedType     | 1        |
| Alto del marco | System.Video.FrameHeight | 2        |
| Ancho del marco  | System.Video.FrameWidth  | 2        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Sistema de propiedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
