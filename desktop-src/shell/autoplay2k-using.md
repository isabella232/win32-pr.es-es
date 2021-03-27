---
description: Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión activa, se determina el contenido del dispositivo o el medio. La reproducción automática, según la configuración actual, realiza una de las acciones siguientes.
title: Uso y configuración de la reproducción automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808876"
---
# <a name="using-and-configuring-autoplay"></a>Uso y configuración de la reproducción automática

Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión activa, se determina el contenido del dispositivo o el medio. La reproducción automática, según la configuración actual, realiza una de las acciones siguientes.

-   Reproduce el contenido automáticamente.
-   Muestra un cuadro de diálogo que pide al usuario que elija un controlador predeterminado para un solo tipo de contenido.
-   Presenta, en el caso de contenido mixto, una lista de las aplicaciones de controlador disponibles que se van a iniciar. El controlador elegido reproduce automáticamente su tipo de contenido asociado.
-   Muestra una vista de carpeta estándar de los archivos.
-   No hace nada si, antes, el usuario decidió **no realizar ninguna acción** para ese tipo de contenido, sino que **siempre realiza la acción seleccionada**.

Si el contenido no cumple los criterios de reproducción automática, el evento se pasa a la adquisición de imágenes de Windows (WIA).

En los temas siguientes se describe la instalación y el uso de la reproducción automática.

