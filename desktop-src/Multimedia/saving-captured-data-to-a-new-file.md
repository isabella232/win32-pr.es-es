---
title: Guardar los datos capturados en un archivo nuevo
description: Guardar los datos capturados en un archivo nuevo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Mensaje WM_CAP_FILE_SAVEAS
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775985"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="b8130-105">Guardar los datos capturados en un archivo nuevo</span><span class="sxs-lookup"><span data-stu-id="b8130-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="b8130-106">Si el usuario desea guardar los datos capturados, la aplicación debe guardar el contenido del archivo de captura en otro archivo mediante el [**mensaje \_ \_ \_ SaveAs archivo Cap de WM**](wm-cap-file-saveas.md) (o la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ).</span><span class="sxs-lookup"><span data-stu-id="b8130-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="b8130-107">Este mensaje no cambia el nombre ni el contenido del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b8130-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="b8130-108">La aplicación debe especificar un nombre para el nuevo archivo, ya que el archivo de captura conserva su nombre de archivo original.</span><span class="sxs-lookup"><span data-stu-id="b8130-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="b8130-109">Normalmente, un archivo de captura está preasignado para el segmento de captura más grande previsto y solo una parte de él podría usarse para capturar los datos.</span><span class="sxs-lookup"><span data-stu-id="b8130-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="b8130-110">Este mensaje solo copia la parte del archivo de captura que contiene los datos de captura.</span><span class="sxs-lookup"><span data-stu-id="b8130-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




