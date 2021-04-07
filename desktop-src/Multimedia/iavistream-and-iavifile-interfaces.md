---
title: Interfaces IAVIStream y IAVIFile
description: Interfaces IAVIStream y IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaz IAVIStream
- Interfaz IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903581"
---
# <a name="iavistream-and-iavifile-interfaces"></a><span data-ttu-id="1c39e-105">Interfaces IAVIStream y IAVIFile</span><span class="sxs-lookup"><span data-stu-id="1c39e-105">IAVIStream and IAVIFile Interfaces</span></span>

<span data-ttu-id="1c39e-106">Las interfaces [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) y [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contienen los métodos que usan los controladores de archivos y secuencias.</span><span class="sxs-lookup"><span data-stu-id="1c39e-106">The [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) and [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) interfaces contain the methods used by file and stream handlers.</span></span> <span data-ttu-id="1c39e-107">El tipo de datos **PAVISTREAM** es un puntero a un objeto de flujo AVI (a través de la interfaz **IAVIStream** ) y el tipo de datos **PAVIFILE** es un puntero a un objeto de archivo AVI (a través de la interfaz **IAVIFile** ).</span><span class="sxs-lookup"><span data-stu-id="1c39e-107">The **PAVISTREAM** data type is a pointer to an AVI stream object (through the **IAVIStream** interface) and the **PAVIFILE** data type is a pointer to an AVI file object (through the **IAVIFile** interface).</span></span>

<span data-ttu-id="1c39e-108">Para crear un puntero de objeto en C, asigne primero el espacio para una estructura que sea lo suficientemente grande como para contener el puntero a la tabla de funciones virtuales y los demás miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="1c39e-108">To create an object pointer in C, first allocate space for a structure that is large enough to contain the pointer to the virtual function table and the other data members.</span></span> <span data-ttu-id="1c39e-109">Cree una tabla de función virtual para los métodos del tipo de secuencia y, a continuación, establezca el puntero en la tabla de función virtual en la dirección de la tabla de función virtual.</span><span class="sxs-lookup"><span data-stu-id="1c39e-109">Create a virtual function table for the methods for your type of stream, then set the pointer to the virtual function table to the address of the virtual function table.</span></span>

 

 




