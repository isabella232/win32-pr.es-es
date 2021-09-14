---
description: Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión en caliente, se determina el contenido del dispositivo o del medio. La reproducción automática, en función de su configuración actual, realiza una de las siguientes acciones.
title: Uso y configuración de la reproducción automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 35de48ee77cde7c598088b3f3877083efc2151f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361062"
---
# <a name="using-and-configuring-autoplay"></a>Uso y configuración de la reproducción automática

Cuando el shell detecta la inserción de nuevos medios o los datos adjuntos de un dispositivo de conexión en caliente, se determina el contenido del dispositivo o del medio. La reproducción automática, en función de su configuración actual, realiza una de las siguientes acciones.

-   Reproduce el contenido automáticamente.
-   Muestra un cuadro de diálogo en el que se solicita al usuario que elija un controlador predeterminado para un único tipo de contenido.
-   Presenta, en el caso de contenido mixto, una lista de aplicaciones de controlador disponibles para iniciar. A continuación, el controlador elegido reproduce automáticamente su tipo de contenido asociado.
-   Muestra una vista de carpeta estándar de los archivos.
-   No hace nada si, anteriormente, el usuario había elegido No realizar **ninguna** acción para ese tipo de contenido, así como especificar **Siempre realizar la acción seleccionada.**

Si el contenido no cumple los criterios de Reproducción automática, el evento se pasa a Windows adquisición de imágenes (WIA).

En los temas siguientes se describe la configuración y el uso de La reproducción automática.

