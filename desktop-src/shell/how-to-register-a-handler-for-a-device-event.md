---
description: Describe los procesos para implementar controladores de eventos de dispositivo en el registro.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Cómo registrar un controlador para un evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909537"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Cómo registrar un controlador para un evento de dispositivo

Los controladores definen la parte de software de reproducción automática. Definen el icono y el nombre descriptivo del software, así como el componente del modelo de objetos componentes (COM) para crear instancias y cómo inicializar el componente como respuesta a un evento. Cada controlador de un evento específico se registra como un valor en la clave **EventHandler** adecuada. Cuando se detecta ese evento, se solicita al usuario que elija un controlador de una lista de todos los controladores registrados para ese evento.

## <a name="instructions"></a>Instrucciones


Los controladores y sus valores asociados se definen en la  \\ clave de **Controladores** AutoplayHandlers. Las subclaves varían en función de si el sistema puede leer el contenido del dispositivo directamente o si el dispositivo proporciona contenido al sistema a través de una interfaz de propiedad.

En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo, como una cámara de vídeo digital o un reproductor. mp3, que proporciona su contenido al sistema a través de una interfaz de propiedad. El controlador de ejemplo se denomina **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> Aunque en el ejemplo se muestra un ProgID y un valor de identificador de clase (CLSID), en la práctica estos valores son mutuamente excluyentes para que solo esté presente uno u otro. Se prefiere el valor ProgID. Lo que se use, debe señalar a un componente COM que implementa la interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

 

Puede escribir el valor de la acción como un valor literal, por ejemplo "reproducir música", tal como se muestra en este ejemplo, o como un nombre de archivo con una cadena de recursos. También puede especificar el valor del proveedor como un valor literal o como un nombre de archivo con una cadena de recursos. La reproducción automática combina el valor de la acción y el valor del proveedor con la palabra "usando" para crear un título descriptivo que se muestra en la interfaz de usuario. En el ejemplo, el título resultante es "reproducir música con Windows Media Player."

El valor DefaultIcon apunta a un archivo. ico o a un recurso en un archivo binario. Si el valor numérico que sigue al nombre del archivo binario es cero o superior, es el valor de índice del icono de ese archivo binario. Si es un valor negativo, es el identificador de recurso del icono. Se recomiendan los valores de índice negativos. No es necesario ningún valor en el caso de un archivo. ico. Se recomienda usar variables de entorno en la ruta de acceso.

El valor InitCmdLine pasa sin modificar a través del método [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de que se llame a otros métodos.

En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo que se puede leer directamente, como una unidad de CD-ROM u otro disco extraíble. De nuevo, el controlador de ejemplo se denomina **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

En este ejemplo, los valores de acción y proveedor se muestran como un nombre de archivo con una cadena de recurso en lugar de valores literales, pero las cadenas a las que hacen referencia se usan de la misma manera. Se combinan con la palabra "Using" para formar un título descriptivo como se explicó anteriormente.

Los valores InvokeProgID y InvokeVerb reemplazan CLSID, InitCmdLine y ProgID. Los valores InvokeProgID y InvokeVerb coinciden con los nombres de clave que se encuentran en **HKEY \_ classes \_ root**, tal como se muestra en la siguiente entrada del registro. Este conjunto de claves de ejemplo corresponde al ejemplo de controlador específico que se ha descrito anteriormente.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

La función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa el CLSID para implementar la aplicación adecuada.

Después de definir el controlador en cualquiera de estas dos formas, debe registrarlo para un evento específico. Para ello, proporcione el nombre del controlador como un valor para la clave de ese evento en **EventHandlers**. En el ejemplo siguiente se muestra cómo registrar **MyHandler** como un controlador para el evento GenericVolumeArrival. No tiene ningún valor de datos asignado.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
