---
title: User-Selected compresores
description: User-Selected compresores
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Administrador de compresión de vídeo (VCM), compresores seleccionados por el usuario
- VCM (Administrador de compresión de vídeo), compresores seleccionados por el usuario
- ICCompressorChoose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994391"
---
# <a name="user-selected-compressors"></a><span data-ttu-id="9409c-106">User-Selected compresores</span><span class="sxs-lookup"><span data-stu-id="9409c-106">User-Selected Compressors</span></span>

<span data-ttu-id="9409c-107">Al comprimir los datos, la aplicación puede usar la función [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para crear un cuadro de diálogo en el que el usuario pueda seleccionar el compresor.</span><span class="sxs-lookup"><span data-stu-id="9409c-107">When compressing data, your application can use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to create a dialog box in which the user can select the compressor.</span></span> <span data-ttu-id="9409c-108">Puede especificar marcas para esta función para permitir que el usuario especifique la frecuencia del fotograma clave y la velocidad de datos de la película, o para mostrar una ventana de vista previa.</span><span class="sxs-lookup"><span data-stu-id="9409c-108">You can specify flags for this function to allow the user to specify the key-frame frequency and the movie-data rate, or to display a preview window.</span></span>

<span data-ttu-id="9409c-109">El compresor seleccionado por el usuario se abre automáticamente y su identificador se devuelve en el miembro HIC de la estructura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada en **ICCompressorChoose**.</span><span class="sxs-lookup"><span data-stu-id="9409c-109">The compressor selected by the user is automatically opened and its handle is returned in the hic member of the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure specified in **ICCompressorChoose**.</span></span>

<span data-ttu-id="9409c-110">Si usa **ICCompressorChoose**, use la función [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para cerrar el compresor y liberar los recursos asociados a la estructura **COMPVARS** .</span><span class="sxs-lookup"><span data-stu-id="9409c-110">If you use **ICCompressorChoose**, use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function to close the compressor and free any resources associated with the **COMPVARS** structure.</span></span>

 

 




