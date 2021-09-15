---
description: Registrar el controlador de la hoja de propiedades
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Registrar el controlador de la hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571200"
---
# <a name="registering-your-property-sheet-handler"></a>Registrar el controlador de la hoja de propiedades

Para que el espacio de nombres WPD reconozca el controlador de la hoja de propiedades, debe registrarlo correctamente en el registro Windows propiedades. Las entradas de registro de un controlador de hoja de propiedades de WPD son similares a las del shell, pero se registran como tipos de archivo especiales. Los controladores de hoja de propiedades de WPD se registran según el tipo de contenido que representan. A continuación se muestra un árbol de registro de ejemplo para un controlador de menú contextual de WPD:


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



En el ejemplo anterior se registra un controlador personalizado con el espacio de nombres WPD. Cuando un usuario hace clic con el botón derecho en un archivo de imagen de un dispositivo a través de Windows Shell y selecciona **Propiedades,** invoca este controlador de hoja de propiedades. El espacio de nombres WPD usa EL TIPO DE CONTENIDO DE WPD \_ para determinar qué controladores de hoja de propiedades se \_ cargarán. Si el tipo de contenido no proporciona una clasificación útil, el espacio de nombres cargará los controladores de hoja de propiedades en la clave del **Registro WPDPropSheet.Generic.** En la tabla siguiente se enumeran todas las clases de archivo disponibles para un controlador de menú contextual y qué tipos de contenido y extensiones de archivo representan.



| Clave del Registro                   | Tipo de contenido WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu.Device**      | El registro con esta clave habilita el controlador de menú contextual en el nivel de dispositivo. (Haga clic con el botón derecho en un dispositivo).                   |
| **WPDContextMenu. Storage**     | El registro con esta clave habilita el controlador de menú contextual en el nivel de almacenamiento. (Haga clic con el botón derecho en un almacenamiento).                 |
| **WPDContextMenu.Folder**      | CARPETA DE \_ TIPO DE \_ CONTENIDO \_ WPD                                                                                                     |
| **WPDContextMenu.Image**       | IMAGEN DE \_ TIPO DE \_ CONTENIDO \_ WPD                                                                                                      |
| **WPDContextMenu.Audio**       | AUDIO DE \_ TIPO DE \_ CONTENIDO WPD \_                                                                                                      |
| **WPDContextMenu.Video**       | VÍDEO DE \_ TIPO CONTENIDO \_ WPD \_                                                                                                      |
| **WPDContextMenu.Playlist**    | LISTA DE REPRODUCCIÓN \_ DE TIPO DE CONTENIDO \_ \_ WPD                                                                                                   |
| **WPDContextMenu.Document**    | DOCUMENTO DE \_ TIPO DE \_ CONTENIDO \_ WPD                                                                                                   |
| **WPDContextMenu.Contact**     | CONTACTO DE \_ TIPO DE \_ CONTENIDO WPD \_                                                                                                    |
| **WPDContextMenu.Email**       | CORREO ELECTRÓNICO DE \_ TIPO DE \_ CONTENIDO \_ WPD                                                                                                      |
| **WPDContextMenu.Appointment** | CITA DE \_ TIPO DE \_ CONTENIDO WPD \_                                                                                                |
| **WPDContextMenu.Task**        | TAREA TIPO \_ DE \_ CONTENIDO \_ WPD                                                                                                       |
| **WPDContextMenu.Memo**        | WPD \_ CONTENT \_ TYPE \_ MEMO                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM                                                                                               |
| **WPDContextMenu.AudioAlbum**  | WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM                                                                                               |
| **WPDContextMenu.VideoAlbum**  | WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM                                                                                               |
| **WPDContextMenu.MixedAlbum**  | WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM                                                                                      |
| **WPDContextMenu.Generic**     | TIPO DE \_ CONTENIDO WPD \_ SIN \_ ESPECIFICAR<br/> ARCHIVO GENÉRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD<br/> PROGRAMA DE \_ TIPO DE \_ CONTENIDO \_ WPD<br/> |



 

 

 




