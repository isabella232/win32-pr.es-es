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
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="c136e-103">Cómo registrar un controlador para un evento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c136e-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="c136e-104">Los controladores definen la parte de software de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="c136e-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="c136e-105">Definen el icono y el nombre descriptivo del software, así como el componente del modelo de objetos componentes (COM) para crear instancias y cómo inicializar el componente como respuesta a un evento.</span><span class="sxs-lookup"><span data-stu-id="c136e-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="c136e-106">Cada controlador de un evento específico se registra como un valor en la clave **EventHandler** adecuada.</span><span class="sxs-lookup"><span data-stu-id="c136e-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="c136e-107">Cuando se detecta ese evento, se solicita al usuario que elija un controlador de una lista de todos los controladores registrados para ese evento.</span><span class="sxs-lookup"><span data-stu-id="c136e-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="c136e-108">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c136e-108">Instructions</span></span>


<span data-ttu-id="c136e-109">Los controladores y sus valores asociados se definen en la  \\ clave de **Controladores** AutoplayHandlers.</span><span class="sxs-lookup"><span data-stu-id="c136e-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="c136e-110">Las subclaves varían en función de si el sistema puede leer el contenido del dispositivo directamente o si el dispositivo proporciona contenido al sistema a través de una interfaz de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c136e-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="c136e-111">En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo, como una cámara de vídeo digital o un reproductor. mp3, que proporciona su contenido al sistema a través de una interfaz de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c136e-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="c136e-112">El controlador de ejemplo se denomina **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="c136e-112">The example handler is called **MyHandler**.</span></span>

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
> <span data-ttu-id="c136e-113">Aunque en el ejemplo se muestra un ProgID y un valor de identificador de clase (CLSID), en la práctica estos valores son mutuamente excluyentes para que solo esté presente uno u otro.</span><span class="sxs-lookup"><span data-stu-id="c136e-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="c136e-114">Se prefiere el valor ProgID.</span><span class="sxs-lookup"><span data-stu-id="c136e-114">The ProgID value is preferred.</span></span> <span data-ttu-id="c136e-115">Lo que se use, debe señalar a un componente COM que implementa la interfaz [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="c136e-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="c136e-116">Puede escribir el valor de la acción como un valor literal, por ejemplo "reproducir música", tal como se muestra en este ejemplo, o como un nombre de archivo con una cadena de recursos.</span><span class="sxs-lookup"><span data-stu-id="c136e-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="c136e-117">También puede especificar el valor del proveedor como un valor literal o como un nombre de archivo con una cadena de recursos.</span><span class="sxs-lookup"><span data-stu-id="c136e-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="c136e-118">La reproducción automática combina el valor de la acción y el valor del proveedor con la palabra "usando" para crear un título descriptivo que se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c136e-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="c136e-119">En el ejemplo, el título resultante es "reproducir música con Windows Media Player."</span><span class="sxs-lookup"><span data-stu-id="c136e-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="c136e-120">El valor DefaultIcon apunta a un archivo. ico o a un recurso en un archivo binario.</span><span class="sxs-lookup"><span data-stu-id="c136e-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="c136e-121">Si el valor numérico que sigue al nombre del archivo binario es cero o superior, es el valor de índice del icono de ese archivo binario.</span><span class="sxs-lookup"><span data-stu-id="c136e-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="c136e-122">Si es un valor negativo, es el identificador de recurso del icono.</span><span class="sxs-lookup"><span data-stu-id="c136e-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="c136e-123">Se recomiendan los valores de índice negativos.</span><span class="sxs-lookup"><span data-stu-id="c136e-123">Negative index values are recommended.</span></span> <span data-ttu-id="c136e-124">No es necesario ningún valor en el caso de un archivo. ico.</span><span class="sxs-lookup"><span data-stu-id="c136e-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="c136e-125">Se recomienda usar variables de entorno en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c136e-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="c136e-126">El valor InitCmdLine pasa sin modificar a través del método [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de que se llame a otros métodos.</span><span class="sxs-lookup"><span data-stu-id="c136e-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="c136e-127">En el ejemplo siguiente se muestran las subclaves y los valores que se usan para un dispositivo que se puede leer directamente, como una unidad de CD-ROM u otro disco extraíble.</span><span class="sxs-lookup"><span data-stu-id="c136e-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="c136e-128">De nuevo, el controlador de ejemplo se denomina **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="c136e-128">Again, the example handler is called **MyHandler**.</span></span>

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

<span data-ttu-id="c136e-129">En este ejemplo, los valores de acción y proveedor se muestran como un nombre de archivo con una cadena de recurso en lugar de valores literales, pero las cadenas a las que hacen referencia se usan de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="c136e-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="c136e-130">Se combinan con la palabra "Using" para formar un título descriptivo como se explicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c136e-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="c136e-131">Los valores InvokeProgID y InvokeVerb reemplazan CLSID, InitCmdLine y ProgID.</span><span class="sxs-lookup"><span data-stu-id="c136e-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="c136e-132">Los valores InvokeProgID y InvokeVerb coinciden con los nombres de clave que se encuentran en **HKEY \_ classes \_ root**, tal como se muestra en la siguiente entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="c136e-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="c136e-133">Este conjunto de claves de ejemplo corresponde al ejemplo de controlador específico que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c136e-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="c136e-134">La función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa el CLSID para implementar la aplicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="c136e-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="c136e-135">Después de definir el controlador en cualquiera de estas dos formas, debe registrarlo para un evento específico.</span><span class="sxs-lookup"><span data-stu-id="c136e-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="c136e-136">Para ello, proporcione el nombre del controlador como un valor para la clave de ese evento en **EventHandlers**.</span><span class="sxs-lookup"><span data-stu-id="c136e-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="c136e-137">En el ejemplo siguiente se muestra cómo registrar **MyHandler** como un controlador para el evento GenericVolumeArrival.</span><span class="sxs-lookup"><span data-stu-id="c136e-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="c136e-138">No tiene ningún valor de datos asignado.</span><span class="sxs-lookup"><span data-stu-id="c136e-138">It has no assigned data value.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c136e-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c136e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c136e-140">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c136e-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="c136e-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="c136e-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
