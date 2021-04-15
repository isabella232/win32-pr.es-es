---
description: Registrar el controlador del menú contextual
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Registrar el controlador del menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafd2798683b4bc291653bca34996f143fc36842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648493"
---
# <a name="registering-your-context-menu-handler"></a>Registrar el controlador del menú contextual

Para que el espacio de nombres de WPD reconozca el controlador del menú contextual, debe registrarlo correctamente en el registro de Windows. Las entradas de registro de un controlador del menú contextual de WPD son similares a las del shell, pero se registran como tipos de archivo especiales. Los controladores de menú contextual de WPD se registran según el tipo de contenido que representan. A continuación se muestra un árbol de registro de ejemplo para un controlador del menú contextual de WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



En el ejemplo anterior se registra el visor de imágenes de Shell con el espacio de nombres WPD. Cuando un usuario hace clic con el botón secundario o hace doble clic en el contenido de un dispositivo a través del shell de Windows Vista, invoca este controlador de menú contextual. El espacio de nombres de WPD usa el \_ \_ tipo de contenido WPD para determinar qué controladores de menús contextuales se van a cargar. Si \_ \_ el tipo de contenido de WPD es igual al tipo de contenido de WPD sin \_ \_ \_ especificar, \_ \_ \_ \_ archivo genérico de tipo de contenido de WPD o \_ \_ \_ programa de tipo de contenido WPD, el espacio de nombres de WPD intentará encontrar la mejor coincidencia en función de la extensión del archivo seleccionado. Si ni la extensión de archivo ni el tipo de contenido proporcionan una clasificación útil, el espacio de nombres de WPD cargará los controladores de menú contextual en la clave del registro **WPDContextMenu. Generic** . En la tabla siguiente se enumeran todas las clases de archivo disponibles para un controlador de menú contextual y qué tipos de contenido y extensiones de archivo representan:



| Clave del Registro                           | Tipo de contenido de WPD                                                                                               | Extensión de archivo                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. dispositivo**              | Al registrarse en esta clave, se habilita el controlador de menú contextual en el nivel de dispositivo. (Haga clic con el botón derecho en un dispositivo).   | (No disponible)                                                                                                    |
| **WPDContextMenu. Storage**             | Al registrarse en esta clave, se habilita el controlador de menú contextual en el nivel de almacenamiento. (Haga clic con el botón derecho en un almacenamiento). | (No disponible)                                                                                                    |
| **WPDContextMenu. carpeta**              | \_carpeta de \_ tipo de contenido de WPD \_                                                                                     | (No disponible)                                                                                                    |
| **WPDContextMenu. Image**               | \_imagen de \_ tipo de contenido de WPD \_                                                                                      | .bmp <br/> .gif <br/> .png <br/> .jpg <br/> .jpe <br/> .jpeg <br/>   |
| **WPDContextMenu. audio**               | tipo de contenido de WPD ( \_ \_ \_ audio)                                                                                      | .aiff <br/> .mp3 <br/> .wav <br/> .wma <br/>                                     |
| **WPDContextMenu. vídeo**               | vídeo sobre el tipo de contenido de WPD \_ \_ \_                                                                                      | .asf<br/> .avi <br/> . DVR-MS <br/> . MPEG <br/> .mpg <br/> .wmv <br/> |
| **WPDContextMenu. Playlist**<br/> | \_lista de \_ reproducción de tipo de contenido de WPD \_                                                                                   | . wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> . esperen <br/>                     |
| **WPDContextMenu.Document**            | \_documento de \_ tipo de contenido de WPD \_                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDContextMenu. contact**<br/>  | \_contacto del \_ tipo de contenido de WPD \_                                                                                    | None                                                                                                     |
| **WPDContextMenu.Email**               | \_ \_ correo electrónico de tipo de contenido de WPD \_                                                                                      | None                                                                                                     |
| **WPDContextMenu. appointment**         | \_cita de \_ tipo de contenido de WPD \_                                                                                | None                                                                                                     |
| **WPDContextMenu. Task**                | tipo de contenido de WPD, \_ \_ \_ tarea                                                                                       | None                                                                                                     |
| **WPDContextMenu. Memo**                | tipo de contenido de WPD, \_ \_ \_ memorando                                                                                       | None                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | \_álbum de \_ imagen del tipo de contenido de WPD \_ \_                                                                               | None                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | tipo de contenido de WPD \_ \_ \_ álbum de audio \_                                                                               | None                                                                                                     |
| **WPDContextMenu. videoalbum**          | tipo de contenido de WPD \_ \_ \_ álbum de vídeo \_                                                                               | None                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | \_álbum de \_ \_ contenido mixto \_ de tipo de contenido de \_ WPD                                                                      | None                                                                                                     |
| **WPDContextMenu. Generic**             | tipo de contenido de WPD no \_ \_ \_ especificado                                                                                | Todas las demás extensiones de archivo                                                                                |



 

 

 




