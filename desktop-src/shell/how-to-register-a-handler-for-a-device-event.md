---
description: Describe los procesos para implementar controladores de eventos de dispositivo en el Registro.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Cómo registrar un controlador para un evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859604"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Cómo registrar un controlador para un evento de dispositivo

Los controladores definen la parte del software de Reproducción automática. Definen el icono y el nombre descriptivo del software, así como el componente Modelo de objetos componentes (COM) para crear instancias y cómo inicializar el componente en respuesta a un evento. Cada controlador de un evento específico se registra como un valor en la clave **EventHandler** adecuada. Cuando se detecta ese evento, se solicita al usuario que elija un controlador de una lista de todos los controladores registrados para ese evento.

## <a name="instructions"></a>Instructions


Los controladores y sus valores asociados se definen en la **clave Controladores de AutoplayHandlers.** \\  Las subclaves difieren en función de si el sistema puede leer el contenido del dispositivo directamente o de si el dispositivo proporciona contenido al sistema a través de una interfaz propietaria.

En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo, como una cámara de vídeo digital o un reproductor de .mp3, que proporciona su contenido al sistema a través de una interfaz propietaria. El controlador de ejemplo se denomina **MyHandler.**

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
> Aunque en el ejemplo se muestra un progID y un valor de identificador de clase (CLSID), en la práctica estos valores son mutuamente excluyentes para que solo uno u otro estén presentes. Se prefiere el valor progID. Independientemente de lo que se utilice, debe apuntar a un componente COM que implementa la [**interfaz IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

 

Puede escribir el valor Action como un valor literal, por ejemplo"Reproducir música", como se muestra en este ejemplo, o como un nombre de archivo con una cadena de recursos. También puede especificar el valor proveedor como un valor literal o como un nombre de archivo con una cadena de recurso. Reproducción automática combina el valor action y el valor provider con la palabra "using" para crear un título descriptivo que se muestra en la interfaz de usuario. En el ejemplo, el título resultante es "Reproducir música con Reproductor de Windows Media".

El valor DefaultIcon apunta a un archivo .ico o a un recurso de un archivo binario. Si el valor numérico que sigue al nombre de archivo binario es cero o mayor, es el valor de índice del icono en ese archivo binario. Si es un valor negativo, es el identificador de recurso del icono. Se recomiendan valores de índice negativos. No se necesita ningún valor en el caso de un archivo .ico. Se recomienda usar variables de entorno en la ruta de acceso.

El valor InitCmdLine pasa sin modificar a través del método [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de llamar a cualquier otro método.

En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo que se puede leer directamente, como una unidad de CD-ROM u otro disco extraíble. De nuevo, el controlador de ejemplo se **denomina MyHandler.**

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

En este ejemplo, los valores Action y Provider se muestran como un nombre de archivo con una cadena de recursos en lugar de valores literales, pero las cadenas a las que hacen referencia se usan de la misma manera. Se combinan con la palabra "using" para formar un título descriptivo como se explicó anteriormente.

Los valores InvokeProgID e InvokeVerb reemplazan a CLSID, InitCmdLine y ProgID. Los valores InvokeProgID e InvokeVerb coinciden con los nombres de clave que se encuentran en **HKEY \_ CLASSES \_ ROOT**, como se muestra en la siguiente entrada del Registro. Este conjunto de claves de ejemplo corresponde al ejemplo de controlador específico descrito anteriormente.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

La [**función CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa el CLSID para implementar la aplicación adecuada.

Después de definir el controlador de cualquiera de estas dos maneras, debe registrarlo para un evento específico. Para ello, proporcione el nombre del controlador como un valor para la clave de ese evento en **EventHandlers**. En el ejemplo siguiente se muestra cómo **registrar MyHandler** como controlador para el evento GenericVolumeArrival. No tiene ningún valor de datos asignado.

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

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
