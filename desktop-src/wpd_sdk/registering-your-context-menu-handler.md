---
description: Registrar el controlador de menú contextual
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrar el controlador de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027e01d4b3bc58727579b77345d3f1b8eed668e5b858e49eb4859a40db9ad2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083549"
---
# <a name="registering-your-context-menu-handler"></a>Registrar el controlador de menú contextual

Para que el espacio de nombres WPD reconozca el controlador de menú contextual, debe registrarlo correctamente en el registro Windows contexto. Las entradas de registro de un controlador de menú contextual de WPD son similares a las del shell, pero se registran como tipos de archivo especiales. Los controladores de menú contextual de WPD se registran según el tipo de contenido que representan. A continuación se muestra un árbol de registro de ejemplo para un controlador de menú contextual DE WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



En el ejemplo anterior se registra el visor de imágenes de shell con el espacio de nombres WPD. Cuando un usuario hace clic con el botón derecho o hace doble clic en el contenido de un dispositivo a través de Windows Shell de Vista, invoca este controlador de menú contextual. El espacio de nombres WPD usa WPD \_ CONTENT TYPE para determinar qué controladores de menú contextual se \_ cargarán. Si WPD CONTENT TYPE es igual a \_ \_ WPD \_ CONTENT TYPE \_ \_ UNSPECIFIED, WPD CONTENT TYPE GENERIC FILE o \_ \_ \_ \_ WPD CONTENT TYPE PROGRAM, \_ \_ \_ el espacio de nombres WPD intentará encontrar la mejor coincidencia en función de la extensión del archivo seleccionado. Si ni la extensión de archivo ni el tipo de contenido proporcionan una clasificación útil, el espacio de nombres WPD cargará los controladores de menú contextual en la clave del Registro **WPDContextMenu.Generic.** En la tabla siguiente se enumeran todas las clases de archivo disponibles para un controlador de menú contextual y qué tipos de contenido y extensiones de archivo representan:



| Clave del Registro                           | Tipo de contenido DE WPD                                                                                               | Extensión de archivo                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**              | El registro con esta clave habilita el controlador de menú contextual en el nivel de dispositivo. (Haga clic con el botón derecho en un dispositivo).   | (No disponible)                                                                                                    |
| **WPDContextMenu. Storage**             | El registro con esta clave habilita el controlador de menú contextual en el nivel de almacenamiento. (Haga clic con el botón derecho en un almacenamiento). | (No disponible)                                                                                                    |
| **WPDContextMenu.Folder**              | CARPETA DE TIPO \_ DE \_ CONTENIDO DE \_ WPD                                                                                     | (No disponible)                                                                                                    |
| **WPDContextMenu.Image**               | IMAGEN DE TIPO \_ DE \_ CONTENIDO \_ WPD                                                                                      | .bmp <br/> .gif <br/> .png <br/> .jpg <br/> .jpe <br/> .jpeg <br/>   |
| **WPDContextMenu.Audio**               | AUDIO DE \_ TIPO \_ DE CONTENIDO WPD \_                                                                                      | .aiff <br/> .mp3 <br/> .wav <br/> .wma <br/>                                     |
| **WPDContextMenu.Video**               | VÍDEO DE \_ TIPO \_ DE CONTENIDO \_ WPD                                                                                      | .asf<br/> .avi <br/> .dvr-ms <br/> .mpeg <br/> .mpg <br/> .wmv <br/> |
| **WPDContextMenu.Playlist**<br/> | LISTA DE REPRODUCCIÓN \_ DE TIPO DE CONTENIDO \_ WPD \_                                                                                   | .wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> .pls <br/>                     |
| **WPDContextMenu.Document**            | DOCUMENTO DE \_ TIPO DE CONTENIDO DE \_ \_ WPD                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDContextMenu.Contact**<br/>  | CONTACTO DE TIPO \_ \_ DE CONTENIDO WPD \_                                                                                    | Ninguno                                                                                                     |
| **WPDContextMenu.Email**               | CORREO ELECTRÓNICO DE \_ TIPO DE CONTENIDO DE \_ \_ WPD                                                                                      | Ninguno                                                                                                     |
| **WPDContextMenu.Appointment**         | CITA DE TIPO \_ DE \_ CONTENIDO WPD \_                                                                                | Ninguno                                                                                                     |
| **WPDContextMenu.Task**                | TAREA TIPO \_ DE \_ CONTENIDO \_ WPD                                                                                       | Ninguno                                                                                                     |
| **WPDContextMenu.Memo**                | WPD \_ CONTENT \_ TYPE \_ MEMO                                                                                       | Ninguno                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                               | Ninguno                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM                                                                               | Ninguno                                                                                                     |
| **WPDContextMenu.VideoAlbum**          | WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM                                                                               | Ninguno                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM                                                                      | Ninguno                                                                                                     |
| **WPDContextMenu.Generic**             | TIPO DE \_ CONTENIDO \_ WPD \_ SIN ESPECIFICAR                                                                                | Todas las demás extensiones de archivo                                                                                |



 

 

 




