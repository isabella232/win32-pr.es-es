---
description: Registrar el controlador de la hoja de propiedades
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrar el controlador de la hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716391"
---
# <a name="registering-your-property-sheet-handler"></a>Registrar el controlador de la hoja de propiedades

Para que el espacio de nombres WPD reconozca el controlador de la hoja de propiedades, debe registrarlo correctamente en el registro de Windows. Las entradas de registro para un controlador de la hoja de propiedades de WPD son similares a las del shell, pero se registran como tipos de archivo especiales. Los controladores de la hoja de propiedades de WPD se registran según el tipo de contenido que representan. A continuación se muestra un árbol de registro de ejemplo para un controlador del menú contextual de WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



En el ejemplo anterior se registra un controlador personalizado con el espacio de nombres WPD. Cuando un usuario hace clic con el botón secundario en un archivo de imagen en un dispositivo a través del shell de Windows y selecciona **propiedades**, invoca este controlador de la hoja de propiedades. El espacio de nombres de WPD usa el \_ tipo de contenido WPD \_ para determinar qué controladores de hoja de propiedades se van a cargar. Si el tipo de contenido no proporciona una clasificación útil, el espacio de nombres cargará los controladores de hoja de propiedades en la clave **del registro WPDPropSheet. Generic** . En la tabla siguiente se enumeran todas las clases de archivo disponibles para un controlador de menú contextual y los tipos de contenido y las extensiones de archivo que representan.



| Clave del Registro                   | Tipo de contenido de WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. dispositivo**      | Al registrarse en esta clave, se habilita el controlador de menú contextual en el nivel de dispositivo. (Haga clic con el botón derecho en un dispositivo).                   |
| **WPDContextMenu. Storage**     | Al registrarse en esta clave, se habilita el controlador de menú contextual en el nivel de almacenamiento. (Haga clic con el botón derecho en un almacenamiento).                 |
| **WPDContextMenu. carpeta**      | \_carpeta de \_ tipo de contenido de WPD \_                                                                                                     |
| **WPDContextMenu. Image**       | \_imagen de \_ tipo de contenido de WPD \_                                                                                                      |
| **WPDContextMenu. audio**       | tipo de contenido de WPD ( \_ \_ \_ audio)                                                                                                      |
| **WPDContextMenu. vídeo**       | vídeo sobre el tipo de contenido de WPD \_ \_ \_                                                                                                      |
| **WPDContextMenu. Playlist**    | \_lista de \_ reproducción de tipo de contenido de WPD \_                                                                                                   |
| **WPDContextMenu.Document**    | \_documento de \_ tipo de contenido de WPD \_                                                                                                   |
| **WPDContextMenu. contact**     | \_contacto del \_ tipo de contenido de WPD \_                                                                                                    |
| **WPDContextMenu.Email**       | \_ \_ correo electrónico de tipo de contenido de WPD \_                                                                                                      |
| **WPDContextMenu. appointment** | \_cita de \_ tipo de contenido de WPD \_                                                                                                |
| **WPDContextMenu. Task**        | tipo de contenido de WPD, \_ \_ \_ tarea                                                                                                       |
| **WPDContextMenu. Memo**        | tipo de contenido de WPD, \_ \_ \_ memorando                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | \_álbum de \_ imagen del tipo de contenido de WPD \_ \_                                                                                               |
| **WPDContextMenu.AudioAlbum**  | tipo de contenido de WPD \_ \_ \_ álbum de audio \_                                                                                               |
| **WPDContextMenu. videoalbum**  | tipo de contenido de WPD \_ \_ \_ álbum de vídeo \_                                                                                               |
| **WPDContextMenu.MixedAlbum**  | \_álbum de \_ \_ contenido mixto \_ de tipo de contenido de \_ WPD                                                                                      |
| **WPDContextMenu. Generic**     | tipo de contenido de WPD no \_ \_ \_ especificado<br/> \_ \_ archivo genérico de tipo de contenido de \_ WPD \_<br/> \_programa de \_ tipo de contenido de WPD \_<br/> |



 

 

 




