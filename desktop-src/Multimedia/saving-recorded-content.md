---
title: Guardar contenido grabado
description: Guardar contenido grabado
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave (macro)
- MCIWndSaveDialog (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775984"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="22a9b-105">Guardar contenido grabado</span><span class="sxs-lookup"><span data-stu-id="22a9b-105">Saving Recorded Content</span></span>

<span data-ttu-id="22a9b-106">Después de completar la grabación, puede guardar el contenido mediante la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) o [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) o mediante la función [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) con **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="22a9b-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="22a9b-107">La macro **MCIWndSave** guarda los datos en el archivo asociado a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="22a9b-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="22a9b-108">La macro **MCIWndSaveDialog** permite al usuario especificar un nombre de archivo y guardar los datos grabados en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="22a9b-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="22a9b-109">La función **GetSaveFileNamePreview** muestra el cuadro de diálogo **Guardar** como para elegir un archivo y permite que el usuario obtenga la vista previa (reproducir) del archivo.</span><span class="sxs-lookup"><span data-stu-id="22a9b-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="22a9b-110">Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo **Guardar** como, **GetSaveFileNamePreview** proporciona un pequeño control en el cuadro de diálogo para que el usuario pueda obtener una vista previa del contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="22a9b-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="22a9b-111">Puede guardar los datos grabados en un archivo seleccionado con **GetSaveFileNamePreview** mediante **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="22a9b-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