-   [Preparación del hardware y el software para su uso con reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Cómo busca la reproducción automática multimedia](#how-autoplay-searches-media)
-   [Definir tipos de contenido único y mixto](#defining-single-and-mixed-content-types)
-   [Escenarios de ejemplo](#sample-scenarios)
    -   [Reproducción automática de dispositivos de almacenamiento con medios de imagen](#autoplay-for-storage-devices-with-picture-media)
    -   [Reproducción automática de dispositivos de reproducción de archivos de música y dispositivos de almacenamiento que contienen medios de música](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Reproducción automática para reproducción de vídeo en la primera presentación](#autoplay-for-video-playback-on-first-presentation)
-   [Asignar aplicaciones de controlador predeterminadas](#assigning-default-handler-applications)
-   [Controlar medios que contienen tipos de contenido mixtos](#handling-media-containing-mixed-content-types)
-   [Interfaces de usuario de reproducción automática](#autoplay-user-interfaces)
    -   [Cuadro de diálogo de tipo de contenido único](#single-content-type-dialog-box)
    -   [Cuadro de diálogo medios mixtos](#mixed-media-dialog-box)
    -   [Página de propiedades](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Preparación del hardware y el software para su uso con reproducción automática

Es necesario que aparezcan varios fragmentos de información en el registro para que funcione la reproducción automática. Estos fragmentos de información interactúan y hacen referencia entre sí para formar el entorno completo de reproducción automática. En este documento se presenta la configuración de cada uno de estos fragmentos de información como un procedimiento independiente individual.

Vea los temas siguientes para obtener instrucciones adicionales.

-   [Asignación de un controlador de dispositivo a un dispositivo](how-to-assign-a-device-handler-to-a-device.md)
-   [Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante una clase de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Cómo evitar la reproducción automática de un componente](how-to-prevent-autoplay-for-a-component.md)
-   [Cómo registrar un controlador para un evento de dispositivo](how-to-register-a-handler-for-a-device-event.md)
-   [Cómo usar eventos de reproducción automática en aplicaciones en ejecución](how-to-use-autoplay-events-in-running-applications.md)
-   [Cómo registrar un controlador de eventos](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Cómo busca la reproducción automática multimedia

La reproducción automática busca los elementos multimedia de cuatro niveles de directorio por debajo del directorio raíz para buscar tipos de archivo conocidos. Usa el valor PerceivedType asociado a una extensión de nombre de archivo en el registro para determinar la categoría del archivo, si se trata de una imagen, un archivo de audio o un archivo de vídeo. Con esta información, la reproducción automática inicia el controlador adecuado para ese dispositivo y tipo de archivo. Para obtener más información, vea [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Definir tipos de contenido único y mixto

La reproducción automática define tres categorías de contenido principales.

-   Imágenes
-   Música
-   Vídeo

Se considera que un medio contiene un solo tipo de contenido si todos los archivos del medio se encuentran en una sola de estas tres categorías. Tenga en cuenta que esto no significa que los archivos deben tener el mismo tipo de *archivo* ;. jpg,. gif y. bmp son tipos de archivo diferentes, pero un tipo de contenido (imágenes).

Si los tipos de contenido admitidos están presentes en el medio, pero ningún tipo de contenido único puede tener en cuenta el 100 por ciento del total, se considera que el medio contiene un tipo de contenido mixto y se administra en consecuencia. Para obtener más información, vea [controlar medios que contienen tipos de contenido mixto](#handling-media-containing-mixed-content-types).

## <a name="sample-scenarios"></a>Escenarios de ejemplo

Los escenarios siguientes proporcionan una descripción básica de lo que se debe esperar de la reproducción automática.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>Reproducción automática de dispositivos de almacenamiento con medios de imagen

1.  El usuario conecta un dispositivo de lector CompactFlash USB SanDisk que ya tiene un medio insertado con un tipo de contenido de imagen del 100 por ciento en forma de archivos. jpg.
2.  La notificación muestra **el nuevo hardware-SanDisk ImageMate**.
3.  Reproducción automática inicia la aplicación de imagen adecuada.

Del mismo modo, cuando el usuario inserta el mismo medio de CompactFlash en el lector cuando el lector ya está conectado al sistema, el evento de inserción de medios también hace que la reproducción automática inicie la aplicación de presentación de imágenes. El usuario tiene la opción de ir a la página de propiedades del dispositivo multimedia SanDisk para cambiar el valor predeterminado a otra aplicación de reproducción automática registrada, como el Asistente para escáneres y cámaras o Picture It!.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>Reproducción automática de dispositivos de reproducción de archivos de música y dispositivos de almacenamiento que contienen medios de música

1.  El usuario conecta un reproductor MP3 de Diamond Rio USB.
2.  La notificación muestra **el nuevo hardware, el reproductor mp3 de Diamond Rio**.
3.  La reproducción automática reproduce los archivos con el controlador predeterminado registrado, por ejemplo, Windows Media Player.

Del mismo modo, si el usuario inserta cualquier medio que contenga archivos. mp3 (por ejemplo, CompactFlash, SmartMedia, Memory Stick o un CD-ROM) que representen el 100 por ciento del contenido total admitido en un dispositivo de almacenamiento, el evento de inserción de medios también haría que la reproducción automática reproducira los archivos con la Media Player de Windows. El usuario puede tener acceso a la hoja de propiedades del dispositivo de almacenamiento y cambiar la acción predeterminada a otra aplicación de reproducción automática registrada, como WinAmp o Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Reproducción automática para reproducción de vídeo en la primera presentación

1.  El usuario se conecta a una cámara de vídeo digital 1394 por primera vez.
2.  Al usuario se le presenta un cuadro de diálogo simple que pregunta qué aplicación se va a ejecutar. Las opciones son ejecutar una de las aplicaciones de reproducción automática registradas o abrir una carpeta para ver los archivos. El usuario puede establecer el comportamiento seleccionado para que se guarde como la acción predeterminada para los eventos de conexión en caliente de la cámara de vídeo digital posterior.

## <a name="assigning-default-handler-applications"></a>Asignar aplicaciones de controlador predeterminadas

Una instalación nueva de Windows busca la reproducción automática con un conjunto de aplicaciones de controlador registradas. Las aplicaciones registradas de forma predeterminada durante una instalación de Windows son las siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de soporte</th>
<th>APLICACIONES</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Imágenes</td>
<td><ul>
<li>Presentación (valor predeterminado)</li>
<li>Asistente para cámara y escáner</li>
<li>Asistente para impresión</li>
<li>Abrir carpeta</li>
</ul></td>
</tr>
<tr class="even">
<td>Música</td>
<td><ul>
<li>Media Player de Windows (valor predeterminado)</li>
<li>Abrir carpeta</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vídeo</td>
<td><ul>
<li>Media Player de Windows (valor predeterminado)</li>
<li>Abrir carpeta</li>
</ul></td>
</tr>
</tbody>
</table>



 

En el caso de los tipos no compatibles, se pide a los usuarios que asignen la configuración predeterminada para la acción de reproducción automática asociada con cada dispositivo de almacenamiento en su primera introducción al sistema. En ese momento, se solicita al usuario que elija una acción de una lista proporcionada de aplicaciones registradas o que muestre una vista de carpeta que enumera el contenido multimedia. El usuario también tiene la opción de elegir que se le solicite cada vez que se detecta el tipo de medio en lugar de guardar una aplicación concreta como valor predeterminado.

> [!Note]  
> Los fabricantes de dispositivos tienen la opción de registrar y asignar las aplicaciones predeterminadas que se usarán con sus productos particulares. En estos casos, no se muestra el cuadro de diálogo que ofrece la opción de elegir al usuario.

 

Para que la reproducción automática se ofrezca como una opción de controlador, las aplicaciones recién instaladas deben registrarse en el registro. Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).

Los usuarios siempre pueden cambiar el controlador de reproducción automática predeterminado para cualquier dispositivo de almacenamiento o tipo de contenido. La página de propiedades de reproducción automática es accesible para su cambio en la hoja de propiedades del dispositivo de almacenamiento en **mi PC**.

Para obtener ejemplos de mensajes de usuario y páginas de propiedades, consulte las [interfaces de usuario de reproducción automática](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Controlar medios que contienen tipos de contenido mixtos

Cuando se presenta la reproducción automática con un medio de contenido mixto, se requiere la intervención del usuario antes de que pueda actuar. En este caso, se presenta al usuario un cuadro de diálogo que contiene una lista filtrada de todas las aplicaciones registradas adecuadas disponibles para los tipos de contenido presentes en el medio. El usuario puede elegir una de estas aplicaciones para la reproducción automática de un tipo de contenido determinado, mientras que el resto permanece intacto. Dado que la composición de los medios de contenido mixto varía con cada disco individual, no hay ninguna opción para guardar esta opción como valor predeterminado.

Para obtener ejemplos de mensajes de usuario, consulte las [interfaces de usuario de reproducción automática](#autoplay-user-interfaces).

## <a name="autoplay-user-interfaces"></a>Interfaces de usuario de reproducción automática

Hay tres interfaces de usuario posibles.

-   Cuadro de diálogo que pide al usuario que escriba una acción para un único tipo de contenido.
-   Cuadro de diálogo que pide al usuario que escriba una acción para los tipos de contenido mixto
-   Una página de propiedades

### <a name="single-content-type-dialog-box"></a>Cuadro de diálogo de tipo de contenido único

Se muestra un cuadro de diálogo similar al siguiente cuando todavía no se ha asignado a ningún medio compatible una acción de reproducción automática predeterminada en el sistema.

![captura de pantalla del cuadro de diálogo tipo de contenido único](images/pix.png)

Los usuarios pueden realizar una de las siguientes acciones.

-   Elija una acción de la lista de aplicaciones registradas.
-   Enumere los archivos del medio en una vista de carpeta normal.
-   No realizar ninguna acción.

Un usuario también puede guardar una opción como acción predeterminada para este medio haciendo clic en el cuadro **realizar siempre la acción seleccionada** . Una vez realizada esta opción, el cuadro de diálogo no se muestra de nuevo. Sin embargo, en el Service Pack 1 (SP1) de Windows XP, si se agrega al equipo una nueva aplicación que puede controlar un tipo de medio determinado, el cuadro de diálogo se muestra de nuevo al usuario, lo que les permite seleccionar la nueva aplicación como la acción de reproducción automática predeterminada. Las aplicaciones también se pueden establecer como la selección predeterminada cuando se instalan.

Windows XP SP1 también agrega una característica que conserva la elección de la acción de reproducción automática del usuario si no hace clic en el cuadro **realizar siempre la acción seleccionada** . Si un usuario elige una acción de reproducción automática para una única instancia, la siguiente vez que se presenta el cuadro de diálogo para ese tipo de medio, la misma acción es la selección predeterminada.

Para que una aplicación se incluya en la lista de acciones posibles, debe estar registrada con la reproducción automática. Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Cuadro de diálogo medios mixtos

El siguiente cuadro de diálogo se muestra cuando se presenta al sistema cualquier medio que contenga una combinación de tipos de archivo admitidos. Esto es esencialmente el mismo que el cuadro de diálogo de medio de contenido único, pero con dos diferencias importantes. En primer lugar, las opciones de acción disponibles constan de una lista filtrada de las aplicaciones relevantes para todos los tipos de contenido presentes en el medio. En segundo lugar, no hay ninguna opción para elegir una acción predeterminada permanente, ya que los tipos de contenido y los porcentajes de los medios de contenido mixto son demasiado impredecibles.

![captura de pantalla del cuadro de diálogo medios mixtos](images/mix.png)

Para que una aplicación se incluya en la lista de acciones posibles, debe estar registrada con la reproducción automática. Para obtener más información, consulte [preparación del hardware y el software para su uso con la reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Página de propiedades

A continuación se muestra una página de propiedades de reproducción automática de ejemplo para un dispositivo de DVD o CD-ROM.

![captura de pantalla de la página de propiedades](images/apdlg.png)

Cada tipo de dispositivo ofrece un subconjunto adecuado de tipos de contenido para la configuración de reproducción automática. A su vez, cada tipo de contenido, cuando se selecciona, ofrece una lista adecuada de opciones de acción en el cuadro de lista. Se puede elegir una acción diferente para cada tipo de contenido.

 

 



