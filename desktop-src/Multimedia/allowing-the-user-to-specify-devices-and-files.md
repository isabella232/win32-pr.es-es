---
title: Permitir al usuario especificar dispositivos y archivos
description: Permitir al usuario especificar dispositivos y archivos
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog (macro)
- MCIWndOpen (macro)
- MCIWndOpenInterface (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776519"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="5f0e3-106">Permitir al usuario especificar dispositivos y archivos</span><span class="sxs-lookup"><span data-stu-id="5f0e3-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="5f0e3-107">Puede asociar un dispositivo o un archivo a una ventana de MCIWnd existente mediante las macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)y [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) , y la función [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="5f0e3-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="5f0e3-108">Para permitir que un usuario de la aplicación Seleccione un archivo para reproducirlo, use **MCIWndOpenDialog**.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="5f0e3-109">Esta macro muestra el cuadro de diálogo **abrir** (que se muestra en la siguiente captura de pantalla) para elegir un archivo y asocia el archivo seleccionado a la ventana de MCIWnd actual.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![imagen de la ventana de mciwnd](images/mciwnd3.gif)

<span data-ttu-id="5f0e3-111">Puede permitir que un usuario de la aplicación Seleccione un archivo para asociarlo a una ventana de MCIWnd y obtenga una vista previa del archivo mediante [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span><span class="sxs-lookup"><span data-stu-id="5f0e3-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="5f0e3-112">La función **GetOpenFileNamePreview** muestra el cuadro de diálogo **abrir** para elegir un archivo y permite a la vista previa del usuario (reproducir) su contenido.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="5f0e3-113">Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo, **GetOpenFileNamePreview** proporciona un pequeño control para permitir que el usuario obtenga una vista previa del contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="5f0e3-114">Puede asociar un archivo especificado, seleccionado con **GetOpenFileNamePreview** o especificado de otra manera, con una ventana de MCIWnd con **MCIWndOpen**.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="5f0e3-115">También puede usar **MCIWndOpen** para especificar un dispositivo que se va a asociar a una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="5f0e3-116">Por ejemplo, puede usar un nombre de dispositivo, como "CDAudio".</span><span class="sxs-lookup"><span data-stu-id="5f0e3-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="5f0e3-117">Para asociar una ventana de MCIWnd con una interfaz de archivo o una interfaz de flujo de datos a datos multimedia, use la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="5f0e3-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="5f0e3-118">Para obtener más información sobre las interfaces de archivo y de flujo de datos, vea [AVIFile Functions and macros](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="5f0e3-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="5f0e3-119">Antes de asociar un nuevo archivo o dispositivo a una ventana de MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) y [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) cierran cualquier dispositivo asociado actualmente a la ventana.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="5f0e3-120">No es necesario que la aplicación cierre ningún dispositivo abierto antes de usar estas macros.</span><span class="sxs-lookup"><span data-stu-id="5f0e3-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




