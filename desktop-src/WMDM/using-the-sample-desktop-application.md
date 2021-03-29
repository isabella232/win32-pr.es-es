---
title: Usar la aplicación de escritorio de ejemplo
description: Usar la aplicación de escritorio de ejemplo
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774281"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="e63cd-109">Usar la aplicación de escritorio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e63cd-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="e63cd-110">La aplicación de escritorio de ejemplo es una ventana básica de dos paneles similar a la del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="e63cd-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="e63cd-111">Permite examinar el contenido de un dispositivo, usar una vista de árbol de carpetas en el panel izquierdo y archivos en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="e63cd-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="e63cd-112">La raíz de cada árbol de carpetas se considera lógicamente un dispositivo diferente, aunque algunos dispositivos pueden representarse como varios objetos (uno por cada almacenamiento raíz).</span><span class="sxs-lookup"><span data-stu-id="e63cd-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="e63cd-113">Para leer las propiedades básicas de una carpeta o un archivo, haga clic con el botón secundario en el objeto y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="e63cd-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="e63cd-114">Puede eliminar archivos en el dispositivo seleccionando un archivo en el panel derecho y seleccionando **eliminar** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="e63cd-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="e63cd-115">Para agregar archivos multimedia al dispositivo, puede arrastrar archivos desde el escritorio hasta el panel derecho del programa.</span><span class="sxs-lookup"><span data-stu-id="e63cd-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="e63cd-116">Tenga en cuenta que los archivos deben tener un formato multimedia compatible con el dispositivo. los archivos de formatos no aceptables (archivos no multimedia, como archivos. txt o formatos multimedia no admitidos por el dispositivo) no se enviarán al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e63cd-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="e63cd-117">(Tenga en cuenta que esta restricción es la del programa; Windows Media Administrador de dispositivos permite enviar cualquier archivo a un dispositivo si el dispositivo lo aceptará.</span><span class="sxs-lookup"><span data-stu-id="e63cd-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="e63cd-118">Para capturar los eventos de devolución de llamada enviados a la interfaz [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , debe activar la opción "usar interfaz de operación" en el menú **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="e63cd-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="e63cd-119">El menú **Opciones** también le permite elegir si desea usar varias interfaces más avanzadas con características compatibles con dispositivos avanzados.</span><span class="sxs-lookup"><span data-stu-id="e63cd-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="e63cd-120">El menú **contenedores** tiene opciones que le permiten crear una lista de reproducción o un álbum.</span><span class="sxs-lookup"><span data-stu-id="e63cd-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="e63cd-121">Para crear una lista de reproducción, seleccione una o varias canciones en el dispositivo y haga clic en **crear lista de reproducción** en el menú **contenedores** .</span><span class="sxs-lookup"><span data-stu-id="e63cd-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="e63cd-122">Esta característica solo funciona en dispositivos MTP, ya que el código solo admite la creación de un archivo de lista de reproducción "virtual".</span><span class="sxs-lookup"><span data-stu-id="e63cd-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="e63cd-123">(Una lista de reproducción virtual es una lista de reproducción que solo se especifica mediante valores de metadatos, en lugar de un archivo físico, por ejemplo un archivo WPL). El dispositivo debe admitir listas de reproducción vacías para usar esta característica.</span><span class="sxs-lookup"><span data-stu-id="e63cd-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="e63cd-124">Para crear un álbum (una lista de reproducción con una imagen asociada), seleccione una o varias canciones en el dispositivo y haga clic en **crear álbum** en el menú **contenedores** .</span><span class="sxs-lookup"><span data-stu-id="e63cd-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="e63cd-125">Un cuadro de diálogo le permite buscar un archivo de imagen en el equipo para asociarlo con el álbum.</span><span class="sxs-lookup"><span data-stu-id="e63cd-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="e63cd-126">Del mismo modo que crea listas de reproducción, la aplicación crea un archivo de álbum "vacío"; Si el dispositivo no admite álbumes vacíos, esta característica no funcionará.</span><span class="sxs-lookup"><span data-stu-id="e63cd-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e63cd-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e63cd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e63cd-128">**Aplicación de escritorio de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e63cd-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