-   [Preparación de hardware y software para su uso con reproducción automática](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Cómo la reproducción automática busca medios](#how-autoplay-searches-media)
-   [Definir tipos de contenido únicos y mixtos](#defining-single-and-mixed-content-types)
-   [Escenarios de ejemplo](#sample-scenarios)
    -   [Reproducción automática para Storage dispositivos con medios de imagen](#autoplay-for-storage-devices-with-picture-media)
    -   [Reproducción automática para Música de reproducción de archivos y Storage dispositivos que contienen Música multimedia](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Reproducción automática para reproducción de vídeo en la primera presentación](#autoplay-for-video-playback-on-first-presentation)
-   [Asignación de aplicaciones de controlador predeterminadas](#assigning-default-handler-applications)
-   [Control de medios que contienen tipos de contenido mixtos](#handling-media-containing-mixed-content-types)
-   [Reproducción automática de interfaces de usuario](#autoplay-user-interfaces)
    -   [Cuadro de diálogo Tipo de contenido único](#single-content-type-dialog-box)
    -   [Cuadro de diálogo Medios mixtos](#mixed-media-dialog-box)
    -   [Página de propiedades](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Preparación de hardware y software para su uso con reproducción automática

Es necesario que aparezcan varios fragmentos de información en el Registro para que la reproducción automática funcione. Estos fragmentos de información interactúan y se hacen referencia entre sí para formar el entorno de Reproducción automática completo. En este documento se presenta la configuración de cada uno de estos fragmentos de información como un procedimiento independiente individual.

Consulte los temas siguientes para obtener instrucciones adicionales.

-   [Asignación de un controlador de dispositivos a un dispositivo](how-to-assign-a-device-handler-to-a-device.md)
-   [Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante un grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante una clase de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Cómo evitar la reproducción automática de un componente](how-to-prevent-autoplay-for-a-component.md)
-   [Cómo registrar un controlador para un evento de dispositivo](how-to-register-a-handler-for-a-device-event.md)
-   [Cómo usar eventos de reproducción automática en aplicaciones en ejecución](how-to-use-autoplay-events-in-running-applications.md)
-   [Cómo registrar un controlador de eventos](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Cómo la reproducción automática busca medios

Reproducción automática busca medios cuatro niveles de directorio por debajo del directorio raíz para buscar tipos de archivo conocidos. Usa el valor PerceivedType asociado a una extensión de nombre de archivo en el Registro para determinar la categoría de archivo, ya sea una imagen, un archivo de audio o un archivo de vídeo. Con esta información, Reproducción automática inicia el controlador adecuado para ese tipo de dispositivo y archivo. Para obtener más información, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Definir tipos de contenido únicos y mixtos

Reproducción automática define tres categorías de contenido principales.

-   Imágenes
-   Música
-   Vídeo

Se considera que un medio contiene un único tipo de contenido si todos los archivos del medio solo se incluyen en una de estas tres categorías. Tenga en cuenta que esto no significa que los archivos deben ser del mismo tipo *de* archivo; .jpg, .gif y .bmp son tipos de archivo diferentes, pero un tipo de contenido (imágenes).

Si los tipos de contenido admitidos están presentes en el medio, pero ningún tipo de contenido único puede tener el 100 % del total, se considera que el medio contiene un tipo de contenido mixto y se controla en consecuencia. Para obtener más información, vea [Control de medios que contienen tipos de contenido mixtos.](#handling-media-containing-mixed-content-types)

## <a name="sample-scenarios"></a>Escenarios de ejemplo

Los escenarios siguientes proporcionan una comprensión básica de lo que se espera de La reproducción automática.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>Reproducción automática para Storage dispositivos con medios de imagen

1.  El usuario conecta un dispositivo de lector SanDisk CompactFlash USB que ya tiene un medio insertado que contiene el tipo de contenido de imagen 100 % en forma de .jpg archivos.
2.  La notificación muestra **El nuevo hardware encontrado: SanDisk ImageMate**.
3.  Reproducción automática inicia la aplicación de imagen adecuada.

De forma similar, cuando el usuario inserta ese mismo medio CompactFlash en el lector cuando el lector ya está conectado al sistema, el evento de inserción multimedia también hace que AutoPlay inicie la aplicación de presentación de diapositivas de imagen. El usuario tiene la opción de ir a la página Propiedades del dispositivo multimedia SanDisk para cambiar el valor predeterminado a otra aplicación de Reproducción automática registrada, como el Asistente para escáner y cámara o Imagen.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>Reproducción automática para Música de reproducción de archivos y Storage dispositivos que contienen Música multimedia

1.  El usuario conecta un reproductor USB Diamond Rio MP3.
2.  La notificación muestra **Found New Hardware - Diamond Rio MP3 Player**.
3.  Reproducción automática reproduce los archivos mediante su controlador predeterminado registrado, por ejemplo, Reproductor de Windows Media.

Del mismo modo, si el usuario inserta cualquier medio que contenga archivos .mp3 (por ejemplo, CompactFlash, SmartMedia, Memory Stick o CD-ROM) que representan el 100 % del contenido total admitido en un dispositivo de almacenamiento, el evento de inserción multimedia también provocaría que La reproducción automática reproteja los archivos mediante el Reproductor de Windows Media. El usuario puede acceder a la hoja de propiedades del dispositivo de almacenamiento y cambiar la acción predeterminada a otra aplicación de Reproducción automática registrada, como WinAmp o Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Reproducción automática para reproducción de vídeo en la primera presentación

1.  El usuario conecta una cámara de vídeo digital 1394 por primera vez.
2.  El usuario aparece con un cuadro de diálogo simple que pregunta qué aplicación se va a ejecutar. Las opciones son ejecutar una de las aplicaciones de Reproducción automática registradas o abrir una carpeta para ver los archivos. El usuario puede establecer el comportamiento seleccionado para guardarse como la acción predeterminada para eventos de conexión en caliente de la cámara de vídeo digital posteriores.

## <a name="assigning-default-handler-applications"></a>Asignación de aplicaciones de controlador predeterminadas

Una instalación nueva de Windows busca La reproducción automática con un conjunto de aplicaciones de controlador registradas. Las aplicaciones registradas de forma predeterminada durante Windows instalación son las siguientes.




| Tipo de soporte | Aplicaciones | 
|------------|--------------|
| Imágenes | <ul><li>Presentación con diapositivas (valor predeterminado)</li><li>Asistente para cámara y escáner</li><li>Asistente para impresión</li><li>Abrir carpeta</li></ul> | 
| Música | <ul><li>Reproductor de Windows Media (valor predeterminado)</li><li>Abrir carpeta</li></ul> | 
| Vídeo | <ul><li>Reproductor de Windows Media (valor predeterminado)</li><li>Abrir carpeta</li></ul> | 




 

En el caso de los tipos no admitidos, se pide a los usuarios que asignen la configuración predeterminada para la acción Reproducción automática asociada a cada dispositivo de almacenamiento en su primera introducción al sistema. En ese momento, se pide al usuario que elija una acción de una lista proporcionada de aplicaciones registradas o que muestre una vista de carpeta que muestre el contenido multimedia. El usuario también tiene la opción de elegir que se le solicite cada vez que se detecta el tipo de medio en lugar de guardar cualquier aplicación determinada como valor predeterminado.

> [!Note]  
> Los fabricantes de dispositivos tienen la opción de registrar y asignar aplicaciones predeterminadas que se usarán con sus productos concretos. En estos casos, no se muestra el cuadro de diálogo que ofrece una opción al usuario.

 

Para que AutoPlay la ofreca como opción de controlador, las aplicaciones recién instaladas deben registrarse en el Registro. Para obtener más información, vea [Preparar hardware y software para su uso con Reproducción automática.](#preparing-hardware-and-software-for-use-with-autoplay)

Los usuarios siempre pueden cambiar el controlador de reproducción automática predeterminado para cualquier tipo de contenido o dispositivo de almacenamiento. La página de propiedades Reproducción automática es accesible para el cambio en la hoja de propiedades del dispositivo de almacenamiento **Mi PC**.

Para obtener ejemplos de mensajes de usuario y páginas de propiedades, vea [Reproducción automática de interfaces de usuario.](#autoplay-user-interfaces)

## <a name="handling-media-containing-mixed-content-types"></a>Control de medios que contienen tipos de contenido mixtos

Cuando La reproducción automática se presenta con un medio de contenido mixto, requiere la entrada del usuario para poder tomar medidas. En este caso, se presenta al usuario un cuadro de diálogo que contiene una lista filtrada de todas las aplicaciones registradas adecuadas disponibles para los tipos de contenido presentes en los medios. El usuario puede elegir una de estas aplicaciones para reproducción automática de ese tipo de contenido concreto, mientras que el resto permanece intacto. Como la composición de los medios de contenido mixto varía con cada disco individual, no hay ninguna opción para guardar esta opción de forma predeterminada.

Para obtener ejemplos de mensajes de usuario, vea [Reproducción automática de interfaces de usuario.](#autoplay-user-interfaces)

## <a name="autoplay-user-interfaces"></a>Reproducción automática de interfaces de usuario

Hay tres interfaces de usuario posibles.

-   Cuadro de diálogo que solicita al usuario que escriba una acción para un único tipo de contenido
-   Cuadro de diálogo que solicita al usuario que escriba una acción para tipos de contenido mixtos
-   Una página de propiedades

### <a name="single-content-type-dialog-box"></a>Cuadro de diálogo Tipo de contenido único

Se muestra un cuadro de diálogo similar al siguiente cuando se presenta al sistema cualquier medio compatible que aún no haya asignado una acción de reproducción automática predeterminada.

![captura de pantalla del cuadro de diálogo Tipo de contenido único](images/pix.png)

Los usuarios pueden realizar una de las siguientes acciones.

-   Elija una acción de la lista de aplicaciones registradas.
-   Enumera los archivos del medio en una vista de carpeta normal.
-   No realizar ninguna acción.

Un usuario también puede guardar una opción como acción predeterminada para este medio haciendo clic en **el cuadro Realizar siempre la acción seleccionada.** Una vez realizada esta opción, el cuadro de diálogo no se muestra de nuevo. Sin embargo, en Windows XP Service Pack 1 (SP1), si se agrega una nueva aplicación que puede controlar un tipo de medio determinado al equipo, el cuadro de diálogo se presenta una vez más al usuario, lo que les ofrece la oportunidad de seleccionar la nueva aplicación como acción de reproducción automática predeterminada. Las aplicaciones también pueden establecerse como la selección predeterminada cuando se instalan.

Windows XP SP1 también agrega una característica que conserva la opción del usuario de la acción Reproducción automática si no hace clic en el cuadro Realizar siempre **la acción** seleccionada. Si un usuario elige una acción De reproducción automática para una sola instancia, la próxima vez que se presente ese cuadro de diálogo para ese tipo de medio, la misma acción es la selección predeterminada.

Para que una aplicación se incluya en la lista de posibles acciones, debe registrarse con Reproducción automática. Para obtener más información, vea [Preparar hardware y software para su uso con Reproducción automática.](#preparing-hardware-and-software-for-use-with-autoplay)

### <a name="mixed-media-dialog-box"></a>Cuadro de diálogo Medios mixtos

El siguiente cuadro de diálogo se muestra cuando se presenta al sistema cualquier medio que contenga una combinación de tipos de archivo admitidos. Esto es básicamente lo mismo que el cuadro de diálogo medio de contenido único, pero con dos diferencias significativas. En primer lugar, las opciones de acción disponibles constan de una lista filtrada de aplicaciones relevantes para todos los tipos de contenido presentes en el medio. En segundo lugar, no hay ninguna opción para elegir una acción predeterminada permanente porque los tipos de contenido y los porcentajes de medios de contenido mixto son demasiado impredecibles.

![captura de pantalla del cuadro de diálogo de medios mixtos](images/mix.png)

Para que una aplicación se incluya en la lista de posibles acciones, debe registrarse con Reproducción automática. Para obtener más información, vea [Preparar hardware y software para su uso con Reproducción automática.](#preparing-hardware-and-software-for-use-with-autoplay)

### <a name="property-page"></a>Página de propiedades

A continuación se muestra una página de propiedades de reproducción automática de ejemplo para un dispositivo DVD/CD-ROM.

![captura de pantalla de la página de propiedades](images/apdlg.png)

Cada tipo de dispositivo ofrece un subconjunto adecuado de tipos de contenido para la configuración de reproducción automática. A su vez, cada tipo de contenido, cuando se selecciona, ofrece una lista adecuada de opciones de acción en el cuadro de lista. Se puede elegir una acción diferente para cada tipo de contenido.

 

 



